<template>
    <footer class="fixed-bottom clearfix">
        <div class="col4">
          <router-link to="/index">index</router-link>
        </div>
        <div class="col4">
          <router-link to="/news">news</router-link>
        </div>
        <div class="col4">
          <router-link to="/second">menu3</router-link>
        </div>
        <div class="col4">
          <router-link to="/third">menu4</router-link>
        </div>
    </footer>
</template>
<script>
    export default{
        data(){
            return{
                msg: 'Hello vue'
            }
        }
    }
</script>
<style lang="less">
   @import "footer.less";
</style>
