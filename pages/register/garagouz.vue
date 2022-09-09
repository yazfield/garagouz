<template>
  <section>
    <h2>ڤاراڤوز</h2>
    <card>
      <h4>إستمارة التسجيل</h4>
      <form method="get" action="/generate/ticket">
        <input
          required
          pattern="[a-zA-Z\u0621-\u064A]+"
          oninvalid="setCustomValidity('يرجى إدخال معلومات صحيحة، وخلينا مالترشاق')"
          type="text"
          name="name"
          placeholder="الإسم"
        />
        <input
          required
          pattern="[a-zA-Z\u0621-\u064A]+"
          oninvalid="setCustomValidity('يرجى إدخال معلومات صحيحة، وخلينا مالترشاق')"
          type="text"
          name="city"
          placeholder="المدينة"
        />
        <p>* ليكن في علمكم أننا لا نحتفظ بالمعلومات على السرفر</p>
        <button type="submit" class="button" @click="handleClick">سجل</button>
      </form>
    </card>
  </section>
</template>
<script lang="ts" setup>
const handleClick = (e: MouseEvent) => {
  console.log("click");
};
</script>
<style lang="scss" scoped>
.input {
  display: flex;
  flex-direction: column;
}
.button {
  margin-top: 16px;
}
p {
  font-size: 8px;
}
</style>
