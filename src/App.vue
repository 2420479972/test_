<script lang="ts" setup>


const _click = () => {
  if (window.webkit && window.webkit.messageHandlers && window.webkit.messageHandlers.nativeHandler) {
    window.webkit.messageHandlers.nativeHandler.postMessage("loginSuccess")
  } //登陆成功后调用 就是在获取到token之后调用
}

const _2click = ()=>{
  if (window.webkit && window.webkit.messageHandlers && window.webkit.messageHandlers.nativeHandler) {
    window.webkit.messageHandlers.nativeHandler.postMessage("loginoutSuccess")
  }//退出登陆后调用
}

</script>

<template>
  <button @click="_click">loginSuccess</button>
  <button @click="_2click">loginoutSuccess</button>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
