<template>
    <div class="shijianchuancan">
        <h3>事件传参</h3>
        <button @click="count1">add 454</button>
        <p>count is {{ countNum }}</p>
        <button @click="newCount('hello syxy')">newCount 222</button>
        <hr>
    </div>
</template>

<script> 
export default {
    name: 'shijianchuancan',
    data() {
        return {
            countNum: 0,
            newCountNum: 20
        }
    },
    methods: {
        count1(e) {
            console.log(e, '454545454545454545');
            console.log(e.target,'e.target.target.target.target');
            console.log(e.currentTarget,'e.currentTarget.currentTarget.currentTarget');
            console.log(e.target.innerHtml,'e.target.innerHTML.target.innerHTML.target.innerHTML');
            e.target.innerHTML = '添加添加' + this.countNum;
            this.countNum += 454;
        },
        newCount(msg) {
            console.log(msg, 'msgmsgmsgmsgmsgmsg');
        },
    }
}

</script>

<style scoped>
.shijianchuancan {
    color: royalblue;
}
</style>