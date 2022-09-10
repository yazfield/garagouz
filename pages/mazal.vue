<template>
  <section>
    <h2>مازال شوية</h2>
    <h3>غي اصبر</h3>
    <card>
      <h4>سبوتيفاي</h4>
      <p>
        مشي طع كيفاه، كاين وحد beats راني دايرهم جايين Face B
        <br />
        أيا سبوتيفاي جاي يتعڤن في هاد الصوالح. شوية ونديره، غي ولي وشوف في يوتوب
        ولا، من بعد ساهل
      </p>
      <a href="#" class="button" @click="handleClick">ولي غدوة</a>
    </card>
  </section>
</template>

<script lang="ts" setup>
const router = useRouter();
const handleClick = () => {
  router.back();
};
</script>

<style lang="scss" scoped>
.button {
  margin-top: 16px;
}
h4 {
  font-size: 24px;
  color: var(--color-purple);
}
</style>
