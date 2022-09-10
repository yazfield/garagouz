<template>
  <section>
    <h2>المشاريع</h2>
    <card>
      <h3>ڤاراڤوز EP</h3>
      <iframe
        width="560"
        height="315"
        src="https://www.youtube-nocookie.com/embed/videoseries?list=PLBaYP0sii_CSSNDo-vIArIaLyMTmP83Ni"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
      ></iframe>
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
    </card>
    <hr />
    <card>
      <h3>زليج beats</h3>
      <iframe
        width="560"
        height="315"
        src="https://www.youtube-nocookie.com/embed/videoseries?list=PLBaYP0sii_CSSNDo-vIArIaLyMTmP83Ni"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
      ></iframe>
      <div class="social">
        <ul>
          <li>
            <a
              href="https://youtube.com/playlist?list=PLBaYP0sii_CSSNDo-vIArIaLyMTmP83Ni"
            >
              <img src="~/assets/logo-youtube.png" alt="Youtube" />
            </a>
          </li>
          <li>
            <a href="https://www.instagram.com/el.janyor">
              <img src="~/assets/logo-instagram.png" alt="Instagram" />
            </a>
          </li>
          <li>
            <a href="https://soundcloud.com/el-janyor/sets/zelij-beats">
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
    </card>
  </section>
</template>
<style lang="scss" scoped>
h4 {
  font-size: 24px;
  color: var(--color-purple);
}
h2 {
  font-size: 82px;
}
hr {
  border: none;
  border-top: 1px solid var(--color-purple);
  margin: 16px;
  margin-top: 32px;
}
iframe {
  width: 100%;
  height: 200px;
}
.social {
  margin: 0;
  margin-top: 8px;
  ul {
    margin: 0;
    width: 70%;
    font-size: 12px;
  }
}
h2 {
  margin-bottom: 32px;
}
</style>
