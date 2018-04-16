<style scoped>
  @import "comment.less";
</style>
<template>
  <div class="comment">
    <main-menu></main-menu>
    <section class="comment-list">
      <Button type="ghost" shape="circle" icon="ios-search">Search</Button>
      <div class="comment-list-user">
        **
      </div>
      <div class="comment-lsit-content">
        *****
      </div>
    </section>
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
    $('.comment-list').css('width',bigWidth + 'px');
  }
  },
  mounted () {
    this.init();
  }
  }
</script>
