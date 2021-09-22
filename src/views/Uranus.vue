<template>
    <div>
        <Planet :planets="planets" />
    </div>
</template>


<script>
import Planet from '@/components/Planet.vue'
import uranus from '../assets/uranus.png'
import uranusStructure from '../assets/uranus-structure.png'
import uranusGeo from '../assets/uranus-geo.png'

export default {
    components: {
        Planet
    },
    data() {
        return {
             planets: 
            {
                name: 'uranus',
                linkStyle: {
                    color: '#1EC1A2',
                    width: '68%',
                    height: 'auto'
                },
                infos: [
                    {
                        img: uranus,
                        text: "Uranus is the seventh planet from the Sun. Its name is a reference to the Greek god of the sky, Uranus according to Greek mythology, was the great-grandfather of Ares. It has the third-largest planetary radius and fourth-largest planetary mass in the Solar System."
                    },
                    {
                        img: uranusStructure,
                        text: "The standard model of Uranus's structure is that it consists of three layers: a rocky (silicate/iron–nickel) core in the centre, an icy mantle in the middle and an outer gaseous hydrogen/helium envelope. The core is relatively small, with a mass of only 0.55 Earth masses."
                    },
                    {
                        img: uranusGeo,
                        text: "The composition of Uranus's atmosphere is different from its bulk, consisting mainly of molecular hydrogen and helium. The helium molar fraction, i.e. the number of helium atoms per molecule of gas, is 0.15±0.03 in the upper troposphere."
                    }
                ],
                selfValues: {
                    roTime: "17.2 hours",
                    reTime: "84 years",
                    radius: "25,362 km",
                    avTemp: "-195°c"
                }
            }
        }
    }
    
}
</script>

