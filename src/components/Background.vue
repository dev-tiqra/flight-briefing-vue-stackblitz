<template>
  <div class="clouds text-white absolute top-0 bottom-0 left-0 right-0">
    <div class="cloud" v-for="cloud in 5" :key="cloud" :class="`x${cloud}`"></div>
  </div>
</template>

<style scoped lang="css">
.clouds {
  padding: 100px 0;
  background: #c9dbe9;
  background: linear-gradient(to bottom, #c9dbe9 0%, #fff 100%);
  background: -linear-gradient(to bottom, #c9dbe9 0%, #fff 100%);
  background: -moz-linear-gradient(top, #c9dbe9 0%, #fff 100%);
  z-index: -1;
}

@media (max-width: 640px) {
  .clouds {
    display: none;
  }
}

.dark .clouds {
  background: linear-gradient(to bottom, #0f1629 0%, #3d4a70 100%);
  background: -linear-gradient(to bottom, #0f1629 0%, #3d4a70 100%);
  background: -moz-linear-gradient(top, #0f1629 0%, #3d4a70 100%);
}

.cloud {
  width: 200px;
  height: 60px;
  background: #fff;
  border-radius: 200px;
  position: relative;
}

.cloud:before,
.cloud:after {
  content: '';
  position: absolute;
  background: #fff;
  width: 100px;
  height: 80px;
  position: absolute;
  top: -15px;
  left: 10px;
  border-radius: 100px;
  transform: rotate(30deg);
}

.cloud:after {
  width: 120px;
  height: 120px;
  top: -55px;
  left: auto;
  right: 15px;
}

.x1 {
  animation: moveclouds 15s linear infinite;
}

.x2 {
  left: 200px;
  transform: scale(0.6);
  opacity: 0.6;
  animation: moveclouds 25s linear infinite;
}

.x3 {
  left: -250px;
  top: -200px;
  transform: scale(0.8);
  opacity: 0.8;
  animation: moveclouds 20s linear infinite;
}

.x4 {
  left: 470px;
  top: -250px;
  transform: scale(0.75);
  opacity: 0.75;
  animation: moveclouds 18s linear infinite;
}

.x5 {
  left: -150px;
  top: -150px;
  transform: scale(0.8);
  opacity: 0.8;
  animation: moveclouds 20s linear infinite;
}

@keyframes moveclouds {
  0% {
    margin-left: 1200px;
  }
  100% {
    margin-left: -1000px;
  }
}
</style>
