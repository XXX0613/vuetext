<template>
    <div class="classbangding">
        <h3>class动态绑定</h3>
        <p :class="myclass">11111111</p>
        <h5>动态绑定示例</h5>
        <p :class="{ 'action': isActive, 'text-danger': hasError}">class绑定样式1</p>
        <p :class="clsaaObject">class绑定样式2</p>
        <h5>动态绑定数组示例</h5>
        <p :class="[arrAction, arrHasError]">class绑定样式3</p>
        <p :class="[isAction ? 'action' : '']">class绑定样式4</p>
    </div>

</template>

<script>
export default {
    name: 'classbangding',

    data() {
        return {
            myclass: 'demo',
            isActive: true,
            hasError: false,
            clsaaObject: {
                'action': true,
                'text-danger': true
            },
            arrAction: 'active',
            arrHasError: 'text-danger',
        };
    },
}

</script>

<style scoped>
.classbangding {
    color: slateblue;
}
.active {
    font-size: 35px;
}
text-danger {  
    color: red;
}
</style>