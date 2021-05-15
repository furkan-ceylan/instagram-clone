<template>
<div class="main">
  <div class="direct">
    <div class="sidebar">
      <div class="sidebar-username">
        <CustomText tag="b" size="xlarge">username</CustomText>
      </div>
      <div class="sidebar-users">
        <div class="sidebar-user">
          <div class="user-avatar">
            <img
              src="https://img.pngio.com/profile-icon-png-image-free-download-searchpngcom-profile-icon-png-673_673.png"
              alt="avatar"
              width="60px"
              height="60px"
            />
          </div>
          <div class="user-info">
            <div class="user-name">username</div>
            <div class="user-active">Active 7h ago</div>
          </div>
        </div>
        <div class="sidebar-user">
          <div class="user-avatar">
            <img
              src="https://img.pngio.com/profile-icon-png-image-free-download-searchpngcom-profile-icon-png-673_673.png"
              alt="avatar"
              width="60px"
              height="60px"
            />
          </div>
          <div class="user-info">
            <div class="user-name">username</div>
            <div class="user-active">Active 7h ago</div>
          </div>
        </div>
        <div class="sidebar-user">
          <div class="user-avatar">
            <img
              src="https://img.pngio.com/profile-icon-png-image-free-download-searchpngcom-profile-icon-png-673_673.png"
              alt="avatar"
              width="60px"
              height="60px"
            />
          </div>
          <div class="user-info">
            <div class="user-name">username</div>
            <div class="user-active">Active 7h ago</div>
          </div>
        </div>
        <div class="sidebar-user">
          <div class="user-avatar">
            <img
              src="https://img.pngio.com/profile-icon-png-image-free-download-searchpngcom-profile-icon-png-673_673.png"
              alt="avatar"
              width="60px"
              height="60px"
            />
          </div>
          <div class="user-info">
            <div class="user-name">username</div>
            <div class="user-active">Active 7h ago</div>
          </div>
        </div>
        <div class="sidebar-user">
          <div class="user-avatar">
            <img
              src="https://img.pngio.com/profile-icon-png-image-free-download-searchpngcom-profile-icon-png-673_673.png"
              alt="avatar"
              width="60px"
              height="60px"
            />
          </div>
          <div class="user-info">
            <div class="user-name">username</div>
            <div class="user-active">Active 7h ago</div>
          </div>
        </div>
        <div class="sidebar-user">
          <div class="user-avatar">
            <img
              src="https://img.pngio.com/profile-icon-png-image-free-download-searchpngcom-profile-icon-png-673_673.png"
              alt="avatar"
              width="60px"
              height="60px"
            />
          </div>
          <div class="user-info">
            <div class="user-name">username</div>
            <div class="user-active">Active 7h ago</div>
          </div>
        </div>
        <div class="sidebar-user">
          <div class="user-avatar">
            <img
              src="https://img.pngio.com/profile-icon-png-image-free-download-searchpngcom-profile-icon-png-673_673.png"
              alt="avatar"
              width="60px"
              height="60px"
            />
          </div>
          <div class="user-info">
            <div class="user-name">username</div>
            <div class="user-active">Active 7h ago</div>
          </div>
        </div>
        <div class="sidebar-user">
          <div class="user-avatar">
            <img
              src="https://img.pngio.com/profile-icon-png-image-free-download-searchpngcom-profile-icon-png-673_673.png"
              alt="avatar"
              width="60px"
              height="60px"
            />
          </div>
          <div class="user-info">
            <div class="user-name">username</div>
            <div class="user-active">Active 7h ago</div>
          </div>
        </div>
        <div class="sidebar-user">
          <div class="user-avatar">
            <img
              src="https://img.pngio.com/profile-icon-png-image-free-download-searchpngcom-profile-icon-png-673_673.png"
              alt="avatar"
              width="60px"
              height="60px"
            />
          </div>
          <div class="user-info">
            <div class="user-name">username</div>
            <div class="user-active">Active 7h ago</div>
          </div>
        </div>
      </div>
    </div>
    <div class="messages">
      <div class="messages-icon">
        <img src="../../img/messages.png" alt="" />
      </div>
      <div class="messages-text">
        <CustomText class="thin" size="xlarge">
          Upload a Video
        </CustomText>
        <br />
        <CustomText size="normal">
          Videos must be between 1 and 60 minutes long.
        </CustomText>
      </div>
      <div class="messages-upload">
        <button class="action-edit" type="button">
          <CustomText tag="b" size="normal">Upload</CustomText>
        </button>
      </div>
    </div>
  </div>
  </div>
</template>

<script>
// @ is an alias to /src

import CustomText from "@/components/CustomText";

export default {
  name: "index",
  components: {
    CustomText,
  },
};
</script>

<style scoped>
.main{
  height:75vh;
}
.direct {
  display: grid;
  grid-template-columns: 350px 1fr;
  width: auto;
  height: 530px;
  border: 1px solid lightgrey;
}
.sidebar {
  background-color: white;
  border-right: 1px solid lightgrey;
  display: grid;
  grid-template-rows: 60px 1fr;
  overflow: hidden;
}
.sidebar-username {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 60px;
  margin-left: auto;
  margin-right: auto;
}
.sidebar-users {
  border-top: 1px solid lightgrey;
}

.sidebar-user {
  display: flex;
  flex-direction: row;
  padding-left: 16px;
  cursor: pointer;
  width: auto;
  height: auto;
  background-color: white;
  -webkit-filter: brightness(100%);
}

.sidebar-user:hover {
  -webkit-filter: brightness(98%);
  -webkit-transition: all ease;
  -moz-transition: all ease;
  -o-transition: all ease;
  -ms-transition: all ease;
  transition: all ease;
}
.user-info {
  display: flex;
  flex-direction: column;
  padding-left: 16px;
  justify-content: center;
}

.user-active {
  color: grey;
}

.user-avatar {
  display: inline-flex;
  border-radius: 50%;
}

.messages {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: white;
}

.messages-icon {
  width: 115px;
  height: 115px;
  display: inline-flex;
  justify-content: center;
  align-items: center;
}

.messages-text {
  display: inline-flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.messages-upload {
  width: 100px;
  height: 30px;
  padding-top: 20px;
}

.action-edit {
  background-color: dodgerblue;
  padding: 0.5rem;
  border-radius: 3px;
  color: white;
  width: 100px;
  height: 30px;
}

.thin {
  font-weight: 100;
  font-size: 25px;
}
.sidebar::-webkit-scrollbar {
  width: 5px;
}
 
.sidebar::-webkit-scrollbar-track {
  box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
}
 
.sidebar::-webkit-scrollbar-thumb {
  background-color: darkgrey;
  outline: 1px solid slategrey;
}
</style>
