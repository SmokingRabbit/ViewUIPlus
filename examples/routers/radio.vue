<template>
    <Radio v-model="disabledSingle" disabled>Radio</Radio>
    <RadioGroup v-model="disabledGroup">
        <Radio label="金斑蝶" disabled></Radio>
        <Radio label="爪哇犀牛"></Radio>
        <Radio label="印度黑羚"></Radio>
    </RadioGroup>

    <RadioGroup type="button">
        <Radio label="北京"></Radio>
        <Radio label="上海"></Radio>
        <Radio label="深圳"></Radio>
        <Radio label="杭州"></Radio>
    </RadioGroup>

    <RadioGroup type="button" button-style="solid">
        <Radio label="北京"></Radio>
        <Radio label="上海"></Radio>
        <Radio label="深圳"></Radio>
        <Radio label="杭州"></Radio>
    </RadioGroup>
    <RadioGroup v-model="button2" type="button" button-style="solid">
        <Radio label="北京"></Radio>
        <Radio label="上海" disabled></Radio>
        <Radio label="深圳"></Radio>
        <Radio label="杭州"></Radio>
    </RadioGroup>
</template>
<script>
    export default {
        data () {
            return {
                disabledSingle: true,
                disabledGroup: '爪哇犀牛'
            }
        }
    }
</script>
