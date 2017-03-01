<template>
    <div>
        <h4 class="news-tit">啥玩意儿?？{{$route.params.appId || 'empty'}}</h4>
        <h3>{{msg}}</h3>
    </div>
</template>

<script type="text/ecmascript-6">
    import axios from 'axios'

    export default {

        data(){
            return{
                msg:'这个页面包含了使用axios去请求ajax数据和其他事件方法'
            }
        },

        created() {
            console.log('created!!!')
            console.log(this.$route.params.appId)
            console.log(this.msg)


            axios.get('http://localhost:12306/api/marketable-products/ZYZG/22400')
                    .then(function(response) {
                        console.log('response')
                        this.msg=response.timestamp
                    })
                    .catch(function(error) {
                        console.log('error')
                        console.log(response)
                        this.msg=response.timestamp
                    });
        }
    }

</script>
<style>
    .news-tit {
        font-size: 18px;
        margin-top: 60px;
        text-align: center;
    }
</style>
