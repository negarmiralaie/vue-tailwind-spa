<template>
  <section class="desktopNavbar md:px-5% md:w-full flex">
    <section class="ml-auto w-1/2 hidden md:inline relative">
      <button
        class="bg-customOrange font-bold hover:bg-customYellow hover:text-black text-white transition ease-in-out delay-150 hover:scale-105 rounded-3xl px-6 py-3 absolute right-1/4"
      >
        ثبت درخواست ویزیت
      </button>
    </section>

    <section
      class="flex flex-col md:flex-row items-center justify-between hidden md:flex w-1/2"
    >
      <router-link
        to="/about-us"
        class="desktopNavbarElement py-3 transition ease-in-out delay-150 hover:scale-105 font-bold"
        :class="{ activeDesktopNavbarElement: $route.name === 'about-us' }"
        >درباره ما</router-link
      >
      <router-link
        to="/services"
        class="desktopNavbarElement py-3 transition ease-in-out delay-150 hover:scale-105 font-bold"
        :class="{ activeDesktopNavbarElement: $route.name === 'services' }"
        >خدمات</router-link
      >
      <router-link
        to="/blog"
        class="desktopNavbarElement py-3 transition ease-in-out delay-150 hover:scale-105 font-bold"
        :class="{ activeDesktopNavbarElement: $route.name === 'blog' }"
        >بلاگ</router-link
      >
      <router-link
        to="/contact-us"
        class="desktopNavbarElement py-3 transition ease-in-out delay-150 hover:scale-105 font-bold"
        :class="{ activeDesktopNavbarElement: $route.name === 'contact-us' }"
        >ارتباط با ما</router-link
      >
      <router-link
        to="/"
        class="desktopNavbarLogo text-left text-2xl md:text-4xl font-extrabold"
        >MED</router-link
      >
    </section>
  </section>
</template>

<script>
export default {};
</script>
