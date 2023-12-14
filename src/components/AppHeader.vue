<template lang="">
    <header>
        <div class="wrapper">
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="DC comics header logo">
            </div>
            <section class="navigation">
                <ul>
                    <li v-for='link in navLinks'>{{ link.name }}</li>
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
    img{
        width: 80%
    }
    .wrapper{
        @include flex(row, space-between,center);
        ul{
            @include flex(row,center,center);
            gap: 1rem;
            list-style: none;
            li{
                padding: 3rem 1rem;
            }
        }
    }
}
    
</style>