<template>
  <div class="avatar">
    <img :src="partContent.text" />
  </div>
</template>

<script>
export default {
  props: ["partContent"],
};
</script>

<style></style>
