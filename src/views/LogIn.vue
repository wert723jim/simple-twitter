<template>
  <div class="container">
    <img src="../assets/logo.png" alt="" class="brand-logo">
    <form action="">
      <div class="form-title">
        <h3>登入 Alphitter</h3>
      </div>
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
        <label for="password">
          密碼
        </label>
        <input 
          type="password" 
          placeholder="請輸入密碼"
          id="password"
        >
      </div>

      <button
        type="submit"
        class="btn"
      >
        登入
      </button>
    </form>

    <div class="tunel">
      <a href="#">註冊</a>
      <span>・</span>
      <a href="#">後台登入</a>
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

  .btn {
    margin-top: 8px;
    width: 100%;
    height: 46px;
    border-radius: 50px;
    border: none;
    background: #FF6600;
    color: #FFFFFF;
    font-size: 20px;
  }

  .btn:hover {
    cursor: pointer;
  }

  .tunel {
    margin-top: 22px;
    text-align: end;
  }

  .tunel a {
    text-decoration: underline;
  }

  .tunel span {
    margin: 0 12px;
  }
</style>