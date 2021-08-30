<template>
  <div class="stats-preview">
    <slot />
  </div>
</template>

<script>
export default {
  name: "Page"
}
</script>

<style lang="scss" scoped>
    .stats-preview {
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
      width: 100%;
      height: 100%;
      background: #0a0c1c;

      @media (max-width: 475px) {
        height: auto;
      }
    }
</style>
