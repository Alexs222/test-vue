<template lang="pug">
    div
        h1 {{title}}
        button(
            type='button'
            @click='emitClick'
        ) Кнопка
        .wrap
            .top
                slot(name='top')
            .bottom
                slot(name='bottom')
            .default
                slot(name='default')

</template>


<script>
export default {
    props: {
        title: {
            type: String,
            default: "Hello world"
        }
    },
    methods: {
        emitClick() {
            this.$emit('buttonWasClicked', 'sting', 12345, true);
        }
    }

}
</script>

<style lang="scss" scoped>
</style>



