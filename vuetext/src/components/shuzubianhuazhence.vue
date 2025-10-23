<template>
    <div class="shuzubianhuazhence">
        <h3>数组变化侦测</h3>
        <button @click="addData">添加数据</button>
        <ul>
            <li v-for="(value, index) in names">{{ value }}</li>
        </ul>

        <button @click="hebingshuzu">合并数据</button>
        <h1>数组1</h1>
        <p v-for="(value, index) in arr1" :key="index">{{ value }}</p>
        <h1>数组2</h1>
        <p v-for="(value, index) in arr2" :key="index">{{ value }}</p>
    </div>
</template>

<script>
    export default {
        name: 'shuzubianhuazhence',
        data() {
            return {
                names: ['张三', '李四', '王五'],
                arr1: [1,2,3],
                arr2: [4,5,6]
            }
        },
        methods: {
            addData() {
                this.names.push('赵六');

                console.log(this.names.concat(['赵六']));
            },
            hebingshuzu() {
                // this.arr1 = this.arr1.concat(this.arr2);
                this.arr1 = [...this.arr1, ...this.arr2];
            },
        }
    }
</script>

<style scoped>
.shuzubianhuazhence{
    color: aqua;
}
</style>