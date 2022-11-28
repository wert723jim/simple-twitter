<template>
  <nav class="nav">
    <img src="../assets/logo.png" alt="" class="brand-logo">
    <div class="nav-tools">
      <div class="nav-list">
        <ul class="list-items">
          <li class="item">
            <a href="#" class="item-link">
              <img src="../assets/home_hollow_2x.png" alt="" class="item-img">
              首頁
            </a>
          </li>
          <li class="item">
            <a href="#" class="item-link">
              <img src="../assets/info_hollow_2x.png" alt="" class="item-img">
              個人資料
            </a>
          </li>
          <li class="item">
            <a href="#" class="item-link">
              <img src="../assets/setting_hollow_2x.png" alt="" class="item-img">
              設定
            </a>
          </li>
        </ul>
      </div>
      <div class="nav-btn">
        <button  class="btn">
          推文
        </button>
      </div>
    </div>
    <div class="item">
      <a href="#" class="item-link">
        <img src="../assets/logout_hollow_2x.png" alt="" class="item-img">
        登出
      </a>
    </div>
  </nav>
</template>

<style scoped>
  .nav {
    display: flex;
    flex-direction: column;
    position: fixed;
    z-index: 999;
    width: 178px;
    height: 100%;
    margin: 0;
    text-align: start;
    background: #FFFFFF;
  }

  .brand-logo {
    width: 40px;
    height: 40px;
    margin: 13px 0 0 13px;
  }

  .nav-tools {
    flex: 1;
  }

  .nav-list {
    margin-bottom: 8px;
  }

  .item {
    padding: 16px;
    font-size: 18px;
  }

  .item-link {
    display: flex;
    align-items: center;
    color: black;
  }

  .item-img {
    width: 24px;
    height: 24px;
    margin-right: 16px;
  }

  .btn {
    width: 100%;
    height: 46px;
    border: none;
    border-radius: 50px;
    background: #FF6600;
    font-size: 20px;
    color: #FFFFFF;
    cursor: pointer;
  }

</style>