<template>
  <div>
    <section class="item">
      <div class="info">
        <h3>المنتظر</h3>
        <img src="~/assets/logo.png" alt="المنتظر" />
        <h4>معلومات عامة</h4>
        <ul>
          <li><strong>الإسم: </strong><span>المنتظر</span></li>
          <li><strong>مكان الميلاد: </strong><span>قم</span></li>
          <li><strong>المهنة: </strong><span>قائد طائفة سرية</span></li>
          <li>
            <strong>الألقاب: </strong><span>حسن الصباح، المعلم، الجنيور</span>
          </li>
        </ul>
      </div>
    </section>
    <section class="item blur">
      <div class="info">
        <h3>الزعيم</h3>
        <img src="~/assets/logo.png" alt="الزعيم" />
        <h4>معلومات عامة</h4>
        <ul>
          <li><strong>الإسم: </strong><span>الزعيم</span></li>
          <li><strong>مكان الميلاد: </strong><span>وهران</span></li>
          <li><strong>المهنة: </strong><span>رئيس جمهورية وهران</span></li>
          <li><strong>الألقاب: </strong><span>القائد، الباي، الجنيور</span></li>
        </ul>
      </div>
    </section>
    <section class="item blur">
      <div class="info">
        <h3>الرأسمالي</h3>
        <img src="~/assets/logo.png" alt="الرأسمالي" />
        <h4>معلومات عامة</h4>
        <ul>
          <li><strong>الإسم: </strong><span>الرأسمالي</span></li>
          <li><strong>مكان الميلاد: </strong><span>وهران</span></li>
          <li><strong>المهنة: </strong><span>رائد أعمال</span></li>
          <li><strong>الألقاب: </strong><span>مول الشي، الجنيور</span></li>
        </ul>
      </div>
    </section>
  </div>
</template>
<style lang="scss">
body,
main {
  background-color: var(--color-grey);
}
</style>

<style lang="scss" scoped>
.item {
  margin: 16px 24px;
  display: flex;
  .info {
    width: 100%;
    display: flex;
    align-items: center;
    flex-direction: column;
    img {
      width: 194px;
      border: 1px solid var(--color-purple);
    }
    h3 {
      margin: 0;
      background-color: var(--color-purple);
      width: 194px;
      color: var(--color-salmon);
    }
    h4 {
      margin: 16px 0;
    }
    ul {
      width: 340px;
      background-color: var(--color-salmon-light);
      border: 2px solid var(--color-purple-light);
      list-style-type: none;
      margin: 0;
      padding: 16px;
      li {
        display: flex;
        * {
          display: flex;
          width: 50%;
        }
        span {
          font-weight: light;
          font-style: italic;
        }
      }
    }
  }
}
.blur img {
  filter: blur(50px);
}
</style>
