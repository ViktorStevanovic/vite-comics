<template lang="">
    <main>
        <section class='upper-main'>
            <div class="wrapper">
                <section>
                    <h1>Content goes here</h1>
                </section>
            </div>          
        </section>
        <section class='lower-main'>
            <div class="wrapper">
                <section>
                    <h1>Content goes here</h1>
                </section>
            </div>          
        </section>
        
    </main>
</template>
<script>
export default {
    
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;
main{
    width: 100%;
    .upper-main{
        background-color: $bg-gray;
    }
    .lower-main{
        background-color: $color-blue;
    }
    .wrapper{
        // width: 100%;
        section{
            margin: 0 auto;
    
            h1{
                color: white;
                padding: 3rem 0;
                font-size: 2rem;
            }
        }
    }
}   
</style>