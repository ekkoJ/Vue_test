<template lang="html">
    <div class="frame2">
        <div class="content-wrapper">
            <!--<div class="title">Who are you shopping for?</div>-->
        </div>
        <ul class="grid-wrapper">
            <!--<li class="person" v-for="(item, index) in personData" key="index">
                <div class="cover-wrapper">
                    <img :src="`image/r29/image/${item.toLowerCase()}.svg`" alt="" class="normal">
                    <img :src="'image/r29/image/' + item.toLowerCase() + '_hover.svg'" alt="" class="hover">
                </div>
                <div class="name">{{ item }}</div>
            </li>-->

        </ul>
        <div class="box"></div>
        <ul class="projects">
            <li>
                <div class="bg-placeholder">
                    <img src="image/picture1.png" alt="">
                </div>
                <div class="bg">
                    <img src="image/picture1.png" alt="">
                </div>
                <div class="gradient">
                    <img src="image/shadow.png" alt="">
                </div>
            </li>
            <li>
                <div class="bg-placeholder">
                    <img src="image/picture1.png" alt="">
                </div>
                <div class="bg">
                    <img src="image/picture1.png" alt="">
                </div>
                <div class="gradient">
                    <img src="image/shadow.png" alt="">
                </div>
            </li>
            <li>
                <div class="bg-placeholder">
                    <img src="image/picture1.png" alt="">
                </div>
                <div class="bg">
                    <img src="image/picture1.png" alt="">
                </div>
                <div class="gradient">
                    <img src="image/shadow.png" alt="">
                </div>
            </li>
            <li>
                <div class="bg-placeholder">
                    <img src="image/picture1.png" alt="">
                </div>
                <div class="bg">
                    <img src="image/picture1.png" alt="">
                </div>
                <div class="gradient">
                    <img src="image/shadow.png" alt="">
                </div>
            </li>
            <li>
                <div class="bg-placeholder">
                    <img src="image/picture1.png" alt="">
                </div>
                <div class="bg">
                    <img src="image/picture1.png" alt="">
                </div>
                <div class="gradient">
                    <img src="image/shadow.png" alt="">
                </div>
            </li>
            <li>
                <div class="bg-placeholder">
                    <img src="image/picture1.png" alt="">
                </div>
                <div class="bg">
                    <img src="image/picture1.png" alt="">
                </div>
                <div class="gradient">
                    <img src="image/shadow.png" alt="">
                </div>
            </li>
        </ul>
        <div class="box"></div>
    </div>
</template>

<script>

export default {
    data () {
        return {
            personData: [
               'MOM',
               'DAD',
               'S.O.',
               'BFF',
               'WORK SPOUSE',
               'SUPRISE'
            ]
        }
    },
    methods: {
        
    }
}
</script>

<style lang="scss">
.frame2 {
    .content-wrapper{
        position: absolute;
        top: 50%;
        left: 50%;
        width: 90%;
        max-width: 850px;
        text-align: center;
        transform: translateX(-50%) translateY(-50%);
        .title{
            font-family: BrownStd-Bold;
            font-size: 22px;
            letter-spacing: 2px;
            text-align: center;
            color: #ce912c;
            transform: translate3d(0,0,0);
        }
        .grid-wrapper{
            margin-top: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-wrap: wrap;
            li{
                position: relative;
                width: 30%;
                margin: 1.4%;
                cursor: pointer;
                text-align: center;
                .cover-wrapper{
                    position: relative;
                    .normal{
                        position: absolute;
                        top: 0;
                        left: 0;
                        width: 100%;
                        opacity: 1;
                    }
                    .hover{
                        position: relative;
                        opacity: 0;
                        transition: opacity .2s linear;
                    }
                }
            }
        }
    }
    .box{
        background: #000;
        height: 300px;
        width: 1200px;
        margin: 0 auto;
    }
    .projects{
        position: relative;
        background-color: black;
        max-width: 1200px;
        margin: 0 auto;
        li{
            position: relative;
            display: inline-block;
            overflow: hidden;
            width: 400px;
            vertical-align: top;
            cursor: pointer;
            div{
                img{
                    width: 100%;
                    display: block;
                }
            }
            .bg-placeholder{
                position: relative;
                width: 100%;
            }
            .bg{
                position: absolute;
                top: 0;
                left: 0;
                width: 100%;
                height: 100%;
                transition: transform cubic-bezier(0.165, 0.84, 0.44, 1) 0.3s, -webkit-transform cubic-bezier(0.165, 0.84, 0.44, 1) 0.3s;
            }
            .gradient {
                position: absolute;
                // width: 100%;
                height: 80%;
                left: -2px;
                right: -1px;
                top: auto;
                bottom: -1px;
                transform: translate3d(0,0,0);
                transition: height cubic-bezier(0.165, 0.84, 0.44, 1) 0.5;
                img {
                    height: 100%;
                }
            }
            &:hover {
                .bg {
                    transform: scale(1.12);
                    transition: all 0.3s ease;
                }

                .gradient {
                    height: 200%;
                    transition: all 0.3s ease;
                }
            }
        }
    }
}
</style>