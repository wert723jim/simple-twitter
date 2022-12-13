<template>
  <div class="form-container">
    <form action="">
      <div class="form-label-group">
        <label for="account">
          帳號
        </label>
        <input
          type="text"
          placeholder="請輸入帳號"
          id="account"
        >
      </div>

      <div class="form-label-group">
        <label for="name">
          名稱
        </label>
        <input 
          type="text" 
          placeholder="請輸入使用者名稱"
          id="name"
        >
      </div>

      <div class="form-label-group">
        <label for="email">
          Email
        </label>
        <input 
          type="text" 
          placeholder="請輸入Email"
          id="email"
        >
      </div>

      <div class="form-label-group">
        <label for="password">
          密碼
        </label>
        <input 
          type="password" 
          placeholder="請輸入密碼"
          id="password"
        >
      </div>

      <div class="form-label-group">
        <label for="password-confirm">
          密碼確認
        </label>
        <input 
          type="password" 
          placeholder="請再次輸入密碼"
          id="password-confirm"
        >
      </div>

      <div class="button-wrapper">
        <button
          type="submit"
          class="save-btn btn show"
        >
          儲存
        </button>

        <button
          type="submit"
          class="regist-btn btn"
        >
          註冊
        </button>
      </div>      
    </form>

    <div class="tunel">
      <router-link to="$router.back()">取消</router-link>
    </div>
  </div>
    

</template>

<style scoped>
  .container {
    width: 356px;
    margin: 0 auto;
    margin-top: 69px;
  }

  .brand-logo {
    width: 40px;
    height: 40px;
    margin-bottom: 29px;
  }

  .form-title {
    margin-bottom: 40px;
  }

  .form-label-group {
    display: flex;
    flex-direction: column;
    justify-content: start;
    margin-bottom: 32px;
    padding: 2px 10.55px;
    border-bottom: 2px solid #657786;
    border-radius: 2px;
    width: 100%;
    height: 54px;
    background: #F5F8FA;
  }
  
  .form-label-group > label {
    text-align: start;
    font-size: 14px;
    color: #696974
  }

  .form-label-group > input {
    border: none;
    outline: none;
    height: 26px;
    font-size: 16px;
    background: transparent;
  }

  .button-wrapper {
    text-align: right;
  }

  .btn {
    cursor: pointer;
  }

  .regist-btn {
    display: none;
    margin-top: 8px;
    width: 100%;
    height: 46px;
    border-radius: 50px;
    border: none;
    background: #FF6600;
    color: #FFFFFF;
    font-size: 20px;
  }

  .save-btn {
    display: none;
    height: 46px;
    width: 88px;
    border-radius: 50px;
    border: none;
    background: #FF6600;
    color: #FFFFFF;
  }

  .show {
    display: inline;
  }

  .tunel {
    display: none;
    margin-top: 22px;
    text-align: center;
  }

  .tunel a {
    text-decoration: underline;
  }

  .tunel span {
    margin: 0 12px;
  }
</style>