<template>
  <div id="app">
    {{ user }}
    <hr />
    登录
    <hr />
    <form @submit.prevent="onSubmit">
      <label>
        <span>用户名</span>
        <my-input v-model="user.username" />
      </label>
      <label>
        <span>密码</span>
        <input type="password" v-model="user.password" />
      </label>
      <button type="submit">登录</button>
    </form>
  </div>
</template>

<script>
import MyInput from "./MyInput.vue";
export default {
  name: "App",
  data() {
    return {
      user: {
        username: 0,
        password: "",
      },
      x: [],
    };
  },
  components: { MyInput },
  methods: {
    onSubmit() {
      console.log(this.user);
    },
  },
};
</script>
