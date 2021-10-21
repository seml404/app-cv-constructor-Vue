<template>
  <p>
    <button class="btn primary" @click="this.$emit('requestForComments')">
      Загрузить комментарии
    </button>
  </p>
  <div class="card">
    <h2>Комментарии</h2>
    <ul class="list" v-if="commentsTotal.length > 1">
      <li class="list-item" v-for="commentItem of commentsTotal">
        <div>
          <p>
            <strong>{{ commentItem.name }}</strong>
          </p>
          <small>{{ commentItem.body }}</small>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  emits: ["requestForComments"],
  props: ["commentsTotal"],
};
</script>

<style></style>
