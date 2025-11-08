<template>
  <div>
    <input v-model="id" />
    <input v-model="password" />
    <p>{{ message }}</p>

    <button @click="() => {
      this.message = this.id + '' + this.password;
    }">whoami</button>
  </div>
</template>

<script>
export default
{
  name: "E03Binding",

  data()
  {
    return {
      message: "로그인하세요",
      id: "ID ",
      password: "PASSWORD"
    };
  }
};
</script>
