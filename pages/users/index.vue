<template>
  <section>
    <h1>{{ pageTitle }}</h1>
    <ul>
      <li v-for="item of users" :key="item.id">
        <a href="#" @click.prevent="goTo(item)"
          >{{ item.name }} with email ({{ item.email }})</a
        >
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  asyncData({ $axios, error }) {
    return $axios
      .$get("https://jsonplaceholder.typicode.com/users")
      .then(users => {
        return {
          users
        };
      })
      .catch(err => {
        error(err);
      });
    // return new Promise(resolve => {
    //   setTimeout(() => {
    //     resolve({ users: [1, 2, 3, 4, 5] });
    //   }, 500);
    // });
  },
  data() {
    return { pageTitle: "User page" };
  },
  methods: {
    goTo(user) {
      this.$router.push("/users/" + user.id);
    }
  }
};
</script>
