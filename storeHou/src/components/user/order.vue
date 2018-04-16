<template>
  <div class="order">
    <main-menu></main-menu>
    <div class="order-list">
      dingdan
    </div>
  </div>
</template>
<script>
  import mainMenu from '../main.vue'
  export default {
    components: {
      'mainMenu': mainMenu
    },
    methods:{
      init(){
        let bigWidth = $(window).width()-200;
        $('.user-table').css('width',bigWidth + 'px');
      }
    },
    mounted () {
      this.init();
    }
  }
</script>
