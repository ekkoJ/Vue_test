<template lang="html">
    <div class="frame3">
        <div class="back-container" @click="backFrame">
            <span class="back">
                back
            </span>
        </div>
        <div class="content-wrapper">
            <h3 class="title">
                What is your
                <span class="person-name">{{ selectName }}</span>
                like?
            </h3>
            <h3 class="title">
                Choose {{ total }} <span v-if="total === 1">trait</span><span v-if="total != 1">traits</span>.
            </h3>
            <ul class="trait-list">
                <li v-for="(item, index) in traits"
                    key="index"
                >
                    
                    <label>
                        <input type="checkbox">
                        <div class="flag-box">
                            <div class="circle-container">
                            <div class="circle"></div>
                            <img class="circle-hover" src="image/r29/image/circle_hover.png"></div>
                        <span class="trait">{{ item }}</span>
                        </div>
                    </label>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>

export default {
    data () {
        return {
            traits: [
                'CHILL',
                'CHIC AESTHETE',
                'EMO',
                'TYPE A',
                'EARLY ADOPTER',
                'FANCY'
            ],
            total: 3,
        }
    },
    props: ['selectName'],
    methods: {
        backFrame() {
            this.$emit('cilckEvent',1);
        }
    }
}
</script>

<style lang="scss" scoped>
.frame3 {
    .back-container{
        position: absolute;
        left: 24px;
        top: 20px;
        cursor: pointer;
        .back{
            font-family: BrownStd-Bold;
            font-size: 20px;
            line-height: 44px;
            color: #ce912c;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-left: 10px;
            transition: color .2s ease;
        }
        &:hover{
            .back{
                color: #f00;
            }
        }
    }
    .content-wrapper{
        position: absolute;
        top: 50%;
        left: 50%;
        width: 70%;
        text-align: center;
        transform: translateX(-50%) translateY(-50%);
        .title{
            width: 571px;
            margin: 0 auto;
            text-align: center;
            color: #ce912c;
            font-family: BrownStd-Bold;
            font-size: 22px;
            line-height: 44px;
            letter-spacing: 2px;
            span{
                font-family: BrownStd-Bold;
                font-size: 20px;
                line-height: 44px;
                &.person-name{
                    text-transform: uppercase;
                }
            }
        }
        .trait-list{
            margin-top: 40px;
            li{
                padding: 15px 0;
                cursor: pointer;
            }
            label{
                width: 100%;
                height: 100%;
                cursor: pointer;
            }
            input[type=checkbox] {
                // display: none;
            }
            input[type=checkbox] {
                -webkit-appearance: checkbox;
                box-sizing: border-box;
                background-color: initial;
                margin: 3px 0.5ex;
                padding: initial;
                border: initial;
                -webkit-rtl-ordering: logical;
                user-select: text;
                cursor: auto;
            }
            .flag-box{
                width: 378px;
                display: inline-block;
                text-align: left;
            }
            .circle-container{
                position: relative;
                display: inline-block;
                vertical-align: middle;
                .circle{
                    position: absolute;
                    top: 0;
                    left: 0;
                    width: 30px;
                    height: 30px;
                    border: 2px solid #ce912c;
                    border-radius: 50%;
                }
                .circle-hover{
                    position: relative;
                    width: 30px;
                    opacity: 0;
                }
            }
            .trait{
                font-family: BrownStd-Bold;
                margin-left: 50px;
                padding: 5px 0;
                font-size: 26px;
                letter-spacing: 6px;
                color: #ce912c;
                display: inline-block;
                vertical-align: middle;
                text-transform: uppercase;
                border-bottom: 3px solid;
                border-bottom-color: transparent;
            }
        }
    }
}
</style>