<style scoped>
.mask {
  position: fixed;
  z-index: 1;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
}
.loader {
  text-indent: -9999em;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background: #9a9a9a;
  background: linear-gradient(
    to right,
    #9a9a9a 10%,
    rgba(154, 154, 154, 0) 42%
  );
  position: fixed;
  left: 50%;
  top: 50%;
  z-index: 200;
  margin-left: -20px;
  margin-top: -40px;
  animation: load3 1.4s infinite linear;
  transform: translateZ(0);
}
.loader:before {
  width: 50%;
  height: 50%;
  background: #9a9a9a;
  border-radius: 100% 0 0 0;
  position: absolute;
  top: 0;
  left: 0;
  content: '';
}
.loader:after {
  background: #ffffff;
  width: 75%;
  height: 75%;
  border-radius: 50%;
  content: '';
  margin: auto;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}
@-webkit-keyframes load3 {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(360deg);
    transform: rotate(360deg);
  }
}
@keyframes load3 {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(360deg);
    transform: rotate(360deg);
  }
}
</style>

<template>
  <div class="loading">
    <div class="mask"></div>
    <div class="loader">Loading...</div>
  </div>
</template>
