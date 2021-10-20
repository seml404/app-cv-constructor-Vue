<template>
  <div class="card card-w70">
    <h3 v-if="content.length < 1">
      Добавьте первый блок, чтобы увидеть результат
    </h3>
    <component
      :key="item.id"
      v-for="item in content"
      :is="item.type"
      :partContent="item"
    ></component>
  </div>
</template>

<script>
import AppPartTitle from "./parts/AppPartTitle.vue";
import AppPartSubtitle from "./parts/AppPartSubtitle";
import AppPartText from "./parts/AppPartText.vue";
import AppPartAvatar from "./parts/AppPartAvatar.vue";
export default {
  data() {
    return {};
  },
  props: ["content"],
  components: {
    AppPartTitle,
    AppPartSubtitle,
    AppPartText,
    AppPartAvatar,
  },
};
</script>

<style></style>
