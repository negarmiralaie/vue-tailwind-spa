<template>
  <section
    v-if="isMobileNavbarOpen"
    @click="closeSideNavbar"
    class="mobile-navbar-bg cursor-pointer fixed w-screen bg-[rgba(0,0,0,0.6)] z-10"
  >
    <section
      class="mobile-navbar-content transform -translate-x-full transition duration-1000 ease-in-out flex gap-8 py-8 text-center flex-col items-center min-h-screen fixed z-20 top-0 right-0 w-full w-1/2 bg-customPink text-black"
    >
      <section class="overflow-hidden hover:bg-white w-full">
        <router-link
          to="/about-us"
          class="mobile-navbar-element block py-4 transition ease-in-out delay-150 hover:scale-105 font-bold"
          :class="{ activeMobileNavbarElement: $route.name === 'about-us' }"
          >درباره ما</router-link
        >
      </section>
      <section class="overflow-hidden hover:bg-white w-full">
        <router-link
          to="/services"
          class="mobile-navbar-element block py-4 transition ease-in-out delay-150 hover:scale-105 font-bold"
          :class="{ activeMobileNavbarElement: $route.name === 'services' }"
          >خدمات</router-link
        >
      </section>
      <section class="overflow-hidden hover:bg-white w-full">
        <router-link
          to="/blog"
          class="mobile-navbar-element block py-4 transition ease-in-out delay-150 hover:scale-105 font-bold"
          :class="{ activeMobileNavbarElement: $route.name === 'blog' }"
          >بلاگ</router-link
        >
      </section>
      <section class="overflow-hidden hover:bg-white w-full">
        <router-link
          to="/contact-us"
          class="mobile-navbar-element block py-4 transition ease-in-out delay-150 hover:scale-105 font-bold"
          :class="{ activeMobileNavbarElement: $route.name === 'contact-us' }"
          >ارتباط با ما</router-link
        >
      </section>
      <section class="w-3/4">
        <p
          class="bg-customOrange hover:bg-customYellow hover:text-black text-white rounded-3xl mobile-navbar-element mx-auto block py-3 px-6 transition ease-in-out delay-150 hover:scale-105 font-bold"
        >
          ثبت درخواست ویزیت
        </p>
      </section>
    </section>
  </section>

  <section class="md:hidden">
    <router-link
      to="/"
      class="text-left text-2xl md:text-3xl font-extrabold md:hidden"
      >MED</router-link
    >
  </section>
</template>

<script>
export default {
  props: ["isMobileNavbarOpen"],
  methods: {
    closeSideNavbar(event) {
      if (
        event.target.classList.contains("mobile-navbar-bg") ||
        event.target.classList.contains("mobile-navbar-element")
      ) {
        this.$emit("closeSideNavbar");
      }
    },
  },
};
</script>
