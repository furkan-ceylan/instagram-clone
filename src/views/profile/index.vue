<template>
  <div class="home">
    profile
    <div id="nav">
      <router-link to="/profile">Post</router-link>
      <router-link to="/profile/igtv">IGTV</router-link>
      <router-link to="/profile/save">Save</router-link>
      <router-link to="/profile/tag">Tag</router-link>
    </div>
    <router-view />
  </div>
</template>

<script>
export default {
  name: "profile",
};
</script>

<style></style>
