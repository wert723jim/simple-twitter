<template>
  <div class="tab-container">
    <div class="tab-item">
      <router-link
        :to="{name: 'user-followers', params: {id: 1}}" 
        class="tab-link"
      >
        追隨者
      </router-link>
    </div>
    <div class="tab-item">
      <router-link
        :to="{name: 'user-followings', params: {id: 1}}"
        class="tab-link"
      >
        追隨中
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  
}
</script>

<style scoped>
  .tab-container {
    display: flex;
    border-bottom: 1px solid #E6ECF0;
  }

  .tab-item {
    display: flex;
    height: 52px;
    width: 130px;
  }

  .tab-link {
    width: 100%;
    height: 100%;
    line-height: 50px;
    color: #657786;
  }

  .active {
    border-bottom: 2px solid #FF6600;
    color: #FF6600;
  }
</style>