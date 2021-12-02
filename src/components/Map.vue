<template>
  <div v-for="p, index in parking" :key="index">{{p}}</div>
</template>

<script>
export default {
    name: 'mymap',
    data () {
        return{
            
        }
    },
    props: {
        parking: []
    },
    methods: {

    }
}
</script>

<style>

</style>