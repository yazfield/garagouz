<template>
  <div class="container">
    <nav class="nav">
      <a href="/" class="nav__logo">
        <img
          class="nav__logo-img"
          src="~/assets/logo-black.png"
          alt="El Janyor"
        />
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
    <footer>
      <a href="/" class="nav__logo">
        <img
          class="nav__logo-img"
          src="~/assets/logo-black.png"
          alt="El Janyor"
        />
        <h1>الجنيور</h1>
      </a>
      <div class="social">
        <ul>
          <li>
            <a href="https://www.youtube.com/channel/UCbjMfMJ6LX2ENeK0Q2ktwPw">
              <img src="~/assets/logo-youtube.png" alt="Youtube" />
            </a>
          </li>
          <li>
            <a href="https://www.instagram.com/el.janyor">
              <img src="~/assets/logo-instagram.png" alt="Instagram" />
            </a>
          </li>
          <li>
            <a href="https://soundcloud.com/el-janyor">
              <img src="~/assets/logo-soundcloud.png" alt="SoundCloud" />
            </a>
          </li>
          <li>
            <a href="/mazal">
              <img src="~/assets/logo-spotify.png" alt="Spotify" />
            </a>
          </li>
        </ul>
      </div>
    </footer>
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
@import url("~/assets/main.scss");

main {
  overflow: hidden;
  font-family: "IBM Plex Sans Arabic", sans-serif;
  background-color: var(--colo-white);
  height: 100%;
  // min-height: 60vh;
  margin-bottom: 32px;
  width: 100%;
  display: flex;
  flex-direction: column;
}
.nav {
  background-color: var(--color-salmon-light);
  margin-bottom: 0;
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
      height: 42px;
      margin: 4px 16px 4px 8px;
      // margin-top: 2px;
      filter: hue-rotate(180deg) saturate(20) sepia(80%) brightness(80%);
    }
    h1 {
      font-size: 28px;
    }
  }
  .menu {
    list-style: none;
    padding: 0;
    display: flex;
    margin: 0;
    margin-right: 16px;
    margin-top: 8px;
    width: 45%;
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
.welcome {
  overflow: hidden;
}
h1 {
  font-size: 24px;
  margin: 0;
  color: var(--color-purple);
}
h2 {
  font-size: 96px;
  color: var(--color-salmon);
  line-height: 96px;
  opacity: 0.6;
  vertical-align: bottom;
  display: inline-block;
  // margin-top: 20px;
}
h3 {
  text-align: center;
  font-size: 32px;
  color: var(--color-red);
  margin-right: -20px;
}
section {
  padding: 8px;
}

footer {
  background-color: var(--color-purple-light);
  margin-top: auto;
  padding-top: 16px;
  .nav__logo {
    text-decoration: none;
    justify-content: center;
    img {
      filter: brightness(0) invert(1);
      height: 32px;
    }
    h1 {
      color: var(--color-white);
    }
  }
  .social {
    padding: 16px;
    margin: 0;
  }
}

@media print {
  @page {
    margin: 0;
  }
  .nav,
  footer {
    display: none;
  }
  body {
    margin: 1.6cm;
  }
}

.container {
  height: 100%;
  display: flex;
  flex-direction: column;
}

#__nuxt {
  height: 100%;
}
</style>
