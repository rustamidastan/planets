<template>
    <div>
        <Planet :planets="planets" />
    </div>
</template>


<script>
import Planet from '@/components/Planet.vue'
import neptune from '../assets/neptune.png'
import neptuneStructure from '../assets/neptune-structure.png'
import neptuneGeo from '../assets/neptune-geo.png'

export default {
    components: {
        Planet
    },
    data() {
        return {
             planets: 
            {
                name: 'neptune',
                linkStyle: {
                    color: '#2D68F0',
                    width: '67.5%',
                    height: 'auto'
                },
                infos: [
                    {
                        img: neptune,
                        text: "Neptune is the eighth and farthest-known Solar planet from the Sun. In the Solar System, it is the fourth-largest planet by diameter, the third-most-massive planet, and the densest giant planet. It is 17 times the mass of Earth, more massive than its near-twin Uranus."
                    },
                    {
                        img: neptuneStructure,
                        text: "Neptune's internal structure resembles that of Uranus. Its atmosphere forms about 5% to 10% of its mass and extends perhaps 10% to 20% of the way towards the core. Increasing concentrations of methane, ammonia and water are found in the lower regions."
                    },
                    {
                        img: neptuneGeo,
                        text: "Neptune's atmosphere is 80% hydrogen and 19% helium. A trace amount of methane is also present. Prominent absorption bands of methane exist at wavelengths above 600 nm, in the red and infrared portion of the spectrum."
                    }
                ],
                selfValues: {
                    roTime: "16.08 hours",
                    reTime: "164.79 years",
                    radius: "24,622 km",
                    avTemp: "-201°c"
                }
            }
        }
    }
    
}
</script>

