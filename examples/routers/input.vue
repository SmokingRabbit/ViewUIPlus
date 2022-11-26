<template>
    <div>
        <Button @click="handleFocus('start')">Focus at first</Button>
        <Button @click="handleFocus('end')">Focus at last</Button>
        <Button @click="handleFocus('all')">Focus to select all</Button>
        <Button @click="handleFocus('preventScroll')">Focus prevent scroll</Button>
        <Input ref="input" v-model="value20" placeholder="Enter something..." style="margin-top: 16px" />
        <Input maxlength="100" show-word-limit type="textarea" placeholder="Enter something..." style="width: 200px" />
        <Input prefix="ios-contact" placeholder="Enter name" style="width: auto" />
        <Input suffix="ios-search" placeholder="Enter text" style="width: auto" />
        <Input>
            <template #prepend>
              <span>http://</span>
            </template>
            <template #append>
              <span>.com</span>
            </template>
        </Input>

        <Input disabled modelValue="dasdsadasdas" />

        <Input search placeholder="Enter something..." />
        <Input search enter-button placeholder="Enter something..." />
    </div>
</template>
<script>
    export default {
        data () {
            return {
                value20: 'View UI’s birthday is July 28'
            }
        },
        methods: {
            handleFocus (type) {
                if (type === 'preventScroll') {
                    this.$refs.input.focus({
                        preventScroll: true
                    });
                } else {
                    this.$refs.input.focus({
                        cursor: type
                    });
                }
            }
        }
    }
</script>
