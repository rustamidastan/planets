<template lang="html">
    <div class="planet">
            <div class="container planet__container ">
                <div class="planet__top">
                    <div class="planet__img-wrapper">
                        <img :src="planets.infos[queue].img" :style="{width: planets.linkStyle.width, height: planets.linkStyle.height}">
                    </div>

                    <div class="planet__info">
                        <div class="planet__info-details">
                            <h1 class="planet__name">{{planets.name}}</h1>
                                
                            <p :style="{color: 'white'}">{{planets.infos[queue].text}}</p>

                            <div class="planet__source">
                                <span>Source : </span>
                                <a href="wikipedia.com/">Wikipedia</a>
                                <img :src="arrowImg">
                            </div>
                        </div>

                        <div class="planet__tabs">
                            <div class="tab" :style="[selectedTab==tab ? {'backgroundColor': selectedColor + '!important'} : {'background': 'transparent'}]"   :class="{'tab-active': selectedTab===tab}"  v-for="(tab, index) in tabs" :key="index" @click="selectedTab=tab, queue=index" >
                                <span>0{{index +1}}</span>
                                <span>{{tab}}</span>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="planet__bottom">
                    <ul class="planet__bottom-list">
                        <li class="planet__bottom-item">  
                            <span>ROTATION TIME</span>
                            <span>{{planets.selfValues.roTime}}</span>
                        </li>

                        <li class="planet__bottom-item">  
                            <span>REVOLUTION TIME</span>
                            <span>{{planets.selfValues.reTime}}</span>
                        </li>

                        <li class="planet__bottom-item">  
                            <span>radius</span>
                            <span>{{planets.selfValues.radius}}</span>
                        </li>

                        <li class="planet__bottom-item">  
                            <span>AVERAGE TEMP.</span>
                            <span>{{planets.selfValues.avTemp}}</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
</template>

<script>

import arrowImg from '../assets/wikipedia.png'
export default {
    props: {
        planets: {
            type: Object,
            required: true
        }
    },

    data() {
        return {
            queue: 0,
            arrowImg: arrowImg,
            tabs: ["OVERVIEW","Internal Structure","Surface Geology"],
            selectedTab: "OVERVIEW",
            selectedColor: this.planets.linkStyle.color
        }
    },
    // methods: {
    //     getImage (img) {
    //     return   require( `../assets/icons/${this.icon}.svg`);

        
    // }
    // },
    computed: {
    background () {
        return this.selectedTab ? 'backgroundColor' : `this.planets.linkStyle.color !important`
      }
    }
}

</script>

<style >

.planet {
    max-width: 1440px;
    margin: 0 auto;
    background-color: #070724;
    background-image: url(../assets/bg-image.png);
    background-repeat: no-repeat;

}

.container {
    max-width: 1100px;
    margin: 0 auto;
}

.planet__container {
    padding-bottom: 56px;
    display: flex;
    flex-direction: column;
}

.planet__top {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.planet__img-wrapper {
    width: 666px;
    max-height: 666px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.planet__info {
    padding-top: 126px;
    padding-bottom: 90px;
}

.planet__info-details {
    max-width: 350px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}

.planet__info p {
    font-family: "Spartan";
    font-size: 14px;
    line-height: 25px;
    font-weight: 400;
    margin-bottom: 25px;
    text-align: left;
}

.planet__name {
    margin-bottom: 25px;
    font-size: 80px;
    line-height: 103px;
    font-weight: 400;
    color: #fff;
    text-transform: uppercase;
}

.planet__tabs {
    margin-top: 40px;
    display: flex;
    flex-direction: column;
}

.tab {
    display: flex;
    align-items: center;
    padding: 12px 28px;
    cursor: pointer;
    border: 1px solid #FFFFFF;
    background-color: transparent;
    color: #fff;
    text-transform: uppercase;
    text-align: left;
    text-decoration: none;
    font-size: 12px;
    line-height: 25px;
    font-weight: 700;
    letter-spacing: 2.57px;
    font-family: "Spartan";
    transition: all 0.3s ease;
}

.tab:not(:last-child) {
    margin-bottom: 16px;
}

.tab span:first-child {
    display: block;
    margin-right: 25px;
    opacity: 0.5;
}

.tab:hover {
    background-color: rgba(216, 216, 216, 0.2);
    border-color: transparent;
}

.tab-active {
    /* background-color: #419EBB; */
    border-color: transparent;
}

.planet__source span {
    color: #fff;
    opacity: 0.5;
    font-size: 14px;
    line-height: 25px;
    font-family: "Spartan";
    font-weight: 400;
}

.planet__source a {
    color: #fff;
    opacity: 0.7;
    font-size: 14px;
    line-height: 25px;
    font-family: "Spartan";
    font-weight: 400;
    transition: all 0.3s ease;
}

.planet__source a:hover {
    opacity: 1;
}

.planet__bottom-list {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.planet__bottom-item {
    box-sizing: border-box;
    padding: 25px;
    width: 255px;
    height: 128px;
    border: 1px solid #fff;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}

.planet__bottom-item span:first-child {
    font-size: 11px;
    line-height: 25px;
    font-weight: 700;
    color: #fff;
    opacity: 0.5;
    letter-spacing: 1px;
    font-family: "Spartan";
}

.planet__bottom-item span:last-child {
    font-size: 40px;
    line-height: 51px;
    font-weight: 400;
    color: #fff;
    letter-spacing: -1px;
}


@media screen and (max-width:880px) {
        .container {
            max-width: 100%;
            padding: 0 7%;
        }
        .planet__top {
            width: 100%;
            flex-direction: column;
        }

        .planet__img-wrapper {
            width: 435px;
            height: 435px;
            margin: 0 auto;
            padding-top: 38px;
            padding-bottom: 11px;
        }

        

        .planet__info {
            width: 100%;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding-top: 0;
            padding-bottom: 27px;
        }

        .planet__info-details {
            max-width: 340px;
        }

        .planet__name {
            font-size: 48px;
            line-height: 62px;
        }

        .planet__info p {
            font-size: 11px;
            line-height: 22px;
        }

        .planet__source span {
            font-size: 12px;
        }

        .tab {
            padding: 8px 20px;
            font-size: 9px;
        }

        .planet__bottom {
            padding-bottom: 30px;
        }

        .planet__bottom-item {
            box-sizing: border-box;
            width: 155px;
            height: 88px;
            padding: 15px;
        }

       .planet__bottom-item span:first-child {
            font-size: 8px;
            line-height: 16px;
            letter-spacing: 0.73px;
        }

        .planet__bottom-item span:last-child {
            font-size: 24px;
            line-height: 31px;
            letter-spacing: -0.9px;
        }
}
</style>
