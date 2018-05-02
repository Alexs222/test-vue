<template lang="pug">
    div
        input(type="text" v-model="name" @keydown.enter="handleChange")
        br
        input(type="checkbox" value="one" v-model="counter")
        .span one
        input(type="checkbox" value="two" v-model="counter")
        .span two
        input(type="checkbox" value="three" v-model="counter")
        .span three
      
        //- h1 {{title}}
        //- button(
        //-     type='button'
        //-     @click='emitClick'
        //- ) Кнопка
        //- .wrap
        //-     .top
        //-         slot(name='top')
        //-     .bottom
        //-         slot(name='bottom')
        //-     .default
        //-         slot(name='default')

</template>


<script>
export default {
    data() {
        return {
            name: "",
            counter: ["one", "three"]
        }
    },
    props: {
        title: {
            type: String,
            default: "Hello world"
        }
    },
    methods: {
        emitClick() {
            this.$emit('buttonWasClicked', 'sting', 12345, true);
        },
        handleChange() {
            this.name = "";
        }
    }

}
</script>

<style lang="scss" scoped>
</style>



