<template>
    <div class="shijianxiushifu">
        <h3>事件修饰符</h3>
        <a @click.prevent="click11" href="https://www.baidu.com">百度百度</a>
        
        <div @click="clickDiv">
            <p @click.stop="clickp">测试冒泡</p>
        </div>

    </div>
</template>

<script>
export default {
    name: 'shijianxiushifu',
    data(){
        return{
        }
    },
    methods:{
        click11(e) {
            e.preventDefault();
            console.log('点击了百度百度')
        },
        clickDiv() {
            console.log('点击了div')
        },
        clickp() {
            console.log('点击了p')
        }
    }
}
</script>

<style scoped>
.shijianxiushifu{
    color: slateblue;   
}
</style>