<template>
  <div class="theme-container">
    <div class="theme-vdoing-content">
      <span class="error-code">404</span>
      <p class="error-message">{{ getMsg() }}</p>
      <router-link to="/" class="home-link">返回首页</router-link>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    getMsg () {
      return "哎呀，迷路了呢 (╯°□°）╯︵ ┻━┻";
    }
  }
}
</script>

<style lang="stylus" scoped>
.theme-container
  width 100%
  height 100vh
  display flex
  align-items center
  justify-content center
  background-image linear-gradient(135deg, #17ead9, #6078ea)

.theme-vdoing-content
  max-width 600px
  width 100%
  padding 2rem
  text-align center
  background-color rgba(255, 255, 255, 0.9)
  box-shadow 0 4px 8px rgba(0, 0, 0, 0.1)
  border-radius 10px  // 添加的圆角效果

.error-code
  font-size 8rem
  color $accentColor
  margin-bottom 1rem
  animation bounce 1s ease infinite

.error-message
  font-size 1.5rem
  color $textColor
  margin-bottom 2rem

.home-link
  display inline-block
  padding 0.5rem 1rem
  color #fff
  background-color $accentColor
  border-radius 5px
  text-decoration none
  transition background-color 0.3s

  &:hover
    background-color darken($accentColor, 10%)

@keyframes bounce
  0%, 100%
    transform translateY(0)
  50%
    transform translateY(-20px)

@media (max-width: 768px)
  .error-code
    font-size 5rem
  .theme-vdoing-content
    padding 1rem
</style>
