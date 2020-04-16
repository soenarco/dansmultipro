<template>
  <header id="site-header">
    <div class="container">
      <div class="row align-items-center justify-content-center">
        Header
      </div>
    </div>
  </header>
</template>

<script>

export default {
  name: 'Header',
};
</script>

<style lang="scss" scoped>
#site-header {
  z-index: 2;
  background-color: white;
  border-top: 1px solid $grey-light;
  border-bottom: 1px solid $grey-light;
}

.header-logo {
  max-width: 200px;
}
</style>
