<template>
  <form class="card card-w30">
    <div class="form-control">
      <label for="type">Тип блока</label>
      <select id="type" v-model="optionVariant">
        <option
          v-for="option in selectOptions"
          :value="option.value"
          :key="option.id"
        >
          {{ option.text }}
        </option>
      </select>
    </div>
    <div class="form-control">
      <label for="value">Значение</label>
      <textarea id="value" rows="3" v-model="textContent"></textarea>
    </div>
    <button
      class="btn primary"
      @click.prevent="formSubmitted"
      :disabled="textContent.length < 3"
    >
      Добавить
    </button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      textContent: "",
      optionVariant: "title",
    };
  },
  emits: ["formSubmitted"],
  props: ["selectOptions"],
  methods: {
    formSubmitted() {
      this.$emit("formSubmitted", {
        titleSelected: this.optionVariant,
        textTyped: this.textContent,
      });
      this.textContent = "";
      this.optionVariant = "title";
      // this.$forceUpdate();
    },
  },
};
</script>

<style></style>
