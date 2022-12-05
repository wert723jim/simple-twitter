<template>
  <div 
    class="modal-container"
    :class="['modal-container', {show: isShow}]"
  >
    <div class="modal-content">
      <div
        class="modal-header"
        @click="closeModal"
      >
        <img src="../assets/close_btn.png" alt="" class="close-btn">
      </div>
      <div class="modal-body">
        <div class="avatar-img">
          <div class="user-img"></div>
        </div>
        <div class="text-content">
          <textarea name="" id="" cols="30" rows="5" placeholder="今天想說什麼?"></textarea>
        </div>
      </div>
      <div class="modal-footer">
        <button class="btn">
          推文
        </button>
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
      isShow: this.showModal
    }
  },
  methods: {
    closeModal() {
      this.isShow = false
      this.$emit("close-modal", false)
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
    height: 300px;
    background: #FFFFFF;
    border-radius: 14px;
  }

  .modal-header {
    padding: 16px 15px;
    text-align: left;
    border-bottom: 1px solid #E6ECF0;
  }

  .close-btn {
    cursor: pointer;
  }

  .modal-body {
    display: flex;
    padding: 16px 24px;
  }

  .user-img {
    width: 50px;
    height: 50px;
    border-radius: 50px;
    background: #FF6600;
  }
  
  .text-content {
    text-align: left;
    width: 100%;

  }

  textarea {
    padding: 8px;
    resize: none;
    border: none;
    width: 100%;
    font-weight: 700;
    font-size: 16px;
    line-height: 26px;
    color: #6C757D;
  }

  textarea:focus {
    outline: none;
  }

  .modal-footer {
    text-align: right;
    padding-right: 16px;
  }

  .btn {
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