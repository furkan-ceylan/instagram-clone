<template>
  <header class="header">
    <Container class="header-inner">
      <div class="nav1">
        <router-link to="/" class="logo">
          <img
            src="https://www.instagram.com/static/images/web/mobile_nav_type_logo.png/735145cfe0a4.png"
          />
        </router-link>
      </div>
      <div class="nav2">
        <form class="search">
          <input type="Text" placeholder="Search..." />
        </form>
      </div>

      <div class="nav3">
        <router-link to="/">
          <IconHomeFill v-if="$route.name === 'Home'" />
          <IconHome v-else />
        </router-link>
        <router-link to="/direct">
          <IconDirectFill v-if="$route.name === 'Direct'" />
          <IconDirect v-else />
        </router-link>
        <router-link to="/explore">
          <IconExploreFill v-if="$route.name === 'Explore'" />
          <IconExplore v-else />
        </router-link>
        <div class="icon-like">
        <router-link to="">
          <IconLike />
        </router-link>
        </div>
        <router-link to="/profile">
          <img
            src="https://img.pngio.com/profile-icon-png-image-free-download-searchpngcom-profile-icon-png-673_673.png"
            alt="avatar"
            width="30px"
            height="30px"
          />
        </router-link>
      </div>
    </Container>
  </header>
</template>

<script>
import Container from "./Container";
import Avatar from "./Avatar";
import IconHome from "@/icons/home.svg";
import IconHomeFill from "@/icons/home-fill.svg";
import IconDirect from "@/icons/direct.svg";
import IconDirectFill from "@/icons/direct-fill.svg";
import IconExplore from "@/icons/explore.svg";
import IconExploreFill from "@/icons/explore-fill.svg";
import IconLike from "@/icons/like.svg";

export default {
  name: "Header",
  components: {
    Container,
    IconHome,
    IconHomeFill,
    IconDirect,
    IconDirectFill,
    IconExplore,
    IconExploreFill,
    IconLike,
    Avatar,
  },
};
</script>

<style>
.header {
  z-index: 90;
  border-bottom: 1px solid rgb(209, 209, 209);
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  background-color: white;
}
.header-inner {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 52px;
  
}
.logo {
  font-size: 1.5rem;
  font-weight: bold;
}

.search {
  display: none;
  padding-right: 30px;
}

.nav3 {
  z-index: 90;
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: white;
  border-top: 1px solid rgb(209, 209, 209);
  height: 50px;
  display: flex;
  align-items: center;
  justify-content: space-around;
}

.nav3 img {
  padding-bottom: 5px;
}

.icon-like{
  display: none;
}

@media screen and (min-width: 980px) {
  .nav3 {
    height: auto;
    border: 0;
    position: static;
    justify-content: flex-end;
    
    
  }
  .nav3 a {
    margin-left: 20px;
  }
  .search {
    display: block;
    padding-right: 30px;
  }
  .search input {
    border: 1px solid rgb(209, 209, 209);
    background-color: rgb(250, 250, 250);
    border-radius: 4px;
    padding-left: 20px;
    padding-right: 20px;
    width: 200px;
    height: 25px;
  }
  .header-inner {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    align-items: center;
    height: 52px;
    
  }

  .icon-like{
  display: inherit;
}
}
</style>
