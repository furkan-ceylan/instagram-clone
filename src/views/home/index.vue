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
      </div>

      <Post />

      <Post />
    </div>
    <div class="sidebar">
      <div class="sidebar-profile">
        <div class="head-avatar">
          <img
            src="https://img.pngio.com/profile-icon-png-image-free-download-searchpngcom-profile-icon-png-673_673.png"
            alt="avatar"
            width="60px"
            height="60px"
          />
        </div>
        <div class="sidebar-name">
          <div class="sidebar-username">
            <CustomText tag="b" size="large">username</CustomText>
          </div>
          <div class="sidebar-displayname">
            <CustomText size="normal">displayname</CustomText>
          </div>
        </div>
        <div class="sidebar-switch">
          <p><CustomText tag="b" size="large">Switch</CustomText></p>
        </div>
      </div>
      <div class="suggestions">
        <div class="suggestions-foryou">
          <CustomText tag="b" size="normal">Suggestions For You</CustomText>
        </div>
        <div class="suggestions-see">
          <CustomText tag="b" size="normal">See All</CustomText>
        </div>
      </div>
      <div class="sidebar-sug-profile">
        <div class="head-avatar">
          <img
            src="https://img.pngio.com/profile-icon-png-image-free-download-searchpngcom-profile-icon-png-673_673.png"
            alt="avatar"
            width="40px"
            height="40px"
          />
        </div>
        <div class="sidebar-name">
          <div class="sidebar-username">
            <CustomText tag="b" size="large">username</CustomText>
          </div>
          <div class="sidebar-displayname">
            <CustomText size="normal">displayname</CustomText>
          </div>
        </div>
        <div class="sidebar-switch">
          <p><CustomText tag="b" size="large">Follow</CustomText></p>
        </div>
      </div>
      <div class="sidebar-sug-profile">
        <div class="head-avatar">
          <img
            src="https://img.pngio.com/profile-icon-png-image-free-download-searchpngcom-profile-icon-png-673_673.png"
            alt="avatar"
            width="40px"
            height="40px"
          />
        </div>
        <div class="sidebar-name">
          <div class="sidebar-username">
            <CustomText tag="b" size="large">username</CustomText>
          </div>
          <div class="sidebar-displayname">
            <CustomText size="normal">displayname</CustomText>
          </div>
        </div>
        <div class="sidebar-switch">
          <p><CustomText tag="b" size="large">Follow</CustomText></p>
        </div>
      </div>
            <div class="sidebar-sug-profile">
        <div class="head-avatar">
          <img
            src="https://img.pngio.com/profile-icon-png-image-free-download-searchpngcom-profile-icon-png-673_673.png"
            alt="avatar"
            width="40px"
            height="40px"
          />
        </div>
        <div class="sidebar-name">
          <div class="sidebar-username">
            <CustomText tag="b" size="large">username</CustomText>
          </div>
          <div class="sidebar-displayname">
            <CustomText size="normal">displayname</CustomText>
          </div>
        </div>
        <div class="sidebar-switch">
          <p><CustomText tag="b" size="large">Follow</CustomText></p>
        </div>
      </div>
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
  overflow: hidden;
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

  .head-avatar {
    display: inline-flex;
    border-radius: 50%;
    cursor: pointer;
  }

  .head-avatar img {
    border-radius: 50%;
  }

  .sidebar-profile {
    margin-bottom: 20px;
    height: 115px;
    display: flex;
    flex-direction: row;
    align-items: center;
    padding: 5px;
  }

  .sidebar-sug-profile {
    height: 45px;
    display: flex;
    flex-direction: row;
    align-items: center;
    padding: 5px;
  }
  .sidebar-username {
    cursor: pointer;
  }
  .sidebar-name {
    margin-left: 16px;
  }
  .sidebar-displayname {
    color: gray;
  }
  .sidebar-switch {
    margin-left: auto;
    margin-right: 0;
    cursor: pointer;
  }

  .sidebar-switch p {
    margin-left: auto;
    margin-right: 0;
    color: #0095f6;
    padding-right: 16px;
  }
  .suggestions {
    display: flex;
    flex-direction: row;
    padding: 5px;
  }

  .suggestions-foryou {
    color: gray;
  }

  .suggestions-see {
    margin-left: auto;
    margin-right: 0;
    cursor: pointer;
    padding-right: 15px;
  }
}
</style>
