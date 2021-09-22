<template>
  <div id="app">
    <div id="nav">
    </div>
    <header>
        <a href="/" class="site-logo">THE PLANETS</a>

        <ul class="header__list">
            <router-link class="nav-link" :style="[selectedItem=='mercury' ? {'borderColor': '#419EBB', 'opacity': '1', 'color': '#419EBB'} : {'background': 'transparent'}]" @click.native="selectedItem='mercury'" :to="{name: 'mercury'}">Mercuriy</router-link>
            <router-link class="nav-link" :style="[selectedItem=='venus' ? {'borderColor': '#EDA249', 'opacity': '1', 'color': '#EDA249'} : {'background': 'transparent'}]" @click.native="selectedItem='venus'" :to="{name: 'venus'}">Venus</router-link>
            <router-link class="nav-link" :style="[selectedItem==='earth' ? {'borderColor': '#6D2ED5', 'opacity': '1', 'color': '#6D2ED5'} : {'background': 'transparent'}]" @click.native="selectedItem='earth'" :to="{name: 'earth'}">Earth</router-link>
            <router-link class="nav-link" :style="[selectedItem==='mars' ? {'borderColor': '#D14C32', 'opacity': '1', 'color': '#D14C32'} : {'background': 'transparent'}]" @click.native="selectedItem='mars'" :to="{name: 'mars'}">Mars</router-link>
            <router-link class="nav-link" :style="[selectedItem==='jupiter' ? {'borderColor': '#D83A34', 'opacity': '1', 'color': '#D83A34'} : {'background': 'transparent'}]" @click.native="selectedItem='jupiter'" :to="{name: 'jupiter'}">Jupiter</router-link>
            <router-link class="nav-link" :style="[selectedItem==='saturn' ? {'borderColor': '#CD5120', 'opacity': '1', 'color': '#CD5120'} : {'background': 'transparent'}]" @click.native="selectedItem='saturn'" :to="{name: 'saturn'}">Saturn</router-link>
            <router-link class="nav-link" :style="[selectedItem==='uranus' ? {'borderColor': '#1EC1A2', 'opacity': '1', 'color': '#1EC1A2'} : {'background': 'transparent'}]" @click.native="selectedItem='uranus'" :to="{name: 'uranus'}">Uranus</router-link>
            <router-link class="nav-link" :style="[selectedItem==='neptune' ? {'borderColor': '#2D68F0', 'opacity': '1', 'color': '#2D68F0'} : {'background': 'transparent'}]" @click.native="selectedItem='neptune'" :to="{name: 'neptune'}">Neptune</router-link>
        </ul>
    </header>
    <router-view />
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedItem: 'mercury',
    }
  }
}
</script>

<style>
#app {
  font-family: Antonio, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: #070724;
  box-sizing: border-box;
}

header {
    max-width: 1400px;
    height: 85px;
    margin: 0 auto;
    padding: 0 35px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    border-bottom: 1px solid rgba(255, 255, 255, 0.2);
}

.site-logo {
    font-size: 28px;
    line-height: 36px;
    font-weight: 400;
    color: #FFFFFF;
    letter-spacing: -1px;
    text-decoration: none;
}

.header__list {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
}

.nav-item {
    margin-left: 33px;
}

.nav-link {
    padding: 28px 0;
    color: #fff;
    text-decoration: none;
    font-size: 11px;
    line-height: 25px;
    font-weight: 700;
    letter-spacing: 1px;
    font-family: "Spartan";
    text-transform: uppercase;
    transition: all 0.3s ease;
    border-top: 4px solid transparent;
    opacity: 0.75;
}

.nav-link:not(:last-child) {
  margin-right: 33px;
}

.nav-link:hover {
    border-top: 4px solid transparent;
    opacity: 1;
}

@media screen and (max-width:880px) {
    header {
      box-sizing: border-box;
      height: 159px;
      padding-top: 32px;
      flex-direction: column;
    }

    .site-logo {
        display: block;
    }

    .nav-link {
      padding: 20px 0;
      display: block;
    }
}


</style>
