<template>
    <div>
        <test v-on:event_child="eventChild"></test>
        {{get_child_info}}
        <test :value="put_to_child"></test>
    </div>
</template>

<script>
    import Test2 from './Test2'

    export default {
        name: "Test",
        data(){
            return {
                get_child_info:'',
                put_to_child: 'Hello world'
            }
        },

        components:{
            'test': Test2
        },

        methods: {
            eventChild: function(info) {
                this.get_child_info = info
            },
        },

    }
</script>

<style scoped>

</style>
