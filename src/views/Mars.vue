<template>
    <div>
        <Planet :planets="planets" />
    </div>
</template>


<script>
import Planet from '@/components/Planet.vue'
import mars from '../assets/mars.png'
import marsStructure from '../assets/mars-structure.png'
import marsGeo from '../assets/mars-geo.png'

export default {
    components: {
        Planet
    },
    data() {
        return {
             planets: 
            {
                name: 'mars',
                linkStyle: {
                    color: '#D14C32',
                    width: '49%',
                    height: 'auto'
                },
                infos: [
                    {
                        img: mars,
                        text: 'Mars is the fourth planet from the Sun and the second-smallest planet in the Solar System, being larger than only Mercury. In English, Mars carries the name of the Roman god of war and is often referred to as the "Red Planet".'
                    },
                    {
                        img: marsStructure,
                        text: 'Like Earth, Mars has differentiated into a dense metallic core overlaid by less dense materials. Scientists initially determined that the core is at least partially liquid. Current models of its interior imply a core consisting primarily of iron and nickel with about 16–17% sulfur.'
                    },
                    {
                        img: marsGeo,
                        text: 'Mars is a terrestrial planet whose surface consists of minerals containing silicon and oxygen, metals, and other elements that typically make up rock. The surface is primarily composed of tholeiitic basalt, although parts are more silica-rich than typical basalt.'
                    }
                ],
                selfValues: {
                    roTime: "1.03 days",
                    reTime: "1.88 years",
                    radius: "3,389.5 km",
                    avTemp: "−28°c"
                }
            }
        }
    }
    
}
</script>

