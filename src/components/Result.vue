<template>
  <div class="result">
        <div class="title">{{results[resultIndex].title}}</div>
        <div class="desc">
            {{results[resultIndex].desc}}
        </div>
    </div>
</template>

<script>
export default {
name:"Result",
props:["results","totalCorrectAns"],
computed:{
    resultIndex(){
        let index = 0;

        this.results.forEach((e,i) => {
            if(e.min<=this.totalCorrectAns && e.max>=this.totalCorrectAns){
                index =i;
            }
        });

        return index;
    }
}
}
</script>

<style>

</style>