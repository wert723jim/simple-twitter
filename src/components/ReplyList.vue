<template>
  <div class="replys-container">
    <div class="reply">
      <div class="reply-avatar">
        <div class="user-img"></div>
      </div>
      <div class="reply-wrapper">
        <div class="reply-avatar-info">
          <div class="name">Apple</div>
          <div class="id">@apple</div>
          <span>・</span>
          <div class="created-time">3小時</div>
        </div>
        <div class="reply-to">
          回覆
          <a href="#">@apple</a>
        </div>
        <div class="reply-content">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta
          quisquam, facilis aperiam qui nisi fugit. Earum quidem nobis vel fugit
          molestiae, deleniti facere praesentium natus illum aut iusto quibusdam
          iste! Ad eveniet ex molestias nemo! Necessitatibus, laboriosam
          nesciunt? Nesciunt doloribus quaerat a quia molestiae reiciendis ipsa
          ullam officia dolores ea? Eligendi, dolores blanditiis dicta
          aspernatur et eum. Recusandae, nostrum omnis?
        </div>
      </div>
    </div>

    <div class="reply">
      <div class="reply-avatar">
        <div class="user-img"></div>
      </div>
      <div class="reply-wrapper">
        <div class="reply-avatar-info">
          <div class="name">Apple</div>
          <div class="id">@apple</div>
          <span>・</span>
          <div class="created-time">3小時</div>
        </div>
        <div class="reply-to">
          回覆
          <a href="#">@apple</a>
        </div>
        <div class="reply-content">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta
          quisquam, facilis aperiam qui nisi fugit. Earum quidem nobis vel fugit
          molestiae, deleniti facere praesentium natus illum aut iusto quibusdam
          iste! Ad eveniet ex molestias nemo! Necessitatibus, laboriosam
          nesciunt? Nesciunt doloribus quaerat a quia molestiae reiciendis ipsa
          ullam officia dolores ea? Eligendi, dolores blanditiis dicta
          aspernatur et eum. Recusandae, nostrum omnis?
        </div>
      </div>
    </div>

    <div class="reply">
      <div class="reply-avatar">
        <div class="user-img"></div>
      </div>
      <div class="reply-wrapper">
        <div class="reply-avatar-info">
          <div class="name">Apple</div>
          <div class="id">@apple</div>
          <span>・</span>
          <div class="created-time">3小時</div>
        </div>
        <div class="reply-to">
          回覆
          <a href="#">@apple</a>
        </div>
        <div class="reply-content">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta
          quisquam, facilis aperiam qui nisi fugit. Earum quidem nobis vel fugit
          molestiae, deleniti facere praesentium natus illum aut iusto quibusdam
          iste! Ad eveniet ex molestias nemo! Necessitatibus, laboriosam
          nesciunt? Nesciunt doloribus quaerat a quia molestiae reiciendis ipsa
          ullam officia dolores ea? Eligendi, dolores blanditiis dicta
          aspernatur et eum. Recusandae, nostrum omnis?
        </div>
      </div>
    </div>

    <div class="reply">
      <div class="reply-avatar">
        <div class="user-img"></div>
      </div>
      <div class="reply-wrapper">
        <div class="reply-avatar-info">
          <div class="name">Apple</div>
          <div class="id">@apple</div>
          <span>・</span>
          <div class="created-time">3小時</div>
        </div>
        <div class="reply-to">
          回覆
          <a href="#">@apple</a>
        </div>
        <div class="reply-content">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta
          quisquam, facilis aperiam qui nisi fugit. Earum quidem nobis vel fugit
          molestiae, deleniti facere praesentium natus illum aut iusto quibusdam
          iste! Ad eveniet ex molestias nemo! Necessitatibus, laboriosam
          nesciunt? Nesciunt doloribus quaerat a quia molestiae reiciendis ipsa
          ullam officia dolores ea? Eligendi, dolores blanditiis dicta
          aspernatur et eum. Recusandae, nostrum omnis?
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.replys-container {
  height: 100%;
}

.reply {
  display: flex;
  padding: 16px 24px;
  border-bottom: 1px solid #e6ecf0;
}

.user-img {
  width: 50px;
  height: 50px;
  margin-right: 8px;
  border-radius: 50px;
  background: gray;
}

.reply-avatar-info {
  display: flex;
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
  color: #6c757d;
}

.reply-to {
  text-align: left;
  margin-bottom: 8px;
  font-size: 14px;
  color: #657786;
}

.reply-to a {
  color: #ff6600;
}

.reply-content {
  margin-bottom: 9px;
  text-align: left;
  font-weight: 400;
  font-size: 16px;
  line-height: 26px;
  color: #171725;
}
</style>