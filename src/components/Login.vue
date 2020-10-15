<template src="@/templates/login.html"></template>

<script>
export default {
  name: "Login",

  data() {
    return {
      username: "",
      password: "",
    };
  },
  methods: {
    go() {
      this.$router.push("/");
    },

    logme(e) {
      e.preventDefault();

      console.log(this.username, this.password);
      //this.$router.push('/');
      (this.username = null), (this.password = null);
    },
  },
};
</script>

<style lang="scss" scoped>
#form {
  margin: auto;
  padding: 10px;
  width: 25%;
  min-height: 38vh;
  border: 2px solid #1d7ef8;
  margin-top: 50px;
  color: #1d7ef8;
  font-weight: bold;
  text-align: start;
  border-radius: 20px;
  box-shadow: 5px 10px #1d7ef8;
  background: #c2e8ff;
}
h1 {
  text-align: center;
  padding: 10px;
  font-weight: bold;
  border-radius: 20px;
}

#input-button,
#input-button1 {
  font-size: 24px;
  border-radius: 24px;
  margin: 20px 0px 0px 25px;
  border: 0;
  display: flexbox;

  outline: none;
  transition: 0.25;

  float: left;
  padding: 0 18px;
}

#input-button:hover,
#input-button1:hover {
  color: black;
}
</style>