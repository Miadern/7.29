<template>
  <div>
    <button @click="editFn">换肤</button>
    <div class="todoapp">
      <todo-header></todo-header>
      <todo-main></todo-main>
      <todo-footer></todo-footer>
    </div>
    <buttonVue
      :height="300"
      :width="500"
      color="red"
      bgc="pink"
      :rad="true"
      type="niceBtn"
    >
      插槽</buttonVue
    >
  </div>
</template>

<script>
import buttonVue from "./components/button.vue";
import TodoFooter from "./components/TodoFooter.vue"; // shift + alt + 下
import TodoHeader from "./components/TodoHeader.vue"; // shift + alt + 下
import TodoMain from "./components/TodoMain.vue"; // shift + alt + 下

export default {
  data() {
    return {};
  },

  components: {
    buttonVue,
    TodoFooter,
    TodoHeader,
    TodoMain,
  },

  created() {},

  methods: {
    editFn() {
      this.$store.commit("sendColor", "green");
    },
  },
};
</script>

<style scoped></style>
