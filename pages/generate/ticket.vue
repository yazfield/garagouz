<template>
  <section class="ticket">
    <div class="web">
      <h2>شكرا</h2>
      <h3>على شراء التذكرة</h3>
      <card>
        <h4>تذكرة مسرحية ڤاراڤوز</h4>
        <ul class="list">
          <li><strong>رقم التذكرة: </strong> {{ ticketNumber }}</li>
          <li><strong>الإسم: </strong> {{ name }}</li>
          <li><strong>المدينة: </strong> {{ city }}</li>
          <li><strong>السعر: </strong> 10 دورو</li>
          <li><strong>المقعد: </strong> 31</li>
          <li><strong>التاريخ: </strong> {{ date }}</li>
        </ul>
        <button class="button" @click="handlePrint">طبع التذكرة</button>
      </card>
    </div>
    <div class="print">
      <div class="printed-ticket">
        <div class="printed-ticket__inner">
          <div class="nav__logo title">
            <img
              class="nav__logo-img"
              src="~/assets/logo.png"
              alt="El Janyor"
            />
            <h1>الجنيور</h1>
            <h1 class="secondtitle">مسرحية الڤاراڤوز</h1>
          </div>
          <div class="content">
            <ul class="list">
              <li><strong>الإسم: </strong> {{ name }}</li>
              <li><strong>المدينة: </strong> {{ city }}</li>
            </ul>
            <ul class="list">
              <li><strong>السعر: </strong> 10 دورو</li>
              <li><strong>المقعد: </strong> 31</li>
              <li><strong>التاريخ: </strong> {{ date }}</li>
            </ul>
            <hr />
            <div class="qrcode">
              <span>{{ ticketNumber }}</span>
              <img src="~/assets/qr-code.png" alt="Qr Code" />
            </div>
          </div>
        </div>
      </div>
      <hr class="dotted" />

      <div class="social">
        <ul>
          <li>
            <a href="https://www.youtube.com/channel/UCbjMfMJ6LX2ENeK0Q2ktwPw">
              <img src="~/assets/logo-youtube.png" alt="Youtube" />
              يوتوب
            </a>
          </li>
          <li>
            <a href="https://www.instagram.com/el.janyor">
              <img src="~/assets/logo-instagram.png" alt="Instagram" />
              إنسطغرام
            </a>
          </li>
          <li>
            <a href="https://soundcloud.com/el-janyor">
              <img src="~/assets/logo-soundcloud.png" alt="SoundCloud" />
              ساوند كلاود
            </a>
          </li>
          <li>
            <a href="https://www.eljanyor.art">
              <img src="~/assets/logo-spotify.png" alt="Spotify" />
              سبوتيفاي
            </a>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { Base64, formatDate } from "@/helpers";

const route = useRoute();

let name = route.query.name as string;
let city = route.query.city as string;
let date = formatDate(new Date());
let ticketNumber = Base64.encode(name + city + date).slice(0, 10);

const handlePrint = () => {
  if (typeof window === "undefined") {
    return;
  }
  window.print();
};
</script>

<style lang="scss">
@media print {
  .ticket {
    .web {
      display: none;
    }
  }
}

.printed-ticket {
  margin: 0;
  margin-top: 32px;
  display: flex;

  flex-direction: column;
  -webkit-print-color-adjust: exact;
  border: 1px solid var(--color-purple-light);
  background: repeating-linear-gradient(
    -65deg,
    var(--color-salmon-light),
    var(--color-salmon-dark) 1px,
    var(--color-salmon-dark) 8px,
    var(--color-salmon-dark) 12px
  );
  //   padding: 4px;
  width: 94%;
  border-radius: 5px;
  $border: 10px;
  &__inner {
    padding: 8px;
    background: var(--color-sepia);
    border: $border dotted var(--color-salmon-dark);
    width: 100%;
    position: relative;
    &:before {
      content: " ";
      position: absolute;
      z-index: 1;
      top: -$border;
      left: -$border;
      right: -$border;
      bottom: -$border;
      border: 5px solid var(--color-salmon-dark);
    }
  }
  .title {
    margin-bottom: 8px;
    .secondtitle {
      margin-right: 96px;
    }
    img {
      margin-top: 8px;
    }
  }
  .content {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    .list {
      list-style-type: none;
    }
    hr {
      background: var(--color-purple);
      border: none;
      width: 2px;

      margin: 16px 0;
      height: 72px;
    }
    .qrcode {
      //   margin-right: 48px;
      margin-top: -18px;
      display: flex;
      flex-direction: column;
      span {
        font-size: 10px;
        text-align: center;
        color: var(--color-purple);
      }
      img {
        width: 96px;
        border: 2px solid var(--color-purple);
      }
    }
  }
}

@media screen {
  .ticket {
    .print {
      display: none;
    }
    .list {
      list-style-type: none;
      margin: 0;
      padding: 0;
      margin-right: 8px;
      margin-bottom: 16px;
      margin-top: 8px;
      li {
        margin: 4px 0;
      }
    }
  }
}

.social {
  display: flex;
  margin-top: 96px;
  justify-content: center;
  ul {
    width: 50%;
    list-style-type: none;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: space-between;
  }
  img {
    width: 24px;
    margin: 0 4px;
  }
  a {
    display: flex;
    align-items: center;
  }
}

hr.dotted {
  margin: 0;
  padding: 0;
  margin-top: 96px;
  width: 94%;
  border-top: 1px dashed black;
}
</style>
