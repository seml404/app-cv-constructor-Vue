<template>
  <div class="container column">
    <app-add-content></app-add-content>

    <app-result-display></app-result-display>
  </div>
  <div class="container">
    <p>
      <button class="btn primary">Загрузить комментарии</button>
    </p>
    <div class="card">
      <h2>Комментарии</h2>
      <ul class="list">
        <li class="list-item">
          <div>
            <p><strong>test@microsoft.com</strong></p>
            <small
              >Lorem ipsum dolor sit amet, consectetur adipisicing elit.
              Eligendi, reiciendis.</small
            >
          </div>
        </li>
      </ul>
    </div>
    <div class="loader"></div>
  </div>
</template>

<script>
import AppAddContent from "./components/AppAddContent.vue";
import AppResultDisplay from "./components/AppResultDisplay.vue";
export default {
  components: { AppAddContent, AppResultDisplay },
};
</script>

<style>
.avat AppResultDisplayar {
  display: flex;
  justify-content: center;
}

.avatar img {
  width: 150px;
  height: auto;
  border-radius: 50%;
}
</style>
