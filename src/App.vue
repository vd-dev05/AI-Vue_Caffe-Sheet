<template>
  <div>
    <router-view v-slot="{ Component }">
      <transition name="page" mode="out-in">
        <component :is="Component" />
      </transition>
    </router-view>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

.router-link-active {
  color: #d97706 !important;
  font-weight: 600;
}

.router-link-exact-active {
  color: #d97706 !important;
  font-weight: 600;
}

/* Hiệu ứng chuyển trang */
.page-enter-active,
.page-leave-active {
  transition: opacity 0.3s, transform 0.3s;
}

.page-enter-from {
  opacity: 0;
  transform: translateY(20px);
}

.page-leave-to {
  opacity: 0;
  transform: translateY(-20px);
}

/* Thêm animation mặc định */
@keyframes float {
  0% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-10px);
  }
  100% {
    transform: translateY(0px);
  }
}

.animate-float {
  animation: float 3s ease-in-out infinite;
}

/* Hiệu ứng hover chung */
.hover-grow {
  transition: all 0.3s ease;
}

.hover-grow:hover {
  transform: scale(1.05);
}

/* Hiệu ứng button */
button {
  position: relative;
  overflow: hidden;
}

button::after {
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  width: 5px;
  height: 5px;
  background: rgba(255, 255, 255, 0.5);
  opacity: 0;
  border-radius: 100%;
  transform: scale(1, 1) translate(-50%);
  transform-origin: 50% 50%;
}

@keyframes ripple {
  0% {
    transform: scale(0, 0);
    opacity: 0.5;
  }
  100% {
    transform: scale(30, 30);
    opacity: 0;
  }
}

button:focus:not(:active)::after {
  animation: ripple 1s ease-out;
}
</style>
