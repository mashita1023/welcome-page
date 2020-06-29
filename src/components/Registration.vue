<template>
<div id="front">
  <dl>
    <dt>E-mail</dt>
    <dd><input type="text"></dd>
    <dt>PW</dt>
    <dd><input type="password"></dd>
    <dt><input type="submit">登録</dt>
    <dt><a uref="">登録していない方はこちら</a></dt>
    <dt><a uref="">パスワードがわからない場合</a></dt>
  </dl>
</div>
</template>

<script>
export default {
  name: 'Registration',
};
</script>

<style lang="scss">
  .front {
    position: absolute;
  }
</style>