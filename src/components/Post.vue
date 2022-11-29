<template>
  <div class="post-container">
    <div class="post-avatar">
      <div class="user-img"></div>
      <div class="post-avatar-info">
        <div class="name">Apple</div>
        <div class="id">@apple</div>
      </div>
    </div>
    <div class="post-wrapper">
      <div class="post-content">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta
        quisquam, facilis aperiam qui nisi fugit. Earum quidem nobis vel fugit
        molestiae, deleniti facere praesentium natus illum aut iusto quibusdam
        iste! Ad eveniet ex molestias nemo! Necessitatibus, laboriosam
        nesciunt? Nesciunt doloribus quaerat a quia molestiae reiciendis ipsa
        ullam officia dolores ea? Eligendi, dolores blanditiis dicta
        aspernatur et eum. Recusandae, nostrum omnis?
      </div>
      <div class="created-time">
        上午 10:05・2021年11月10日
      </div>
    </div>
    <div class="post-counts">
      <div class="post-counts-reply">
        <span class="count">34</span>
        回覆
      </div>
      <div class="post-counts-likes">
        <span class="count">808</span>
        喜歡次數
      </div>
    </div>
    <div class="post-icons">
      <div class="post-icons-comments">
        <img src="../assets/icon_reply_big.png" alt="" class="icon"/>
      </div>
      <div class="post-icons-likes">
        <img src="../assets/icon_like_big.png" alt="" class="icon"/>
      </div>
    </div>
  </div>
</template>

<style scoped>
.post-container {
  padding: 16px 24px;
  border-bottom: 1px solid  #E6ECF0;
}

.post-wrapper {
  border-bottom: 1px solid #E6ECF0;
}

.post-avatar {
  display: flex;
}

.user-img {
  width: 50px;
  height: 50px;
  margin-right: 8px;
  border-radius: 50px;
  background: gray;
}

.post-avatar-info {
  text-align: left;
  margin-bottom: 8px;
}

.name {
  margin-right: 8px;
}

.id,
.id ~ span,
.created-time {
  font-weight: 400;
  font-size: 14px;
  line-height: 22px;
  color: #6C757D;
}

.post-content {
  margin-bottom: 9px;
  text-align: left;
  font-weight: 400;
  font-size: 16px;
  line-height: 26px;
  color: #171725;
}

.created-time {
  text-align: left;
  margin-bottom: 8px;
}

.post-counts {
  display: flex;
  padding: 16px 0;
  border-bottom: 1px solid #E6ECF0;
  color: #6C757D;
}

.post-counts-reply {
  margin-right: 24px;
}

.count {
  color: #171725;
}

.post-icons {
  display: flex;
  margin-top: 19px;
}

.post-icons-comments {
  margin-right: 130px;
}
</style>