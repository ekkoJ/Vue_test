<template lang="html">
    <div class="main">
        <!--<transition name="fade">-->
            <frame1 @cilckEvent="changeFrame(1)" v-if="showFrame === 0"></frame1>
            <frame2 @cilckEvent="changeFrame(2)" v-if="showFrame === 1"></frame2>
            <frame3 @cilckEvent="changeFrame(3)" v-if="showFrame === 2"></frame3>
            <lastFrame></lastFrame>
        <!--</transition>-->
    </div>
</template>

<script>
import frame1 from './r29/frame1.vue';
import frame2 from './r29/frame2.vue';
import frame3 from './r29/frame3.vue';
import lastFrame from './r29/lastFrame.vue';

export default {
    
    data () {
        return {
            showFrame: 1,
        }
    },
    components: {
        frame1,
        frame2,
        frame3,
        lastFrame
    },
    methods: {
        changeFrame(frame) {
            this.showFrame = frame;
        }
    }
}
</script>

<style lang="scss" scoped>

.main {
    width: 100%;
    height: 100%;
    overflow: auto;
    
}
.fade-enter-active, .fade-leave-active {
  transition: opacity .5s
}
.fade-enter, .fade-leave-active {
  opacity: 0
}
</style>