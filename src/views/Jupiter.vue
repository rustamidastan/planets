<template>
    <div>
        <Planet :planets="planets" />
    </div>
</template>


<script>
import Planet from '@/components/Planet.vue'
import jupiter from '../assets/jupiter.png'
import jupiterStructure from '../assets/jupiter-structure.png'
import jupiterGeo from '../assets/jupiter-geo.png'

export default {
    components: {
        Planet
    },
    data() {
        return {
             planets: 
            {
                name: 'jupiter',
                linkStyle: {
                    color: '#D83A34',
                    count: false,
                    width: '85%',
                    height: '85%'
                },
                infos: [
                    {
                        img: jupiter,
                        text: 'Jupiter is the fifth planet from the Sun and the largest in the Solar System. It is a gas giant with a mass two and a half times that of all the other planets in the Solar System combined, but less than one-thousandth the mass of the Sun.'
                    },
                    {
                        img: jupiterStructure,
                        text: "When the Juno arrived in 2016, it found that Jupiter has a very diffuse core that mixes into its mantle. A possible cause is an impact from a planet of about ten Earth masses a few million years after Jupiter's formation, which would have disrupted an originally solid Jovian core."
                    },
                    {
                        img: jupiterGeo,
                        text: 'The best known feature of Jupiter is the Great Red Spot, a persistent anticyclonic storm located 22° south of the equator. It is known to have existed since at least 1831, and possibly since 1665.'
                    }
                ],
                selfValues: {
                    roTime: "9.93 hours",
                    reTime: "11.86 years",
                    radius: "69,911 km",
                    avTemp: "-108°c"
                }
            }
        }
    }
    
}
</script>

