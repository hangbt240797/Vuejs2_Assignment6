<template>
  <section>
    <user-data @set-data="setUserData"></user-data>
    <active-user :yourName="user.name" :yourAge="user.age"></active-user>
  </section>
</template>

<script>
// import ActiveUser from './components/ActiveUser.vue';
// import UserData from './components/UserData.vue';
export default {
  //components: { UserData, ActiveUser },
  data() {
    return {
      user: {
        name: "Mss.Hang",
        age: 25,
      },
    };
  },
  methods: {
    setUserData(name, age) {
      this.user = {
        name: name,
        age: +age
      };
    }
  }
};
</script>

