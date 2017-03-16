<template lang="html">
    <div class="lastframe">
        {{ selectType }}
        {{ selectName }}
    </div>
</template>

<script>

export default {
    data () {
        return {

        }
    },
    props: ['selectType','selectName'],
    methods: {
        
    }
}
</script>

<style lang="scss" scoped>
.lastframe {
    font-size: 16px;
}
</style>