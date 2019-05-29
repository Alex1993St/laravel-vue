<template>
    <div>
        <!--<button v-on:click="emit">-->
            <!--Clique me to emit from child component-->
        <!--</button>-->
        <div>{{value}}</div>
    </div>
</template>

<script>
    export default {
        name: "Test2",
        props: ['value'],
        data(){
            return {
                info: {
                    title: 'test',
                    name: '123'
                },
            }
        },

        created(){
            this.$emit('event_child', this.info)
        }

    }
</script>

<style scoped>

</style>
