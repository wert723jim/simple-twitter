<template>
  <div class="create-post-container">
    <div class="avatar-img">
      <div class="user-img"></div>
    </div>
    <div class="text-content">
      <textarea name="" id="" cols="30" rows="10" placeholder="今天想說什麼?"></textarea>
    </div>
    <div class="send-btn">
      <button class="btn">
        推文
      </button>
    </div>
  </div>
</template>

<style scoped>
  .create-post-container {
    display: flex;
    width: 100%;
    /* 讓此component可以根據view內所設定的高度做變化 */
    height: 100%;
    padding: 16px 0 0 26.49px;
    border-bottom: 10px solid #E6ECF0;
  }

  .user-img {
    width: 50px;
    height: 50px;
    border-radius: 50px;
    background: #FF6600;
  }
  
  .text-content {
    flex: 1;
  }

  textarea {
    padding: 8px;
    height: 100%;
    width: 100%;
    resize: none;
    border: none;
    font-weight: 700;
    font-size: 18px;
    line-height: 26px;
    color: #6C757D;
  }

  textarea:focus {
    outline: none;
  }

  .send-btn{
    position: relative;
    width: 84.69px;
  }

  .btn {
    position: absolute;
    right: 24.69px;
    bottom: 16px;
    width: 60px;
    height: 40px;
    border: none;
    border-radius: 50px;
    background: #FF6600;
    color: white;
    cursor: pointer;
  }
</style>