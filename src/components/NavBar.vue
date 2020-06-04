<template>
    <nav class="navbar" id="nav">
        <router-link to="/">
            Home
        </router-link>
        <router-link to="/shop">
            Shop
        </router-link>
        <router-link to="/about" >
            About
        </router-link>
        <router-link to="/contact">
            Contact
        </router-link>
     </nav>
</template>

<script>
export default {
    name: 'NavBar',
    props: {},
    data () {
        return {
            
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    
    .navbar {
        transition: all 1s;
        animation: fadeInFromRight 1s linear;

        a {
            letter-spacing: .4rem;
            font-size: 1.8rem;
            font-weight: 400;
            color: #2c3e50;
            text-decoration: none;
            margin: 0 5rem;
            position: relative;

            &::after {
                content: '';
                width: 100%;
                height: 100%;
                top: .7rem;
                left: -1.5rem;
                position: absolute;
                background:  url(../assets/images/active-icon.svg);  
                background-repeat: no-repeat;
                animation: fadeInFromTop .5s linear 1s both;
                visibility: hidden;
            }

            &.router-link-exact-active {
                color: #02696C;

                &::after {
                    visibility: visible;
                }
                
            }
        }
    }
    .active-icon {
        width: 10px;
        height: 10px;
        position: absolute;
    }

    @include lessThan(960px) {
       .navbar{
           display: none;
       }
    }

</style>
