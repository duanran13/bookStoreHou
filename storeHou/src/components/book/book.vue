<style scoped>
  @import "book.less";
  @import "../styles/common.less";
</style>
<template>
  <div class="book">
    <main-menu></main-menu>
    <div class="book-sort">
      <Row :style="{height: '100%'}">
        <Col span="7" :style="{height: '100%'}">
        <div>
          <img src="" alt=""/>
        </div>
        </Col>
        <Col span="10" :style="{height: '100%'}">
        <div class="book-sort-list">
          <p class="book-list-name">书名</p>
          <p>作者名</p>
        </div>
        </Col>
        <Col span="7" :style="{height: '100%'}">
        <div class="book-list-action">
          <InputNumber :max="10" :min="1" v-model="value1"></InputNumber>
          <Button type="success">Success</Button>
          <Button type="error">Error</Button>
        </div>
        </Col>
      </Row>

    </div>
  </div>
</template>
<script>
  import mainMenu from '../main.vue'
  export default {
    data () {
      return {
        value1: 1
      }
    },
  components: {
    'mainMenu': mainMenu
  },
  methods:{
    init(){
      let bigWidth = $(window).width()-200;
      $('.book-sort').css('width',bigWidth + 'px');
    }
  },
  mounted () {
    this.init();
  }
  }
</script>
