<template>
  <div 
    :class="['modal-container', {show: isShow}]"
  >
    <div class="modal-content">
      <div
        class="modal-header"
      >
        <img 
          src="../assets/close_btn.png"
          alt=""
          class="close-btn"
          @click="closeModal"
        >
        <button
          class="save-btn btn"
        >
          儲存
        </button>
      </div>
      <div class="modal-body">
        <div class="user-img">
          <div class="user-background">
            <img src="../assets/user_background.png" alt="" class="user-background-img">
            <div class="hover-setting">
              <div class="btn-wrapper">
                <img src="../assets/camera.png" alt="" class="background-camera-btn btn">
                <img src="../assets/white_close_btn.png" alt="" class="background-close-btn btn">
              </div>
            </div>
          </div>
          <div class="user-head-shot">
            <div class="user-head-shot-img"></div>
            <div class="hover-setting">
              <div class="btn-wrapper">
                <img src="../assets/camera.png" alt="" class="btn">
              </div>
            </div>
          </div>
        </div>
        <div class="user-info">
          <div class="user-info-name column-wrapper">
            <label for="user-name">名稱</label>
            <input
              type="text"
              id="user-name"
              v-model="userName"
              @input="nameCounts"
            >
          </div>
          <div class="name-counts counts">
            {{userName.length}}/{{userNameMaxLength}}
          </div>
          <div class="user-info-intro column-wrapper">
            <label for="user-intro">自我介紹</label>
            <textarea  
              cols="30" 
              rows="7"
              id="user-intro"
              v-model="userIntro"
              @input="introCounts"
            >
            </textarea>
          </div>
          <div class="intro-counts counts">
            {{userIntro.length}}/{{userIntroMaxLength}}
          </div>
        </div>
      </div>
      <div class="modal-background">
      </div>
    </div>
    
  </div>
</template>

<script>
export default {
  props: {
    showModal: {
      type: Boolean,
      default: false
    }
  },
  watch: {
    showModal(newValue) {
      this.isShow = newValue
    }
  },
  data() {
    return {
      isShow: this.showModal,
      userName: '',
      userIntro: '',
      userNameMaxLength: 10,
      userIntroMaxLength: 160
    }
  },
  methods: {
    closeModal() {
      this.isShow = false
      this.$emit("close-modal", false)
    },
    nameCounts() {
      if(this.userName.length >= 10) {
        this.userName = this.userName.substring(0, this.userNameMaxLength)
      }
    },
    introCounts() {
      if(this.userIntro.length >= 160) {
        this.userIntro = this.userIntro.substring(0, this.userIntroMaxLength)
      }
    }
  }
}
</script>

<style scoped>
  .modal-container {
    /* 預設為不顯示 */
    display: none;
    position: absolute;
    left: 0;
    top: 0;
    height: 100%;
    width: 100%;
    padding-top: 56px;
    z-index: 1055;
  }

  .modal-container.show {
    display: block;
  }

  .modal-content {
    z-index: 1;
    margin: 0 auto;
    width: 634px;
    background: #FFFFFF;
    border-radius: 14px;
  }

  .modal-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    text-align: left;
    padding: 0 16px;
    height: 57px;
    border-bottom: 1px solid #E6ECF0;
  }

  .close-btn {
    width: 24px;
    height: 24px;
    cursor: pointer;
  }

  .save-btn {
    width:64px;
    height: 40px;
    background: #FF6600;
    border-radius: 50px;
    border: none;
    color: #FFFFFF;
  }

  .modal-body {
    display: flex;
    flex-direction: column;
  }

  .user-img {
    width: 100%;
  }
  /* user-head-shot 的基準點 */
  .user-img {
    position: relative;
  }
/* .hover-setting 的基準點 */
  .user-background {
    position: relative;
  }

  .user-background-img {
    display: block;
    width: 100%;
    height: 100%;
  }

  .hover-setting {
    display: none;
    align-items: center;
    justify-content: center;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(23, 23, 37, .5)
  }

  .user-background:hover .hover-setting{
    display: flex;
  }

  .background-camera-btn {
    margin-right: 36px;
  }

  .btn {
    cursor: pointer;
  }

  .user-head-shot {
    position: absolute;
    bottom: -70px;
    left: 16px;
    width: 140px;
    height: 140px;
    border: 4px solid #FFFFFF;
    border-radius: 140px;
  }

  .user-head-shot-img {
    width: 100%;
    height: 100%;
    border-radius: 100%;
    background: #FF6600;
  }

  .user-head-shot:hover .hover-setting {
    display: flex;
    border-radius: 100%;
  }

  .user-info {
    margin-top: 80px;
    text-align: left;
    padding: 0 16px 16px 16px;
  }

  .user-info-intro {
    height: 147px;
  }

  .user-info-intro textarea {
    border: none;
    outline: none;
    resize: none;
    width: 100%;
    background: transparent;
  }

  .column-wrapper {
    margin-bottom: 4px;
    padding: 2px 18px;
    border-bottom: 2px solid #657786;
    border-radius: 2px;
    background: #F5F8FA;
  }

  .column-wrapper label {
    display: block;
    color: #696974;
    font-size: 14px;
  }

  .column-wrapper input {
    width: 100%;
    outline: none;
    border: none;
    background: transparent;
  }

  .counts {
    margin-bottom: 8px;
    text-align: right;
    color: #696974;
    font-size: 12px;
  }

  .modal-footer {
    text-align: right;
    padding-right: 16px;
  }

  .modal-background {
    z-index: -1;
    position:absolute;
    left: 0;
    top: 0;
    height: 100%;
    width: 100%;
    background: #171725;
    opacity: .4
  }
</style>