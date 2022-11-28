<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;500;700&family=Noto+Sans+TC:wght@300;500;700&display=swap');
#app {
  font-family: 'Noto Sans TC', 'Montserrat', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  height: 100%;
  width: 80%;
  margin: 0 auto;
}

*,
*::before,
*::after {
  box-sizing: border-box;
}
html,
body {
  /* width: 100%; */
  height: 100%;
  margin: 0;
}

h1,
h2,
h3,
h4,
h5 {
  margin: 0;
  line-height: 0.9;
}

p {
  margin: 0;
}

ul,
li {
  list-style-type: none; /* 拿掉前方圈圈 */
  margin: 0;
  padding: 0;
}

a {
  text-decoration: none; /* 拿掉底線 */
}

h1 {
  font-weight: bold;
  font-size: 68px;
}

h2 {
  font-weight: bold;
  font-size: 42px;
}

h3 {
  font-weight: 500;
  font-size: 28px;
}

h4 {
  font-weight: medium;
  font-size: 24px;
}

h5 {
  font-weight: medium;
  font-size: 18px;
}
</style>
