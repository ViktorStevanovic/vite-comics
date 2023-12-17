<template lang="">
    <header>
        <div class="wrapper">
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="DC comics header logo">
            </div>
            <section class="navigation">
                <ul>
                    <li v-for='link in navLinks' :class="(link.active) ? 'active' : ''">{{ link.name }} </li>
                </ul>
            </section>
        </div>
    </header>
    
</template>
<script>
export default {
    data() {
        return {
            name: 'AppHeader',
            navLinks: [
                {
                    name: 'Characters',
                    url: '#',
                    active: false
                },
                {
                    name: 'Comics',
                    url: '#',
                    active: true
                },
                {
                    name: 'Movies',
                    url: '#',
                    active: false
                },
                {
                    name: 'Tv',
                    url: '#',
                    active: false
                },
                {
                    name: 'Games',
                    url: '#',
                    active: false
                },
                {
                    name: 'Collectibles',
                    url: '#',
                    active: false
                },
                {
                    name: 'Videos',
                    url: '#',
                    active: false
                },
                {
                    name: 'Fans',
                    url: '#',
                    active: false
                },
                {
                    name: 'News',
                    url: '#',
                    active: false
                },
                {
                    name: 'Shop',
                    url: '#',
                    active: false
                }
            ]
        }
    },
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;
header{
    width: 100%;
    position: fixed;
    background-color: $bg-white;
    img{
        width: 70px;
    }
    .wrapper{
        @include flex(row, space-between,center);
        div{
            @include flex(row, space-between,center);
        }
        ul{
            @include flex(row,center,center);
            gap: 2rem;
            list-style: none;
            li{
                padding: 2rem 0rem;
                text-transform: uppercase;
                font-size: .8rem;
            }
        }
    }
}
    
</style>