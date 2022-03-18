<template>
  <h1>{{heroTitle}}</h1>
  <p>{{heroDetails}}</p>
</template>

<script>
    export default{
        name: "Hero-app",
        data(){
            return{
                heroTitle: "This is the best hero in town",
                heroDetails: "World best wrestler from Cameroon"
            };
        },
    };
</script>

<style scoped>
</style>