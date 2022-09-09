<template>
  <div>
    <nav class="nav">
      <a href="/" class="nav__logo">
        <img class="nav__logo-img" src="~/assets/logo.png" alt="El Janyor" />
        <h1>الجنيور</h1>
      </a>
      <ul class="menu">
        <li><a href="/projects">المشاريع</a></li>
        <li><a href="/characters">الشخصيات</a></li>
      </ul>
    </nav>
    <main>
      <NuxtPage />
    </main>
  </div>
</template>
<script setup>
useHead({
  title: "الجنيور - ڤاراڤوز",
  // or, instead:
  // titleTemplate: (title) => `My App - ${title}`,
  viewport: "width=device-width, initial-scale=1, maximum-scale=1",
  charset: "utf-8",
  meta: [{ name: "description", content: "موقع الجنيور" }],
  htmlAttrs: {
    dir: "rtl",
  },
});
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=IBM+Plex+Sans+Arabic:wght@100;300;400;700&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;700&display=swap");
:root {
  --color-red: #b22827;
  --color-green: #1a4d2e;
  --color-purple: #3e0d2c;
  --color-purple-light: #955a7f;
  --color-grey: #dddfcf;
  --color-salmon: #f5d3ae;
  --color-salmon-dark: #f4c28d;
  --color-salmon-light: #f3dec8;

  --color-black: #121413;
  --color-sepia: #f6f4ea;
  --color-white: #f7f4f0;
  --color-concrete: #95a5a6;
}
$red: var(--color-red);
$green: var(--color-green);
$purple: var(--color-purple);
$grey: var(--color-grey);
$salmon: var(--color-salmon);
$black: var(--color-black);
$white: var(--color-white);
$sepia: var(--color-sepia);
$concrete: var(--color-concrete);
*,
:after,
:before {
  box-sizing: border-box;
}

:focus {
  outline: none;
}
body {
  padding: 0;
  width: 100%;
  height: 100%;
  margin: 0;
  top: 0;
  background-color: $white;
}
h1,
h2,
h3,
h4,
h5 {
  margin: 0;
  padding: 0;
  font-family: "Cairo", sans-serif;
}

br {
  margin-bottom: 8px;
}

main {
  font-family: "IBM Plex Sans Arabic", sans-serif;
  background-color: $white;
  height: 100vh;
  width: 100%;
  display: flex;
  flex-direction: column;
}
.nav {
  background-color: var(--color-salmon-light);
  margin-bottom: 12px;
  padding: 8px 0 8px 16px;
  box-shadow: rgba(0, 0, 0, 0.6) 0px 2px 0px;
  border-bottom: 3px solid var(--color-purple-light);
  display: flex;
  align-items: center;
  a {
    text-decoration: none;
  }
  &__logo {
    height: 42px;
    display: flex;
    // align-content: center;
    align-items: center;
    img {
      height: 64px;
      // margin-top: 2px;
      filter: hue-rotate(180deg) saturate(20) sepia(80%) brightness(80%);
    }
  }
  .menu {
    list-style: none;
    padding: 0;
    display: flex;
    margin: 0;
    margin-right: 16px;
    margin-top: 8px;
    width: 40%;
    justify-content: space-around;
    a {
      color: var(--color-red);
      font-weight: bold;
      &:hover {
        color: var(--color-purple);
      }
    }
  }
}
h1 {
  font-size: 24px;
  margin: 0;
  color: $purple;
}
h2 {
  font-size: 96px;
  color: $salmon;
  line-height: 96px;
  opacity: 0.6;
  vertical-align: bottom;
  display: inline-block;
  margin-top: 20px;
}
h3 {
  text-align: center;
  font-size: 32px;
  color: $red;
  margin-right: -20px;
}
section {
  padding: 8px;
}

@media print {
  @page {
    margin: 0;
  }
  .nav {
    display: none;
  }
  body {
    margin: 1.6cm;
  }
}
</style>
