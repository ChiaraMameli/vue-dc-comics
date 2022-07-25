<template>
    <header class="container">
        <nav>
            <a href="#">
                <img src="../assets/img/dc-logo.png" alt="dc logo">
            </a>

            <div id="nav-links">
                <ul>
                    <li v-for="link in NavBar" v-bind:key="link.text" :class="{'active' : link.current}"><a :href="link.url">{{link.text}}</a></li>
                </ul>
            </div>
        </nav>
    </header>
</template>

<script>
export default {
    name: 'BaseHeader',
    data(){
    return{
        NavBar: [
  {
    text: 'Characters',
    url: '#',
    current: false,
  },
  {
    text: 'Comics',
    url: '#',
    current: true,
  },
  {
    text: 'Movies',
    url: '#',
    current: false,
  },
  {
    text: 'TV',
    url: '#',
    current: false,
  },
  {
    text: 'Games',
    url: '#',
    current: false,
  },
  {
    text: 'Collectibles',
    url: '#',
    current: false,
  },
  {
    text: 'Videos',
    url: '#',
    current: false,
  },
  {
    text: 'Fans',
    url: '#',
    current: false,
  },
  {
    text: 'News',
    url: '#',
    current: false,
  },
  {
    text: 'Shop',
    url: '#',
    current: false,
  },
]

    }
    }
}
</script>

<style lang="scss" scoped>
    nav {
        display: flex;
        justify-content: space-between;
        padding: 1rem 0;

        img {
        max-height: 4rem;
        }

    }

    #nav-links {
      ul {
        height: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
      }
      li {
        color: #000;
        padding-right:  1rem;
        cursor: pointer;
        text-align: center;  
        
        &.active {
        border-bottom: 1px solid blue;
        }
        }
    }
</style>