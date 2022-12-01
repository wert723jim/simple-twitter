<template>
  <div class="tab-container">
    <div class="tab">
      <a href="#" class="tab-link active">
        推文
      </a>
    </div>
    <div class="tab">
      <a href="#" class="tab-link">
        回覆
      </a>
    </div>
    <div class="tab">
      <a href="#" class="tab-link">
        喜歡的內容
      </a>
    </div>
  </div>
</template>

<style scoped>
  .tab-container {
    display: flex;
  }

  .tab {
    display: flex;
    width: 130px;
    height: 50px
  }

  .tab-link {
    width: 100%;
    height: 100%;
    line-height: 48px;
    color: #657786;
    font-size: 15px;
  }
  
  .tab-link.active {
    color: #FF6600;
    border-bottom: 2px solid #FF6600;
  }
</style>