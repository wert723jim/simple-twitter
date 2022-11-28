<template>
  <div class="recommended-wrapper">
    <div class="recommended-title">
      <h4>推薦跟隨</h4>
    </div>
    <div class="recommended-list">
      <ul class="list-items">
        <li class="item">
          <div class="item-img">
            <div class="user-img"></div>
          </div>
          <div class="item-name">
            <div class="user-name">
              Pizza Hut
            </div>
            <div class="user-id">
              @pizzahut
            </div>
          </div>
          <div class="item-followed-btn">
            <button class="unfollowed-btn btn">
              正在跟隨
            </button>
            <button class="followed-btn btn">
              跟隨
            </button>
          </div>
        </li>

        <li class="item">
          <div class="item-img">
            <div class="user-img"></div>
          </div>
          <div class="item-name">
            <div class="user-name">
              Pizza Hut
            </div>
            <div class="user-id">
              @pizzahut
            </div>
          </div>
          <div class="item-followed-btn">
            <button class="unfollowed-btn btn">
              正在跟隨
            </button>
            <button class="followed-btn btn">
              跟隨
            </button>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
  .recommended-wrapper {
    width: 273px;
    height: 731px;
    background: #FAFAFB;
  }

  .recommended-title {
    padding: 24px;
    text-align: start;
    border-bottom: 1px solid #E6ECF0;
  }

  .list-items {
    padding: 16px;
  }

  .item {
    display: flex;
    margin-bottom: 32px;
  }

  .user-img {
    margin-right: 8px;
    width: 50px;
    height: 50px;
    background: orange;
    border-radius: 50px;
  }

  .item-name {
    text-align: left;
    /* 佔滿剩餘位置 */
    flex: 1;
    /* margin-right: 13px; */
  }

  .user-name {
    line-height: 22px;
  }

  .user-id {
    font-size: 14px;
    line-height: 22px;
    color: #92929D;
  }

  .item-followed-btn {
    text-align: end;
    line-height: 50px;
  }

  .btn {
    cursor: pointer;
  }

  .followed-btn {
    width: 64px;
    height:40px;
    border: 1px solid #FF6600;
    border-radius: 50px;
    color: #FF6600;
  }

  .unfollowed-btn {
    display: none;
    width: 96px;
    height: 40px;
    border: none;
    border-radius: 50px;
    background: #FF6600;
    color: #FFFFFF;
  }
</style>