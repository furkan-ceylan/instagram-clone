<template>
  <div class="post">
    <!-- header -->
    <div class="head section">
      <div class="head-author">
        <div class="head-avatar">
          <img
            src="https://img.pngio.com/profile-icon-png-image-free-download-searchpngcom-profile-icon-png-673_673.png"
            alt="avatar"
            width="40px"
            height="40px"
          />
        </div>

        <div class="head-author-info">
          <div>
            <CustomText tag="b">username</CustomText>
          </div>
          <div>
            <CustomText size="xsmall">Montreal, Quebec</CustomText>
          </div>
        </div>
      </div>
      <div class="head-more">
        <button type="button">
          <IconMore />
        </button>
      </div>
    </div>

    <!-- media -->
    <div class="post-media">
      <img
        src="https://images.theconversation.com/files/296052/original/file-20191008-128681-ngzwqb.jpg?ixlib=rb-1.1.0&q=45&auto=format&w=1200&h=900.0&fit=crop"
        alt=""
      />
    </div>

    <!-- actions -->
    <div class="action-buttons section">
      <button type="button">
        <IconLike />
      </button>
      <button type="button">
        <IconComment />
      </button>
      <button type="button">
        <IconDirect />
      </button>
      <button class="action-save" type="button">
        <IconSave />
      </button>
    </div>

    <!-- view count -->

    <div class="view-count section">
      <custom-text tag="b">1.345 beğenme</custom-text>
    </div>

    <!-- comment list -->
    <div class="view-comment section">
      <custom-text tag="b">Richard Harlow</custom-text>
      blind eye works
    </div>
    <!-- datetime -->
    <div class="view-datetime section">
      <div class="view-datetime text">
        <CustomText tag="b" size="xsmall">2 HOURS AGO</CustomText>
      </div>
    </div>
    <!-- comment form -->
    <div class="comment-form section">
      <button type="button">
        <Emoji />
      </button>
      <form class="comment-form commentline">
        <input type="Text" placeholder="Add a comment..."/>
      </form>
      <button class="action-share" type="button">
        <CustomText tag="b" size="large">Paylaş</CustomText>
      </button>
    </div>

  </div>
  
</template>

<script>
import Avatar from "@/components/Avatar";
import CustomText from "@/components/CustomText";
import IconMore from "@/icons/more.svg";
import IconLike from "@/icons/like.svg";
import IconComment from "@/icons/comment.svg";
import IconDirect from "@/icons/direct.svg";
import IconSave from "@/icons/save.svg";
import Emoji from "@/icons/emoji.svg";

export default {
  name: "Post",
  components: {
    IconLike,
    IconComment,
    IconDirect,
    IconSave,
    IconMore,
    CustomText,
    Avatar,
    Emoji
  },
  data: function () {
    return {
      notPost: false,
    };
  },
};
</script>

<style scoped>
.post {
  border-radius: 3px;
  border: 1px solid rgb(209, 209, 209);
  background-color: white;
  margin-bottom: 62px;
}

.section {
  padding-left: 16px;
  
}

.text {
  color:gray;
}

.head {
  height: 60px;
  display: flex;
  align-items: center;
}

.head-avatar {
  display: inline-flex;
  border-radius: 50%;
  background: linear-gradient(
    219deg,
    rgba(184, 63, 140, 1) 0%,
    rgba(237, 158, 90, 1) 100%
  );
}

.head-avatar img {
  border-radius: 50%;
}

.head-author {
  display: flex;
  align-items: center;
}

.head-author-info {
  margin-left: 8px;
}

.head-more {
  margin-left: auto;
  padding-right: 16px;
}

.action-buttons {
  height: 45px;
  display: flex;
  align-items: center;
}

.action-buttons button {
  margin-right: 16px;
}

.action-save {
  margin-left: auto;
  margin-right: 0;
}

.action-share {
  margin-left: auto;
  margin-right: 0;
  color:#0095f6;
  padding-right: 16px;
}

.post-media {
  min-width: 100px;
  min-height: 100px;
  background-color: rgb(245, 245, 245);
}

.view-comment {
  padding-top: 8px;
}

.comment-form {
  border-top:1px solid rgb(209, 209, 209);
  height: 50px;
  display: flex;
  align-items: center;
  margin-top: 16px;
  overflow:hidden
}

.commentline {
  padding-left: 16px;
  font-weight: 600;
  padding-bottom: 16px;
}

.commentline input {
  width: 540px; 
}

@media screen and (min-width: 980px) {
  .action-share {
  margin-left: auto;
  margin-right: 0;
  color:#0095f6;
  padding-right: 16px;
}

.comment-form {
  border-top:1px solid rgb(209, 209, 209);
  height: 50px;
  display: flex;
  align-items: center;
  margin-top: 16px;
}
}

</style>
