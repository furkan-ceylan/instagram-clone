<template>
  <div class="home">
    <div class="profile-header">
      <div class="head-avatar">
        <img
          src="https://img.pngio.com/profile-icon-png-image-free-download-searchpngcom-profile-icon-png-673_673.png"
          alt="avatar"
          width="180px"
          height="180px"
        />
      </div>
      <div class="head-profile-detail">
        <div class="detail-name">
          <div class="detail-name-username">
            <CustomText class="thin" size="xxlarge">username</CustomText>
          </div>
          <div class="detail-name-edit">
            <button class="action-edit" type="button">
              <CustomText tag="b" size="normal">Edit Profile</CustomText>
            </button>
          </div>
          <div class="icon-options">
            <IconOptions />
          </div>
        </div>
        <div class="detail-numbers">
          <div class="number-1">
            <CustomText tag="b" size="xlarge">5 </CustomText>
            <CustomText size="xlarge">posts</CustomText>
          </div>
          <div class="number-1">
            <CustomText tag="b" size="xlarge">124 </CustomText>
            <CustomText size="xlarge">followers</CustomText>
          </div>
          <div class="number-1">
            <CustomText tag="b" size="xlarge">135 </CustomText>
            <CustomText size="xlarge">following</CustomText>
          </div>
        </div>
        <div class="detail-info">
          <CustomText tag="b" size="xlarge">userinfo</CustomText>
        </div>
      </div>
    </div>
    <div class="detail-numbers-mob">
      <div class="number-1">
        <CustomText tag="b" size="xlarge">5 </CustomText>
        <CustomText size="xlarge">posts</CustomText>
      </div>
      <div class="number-1">
        <CustomText tag="b" size="xlarge">124 </CustomText>
        <CustomText size="xlarge">followers</CustomText>
      </div>
      <div class="number-1">
        <CustomText tag="b" size="xlarge">135 </CustomText>
        <CustomText size="xlarge">following</CustomText>
      </div>
    </div>
    <div class="tabs">
      <div>
        <router-link to="/profile">
          <IconPostsFill v-if="$route.name === 'ProfilePost'" />
          <IconPosts v-else />
          <span
            :class="[
              $route.name === 'ProfilePost'
                ? 'tabs-item-active'
                : 'tabs-item-deactive',
            ]"
          >
            POSTS</span
          >
        </router-link>
      </div>
      <div>
        <router-link to="/profile/igtv">
          <IconIGTVFill v-if="$route.name === 'ProfileIGTV'" />
          <IconIGTV v-else />
          <span
            :class="[
              $route.name === 'ProfileIGTV'
                ? 'tabs-item-active'
                : 'tabs-item-deactive',
            ]"
          >
            IGTV</span
          >
        </router-link>
      </div>
      <div>
        <router-link to="/profile/save">
          <IconSavedFill v-if="$route.name === 'ProfileSave'" />
          <IconSaved v-else />
          <span
            :class="[
              $route.name === 'ProfileSave'
                ? 'tabs-item-active'
                : 'tabs-item-deactive',
            ]"
          >
            SAVED</span
          >
        </router-link>
      </div>
      <div>
        <router-link to="/profile/tag">
          <IconTaggedFill v-if="$route.name === 'ProfileTag'" />
          <IconTagged v-else />
          <span
            :class="[
              $route.name === 'ProfileTag'
                ? 'tabs-item-active'
                : 'tabs-item-deactive',
            ]"
          >
            TAGGED</span
          ></router-link
        >
      </div>
    </div>
    <div class="tab-view">
      <router-view />
    </div>
  </div>
</template>

<script>
import CustomText from "@/components/CustomText";
import Avatar from "@/components/Avatar";
import Post from "@/components/Post";
import IconOptions from "@/icons/options.svg";
import IconPostsFill from "@/icons/posts-fill.svg";
import IconIGTVFill from "@/icons/igtv-fill.svg";
import IconSavedFill from "@/icons/saved-fill.svg";
import IconTaggedFill from "@/icons/tagged-fill.svg";
import IconPosts from "@/icons/posts.svg";
import IconIGTV from "@/icons/igtv.svg";
import IconSaved from "@/icons/saved.svg";
import IconTagged from "@/icons/tagged.svg";

export default {
  name: "profile",
  components: {
    CustomText,
    Avatar,
    Post,
    IconOptions,
    IconPosts,
    IconIGTV,
    IconSaved,
    IconTagged,
    IconPostsFill,
    IconIGTVFill,
    IconSavedFill,
    IconTaggedFill,
  },
};
</script>

<style scoped>
.home {
  margin-left: auto;
  margin-right: auto;
}

.profile-header {
  display: grid;
  grid-template-columns: 1fr 2fr;
}
.head-avatar {
  min-width: 150px;
  min-height: 150px;
  overflow: hidden;
}
.icon-options {
  display: none;
}

.thin {
  font-weight: 100;
}

.head-profile-detail {
  padding-left: 20px;
}

.detail-name {
  padding-top: 20px;
}

.detail-numbers {
  display: none;
}

.detail-info {
  padding-top: 15px;
}

.action-edit {
  border: 1px solid rgb(209, 209, 209);
  padding: 0.3rem;
  border-radius: 3px;
  min-width: 200px;
}

.detail-numbers-mob {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  justify-content: space-evenly;
  border-top: 2px solid rgb(231, 231, 231);
  padding-top: 1rem;
  padding-bottom: 1rem;
}

.detail-numbers-mob .number-1 {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.tabs {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  justify-items: center;
  align-items: center;
  border-top: 2px solid rgb(231, 231, 231);
  padding-top: 1rem;
  padding-bottom: 1rem;
}

.tabs span {
  display: none;
}

@media screen and (min-width: 980px) {
  .home {
    max-width: none;
    display: grid;
    grid-template-rows: 195px 1fr;
    grid-gap: 10px;
  }

  .profile-header {
    padding-right: 10px;
    max-width: none;
    display: grid;
    grid-template-columns: 285px 1fr;
    grid-gap: 10px;
  }

  .tabs {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
    padding-left: 25%;
    padding-right: 25%;
    padding-bottom: 14px;
    padding-top: 14px;
    font-weight: 500;
    font-size: 13px;
    border-top: 2px solid rgb(231, 231, 231);
  }

  .tabs-item-deactive {
    color: #aaa;
  }

  .tabs-item-active {
    color: black;
    border-top: 1px solid black;
    padding-top:15px
  }

  .tab-view {
    display: block;
  }

  .tabs span {
    display: inherit;
  }

  .head-avatar {
    display: inline-flex;
    border-radius: 50%;
    cursor: pointer;
    justify-content: center;
    align-items: center;
    margin-bottom: 25px;
  }

  .head-avatar img {
    border-radius: 50%;
  }

  .thin {
    font-weight: 100;
  }

  .head-profile-detail {
    width: 300px;
    margin-left: 30px;
    margin-bottom: 10px;
  }

  .detail-name {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    padding-right: 40px;
    padding-top: 20px;
    align-items: center;
  }

  .detail-numbers {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;

    padding-top: 20px;
    align-items: center;
  }

  .detail-info {
    padding-top: 15px;
  }

  .action-edit {
    border: 1px solid rgb(209, 209, 209);
    padding: 0.3rem;
    border-radius: 3px;
    margin-left: 20px;
  }
  .detail-numbers-mob {
    display: none;
  }
}
</style>
