<template src="@/templates/home.html"></template>

<script>
export default {
  name: "Home",
  data() {
    return {
      typeme: "",
      iamdata: [],
      showme: false,
      form: {
        email: "",
        name: "",
        food: null,
        checked: [],
      },
      foods: [
        { text: "Select One", value: null },
        "Carrots",
        "Beans",
        "Tomatoes",
        "Corn",
      ],
      show: true,
    };
  },
  methods: {
    clickme() {
      if (this.typeme === "") {
        alert("type something");
      } else {
        this.iamdata.push(this.typeme);
        this.typeme = "";
        console.log(this.iamdata);
      }
    },
    onSubmit(evt) {
      evt.preventDefault();
      this.showme = true;
    },

    onReset(evt) {
      evt.preventDefault();
      // Reset our form values
      this.form.email = "";
      this.form.name = "";
      this.form.food = null;
      this.form.checked = [];
      // Trick to reset/clear native browser form validation state
      this.show = false;
      this.$nextTick(() => {
        this.show = true;
        // to reset the form data result
        this.showme = false;
      });
    },
  },
};
</script>

