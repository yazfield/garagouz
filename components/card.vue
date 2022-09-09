<template>
  <div class="card">
    <slot />
  </div>
</template>

<style lang="scss">
$form-bg: var(--color-sepia);
$form-shadow: var(--color-salmon);
$form-primary-highlight: var(--color-purple-light);
$form-secondary-highlight: #ffc8ff;
$font-size: 14pt;
$font-face: "Fjalla One";
$font-color: #2a293e;
.card {
  background: var(--color-white);
  margin: 16px;
  padding: 16px 32px 50px 32px;
  border: 2px solid rgba(0, 0, 0, 1);
  box-shadow: 15px 15px 1px $form-shadow, 15px 15px 1px 2px rgba(0, 0, 0, 1);
}
input {
  display: block;
  width: 100%;
  font-size: $font-size;
  line-height: $font-size * 2;
  font-family: $font-face;
  margin-bottom: $font-size * 2;
  border: none;
  border-bottom: 5px solid rgba(0, 0, 0, 1);
  background: var(--color-white);
  min-width: 250px;
  padding-left: 5px;
  outline: none;
  color: rgba(0, 0, 0, 1);
}

input:focus {
  border-bottom: 5px solid var(--color-purple-light);
}

.button {
  color: var(--color-black);
  text-decoration: none;
  cursor: pointer;
  display: inline-block;
  margin: 0 auto;
  line-height: $font-size * 2;
  padding: 0 20px;
  background: var(--color-salmon);
  letter-spacing: 2px;
  transition: 0.2s all ease-in-out;
  outline: none;
  border: 1px solid rgba(0, 0, 0, 1);
  box-shadow: 3px 3px 1px 1px $form-primary-highlight,
    3px 3px 1px 2px rgba(0, 0, 0, 1);

  &:hover {
    background: var(--color-purple);
    color: white;
    border: 1px solid var(--color-purple);
  }
  &:active {
    box-shadow: 1px 1px 1px 1px $form-primary-highlight,
      1px 1px 1px 1px rgba(0, 0, 0, 1);
    transform: translate(2px, 2px);
  }
}

::selection {
  background: $form-secondary-highlight;
}

input:-webkit-autofill,
input:-webkit-autofill:hover,
input:-webkit-autofill:focus {
  border-bottom: 5px solid $form-primary-highlight;
  -webkit-text-fill-color: $font-color;
  -webkit-box-shadow: 0 0 0px 1000px $form-bg inset;
  transition: background-color 5000s ease-in-out 0s;
}

p {
  font-size: 14px;
  font-weight: lighter;
  margin: 0;
  color: var(--color-black);
}
</style>
