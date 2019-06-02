<template>
  <div>
    <app-navigation />
    <nuxt/>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  computed: mapState(['page'])
}
</script>

<style scoped lang="scss">
ul {
  list-style: none;
  li {
    display: inline-block;
    margin-right: 10px;
  }
  a,
  a:active,
  a:visited {
    color: white;
    text-decoration: none;
  }
}
.nuxt-link-active {
  font-weight: bold;
}
.items,
.list-move {
  transition: all 0.4s ease;
}
.list-leave-active {
  position: absolute;
}
#text {
  transform-origin: 50% 50%;
}
svg {
  fill: #a8dadc;
}
.active {
  fill: #e63946;
  .rect {
    transform: translate3d(0, 30px, 0);
  }
  .circ {
    transform: translate3d(30px, 0, 0) scale(0.5);
  }
  .text {
    transform: rotate(90deg) scaleX(0.08) translate3d(-300px, -35px, 0);
  }
  .footer {
    transform: translate3d(100px, 0, 0);
  }
}
</style>