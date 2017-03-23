<template lang="html">
    <div class="container">
        {components[0]}
        <test1 v-if="showframe === 1"></test1>
        <test2 v-if="showframe === 2"></test2>
        <test3 v-if="showframe === 3"></test3>
        <test4 v-if="showframe === 4"></test4>
        <test5 v-if="showframe === 5"></test5>
        <FilterCom v-if="showframe === 6"></FilterCom>
        <r29 v-if="showframe === 7"></r29>
        <div class="chooseFrame">
         <p>show frame <input v-model="textframe" @input="textin"></input></p>
         <p>please write the number of 1 - 7</p>
        </div>
    </div>
</template>

<script>
import test1 from './components/test1.vue';
import test2 from './components/test2.vue';
import test3 from './components/test3.vue';
import test4 from './components/test4.vue';
import test5 from './components/test5.vue';
import FilterCom from './components/FilterCom.vue';
import r29 from './components/main.vue';

export default {
    data () {
        return {
            textframe: 1,
            // comlength: components.length,
        }
    },
    components: {
        test1,
        test2,
        test3,
        test4,
        test5,
        FilterCom,
        r29,
    },
    computed: {
        showframe: function(){
            return parseInt(this.textframe);
        }
    },
    methods: {
        textin() {
            // if (parseInt(this.textframe) > 7 || parseInt(this.textframe) < 1) {
            //     this.textframe = this.textframe;
            //     return;
            // } 
        }
    }
}
</script>

<style lang="scss">
@import "./style/reset";
@import "./style/mixin";

*{
    margin: 0;
    padding: 0;
    font-size: 0;
}
body, html {
    width: 100%;
    height: 100%;
    overflow: hidden;
}
body {
    background-color: #fcf3f4;
}
#main{
    width: 100%;
    height: 100%;
    .container{
        width: 100%;
        height: 100%;
    }
}
.chooseFrame{
    position: fixed;
    top: 0;
    right: 5%;
    p{
        font-size:16px;
    }
    input{
        width: 50px;
        height: 50px;
        font-size:16px;
    }
}
.disnone{
    display: none !important;
}
</style>