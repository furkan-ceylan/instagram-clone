<template>
  <div class="home">
    <div class="timeline">
      <div class="stories">
        <Avatar :size="52" />
        <Avatar :size="52" />
        <Avatar :size="52" />
        <Avatar :size="52" />
        <Avatar :size="52" />
        <Avatar :size="52" />
        <Avatar :size="52" />
        <Avatar :size="52" />
      </div>

      <Post />

      <Post />
    </div>
    <div class="sidebar">
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate,
        delectus ipsa? Optio aspernatur, voluptates ab repellat laudantium
        dolorum sed magnam facilis iure vitae dolor porro eum quasi
        necessitatibus in nobis.
      </p>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate,
        delectus ipsa? Optio aspernatur, voluptates ab repellat laudantium
        dolorum sed magnam facilis iure vitae dolor porro eum quasi
        necessitatibus in nobis.
      </p>
    </div>
  </div>
</template>

<script>
import CustomText from "@/components/CustomText";
import Avatar from "@/components/Avatar";
import Post from "@/components/Post";

export default {
  name: "index",
  components: {
    CustomText,
    Avatar,
    Post,
  },
};
</script>

<style scoped>
.home {
  max-width: 685px;
  margin-left: auto;
  margin-right: auto;
}
.timeline {
  padding-right: 10px;
}

.sidebar {
  display: none;
}

@media screen and (min-width: 980px) {
  .home {
    max-width: none;
    display: grid;
    grid-template-columns: 1fr 295px;
    grid-gap: 30px;
  }

  .sidebar {
    display: block;
  }

  .stories {
    border-radius: 3px;
    border: 1px solid rgb(209, 209, 209);
    background-color: white;
    margin-bottom: 20px;
    height: 115px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-around;
    padding: 5px;
  }
}
</style>
