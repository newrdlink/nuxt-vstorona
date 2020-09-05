<template>
  <section>
    <h1>Users page</h1>
    <ul>
      <li v-for="item of users" :key="item">
        <a href="#" @click.prevent="goTo(item)">User {{ item }}</a>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  data: () => ({
    users: [1, 2, 3, 4, 5]
  }),
  methods: {
    goTo(user) {
      this.$router.push("/users/" + user);
    }
  }
};
</script>
