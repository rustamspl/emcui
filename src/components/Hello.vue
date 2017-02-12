<template>
    <div class="hello">
        <button @click="test">
            test1
        </button>
    </div>
</template>
<script>
var data={}
export default {
    data(){return data},
    methods:{

    test:function() {
        this.$http.get('/').then(res => {
            console.log(res.body);

        });
    }
    }
}
</script>
<style scoped="">
    .hello{
    padding: 50px;
    margin: 50px auto;
}
</style>
