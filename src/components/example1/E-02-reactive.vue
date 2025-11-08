<template>
  <div>{{ fullName }}</div>
</template>

<script>
export default
{
  name: "E02Reactive",

  data()
  {
    return {
      firstName: "Seokmin",
      lastName: "Kang"
    };
  },

  mounted()
  {
    console.log('mounted');

    setTimeout(() => {
      this.lastName = "Gang";
    }, 2000);
  },

  computed: {
    fullName()
    {
      return this.firstName + " " + this.lastName;
    }
  }
};
</script>
