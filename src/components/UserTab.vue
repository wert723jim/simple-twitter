<template>
  <div class="tab-container">
    <div class="tab">
      <a 
        href="#" 
        :class="['tab-link', {active: tab_link === 'tweets'}]"
        @click.stop.prevent="chosenTab('tweets')"
      >
        推文
      </a>
    </div>
    <div class="tab">
      <a 
        href="#" 
        :class="['tab-link', {active: tab_link === 'replies'}]"
        @click.stop.prevent="chosenTab('replies')"
      >
        回覆
      </a>
    </div>
    <div class="tab">
      <a 
        href="#" 
        :class="['tab-link', {active: tab_link === 'likes'}]"
        @click.stop.prevent="chosenTab('likes')"
      >
        喜歡的內容
      </a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tab_link: 'tweets'
    }
  },
  methods: {
    chosenTab(tabName) {
      this.tab_link = tabName
      this.$emit("chosen-tab", tabName)
    }
  }
}
</script>

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