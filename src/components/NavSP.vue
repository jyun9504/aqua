<template>
    <nav class="nav-sp">
        <a class="menu-btn" :class="{'menu-btn--active': isActive}" href="#" @click="toggleMenu">
            <span></span>
            <span></span>
        </a>
        <div class="menu" v-show="this.isActive">
            <nav class="menu__list" id="nav">
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
        </div>
    </nav>
</template>

<script>
export default {
    data() {
        return {
            isActive: false
        }
    },
    methods: {
        toggleMenu() {
            this.isActive = !this.isActive;
        }
    }
}
</script>

<style lang="scss" scoped>
    .nav-sp {
        display: none;
    }

    .menu-btn {
        position: absolute;
        top: 4.7rem;
        right: 5rem;
        height: 2.5rem;
        width: 3rem;
        z-index: 99;

        & span {
            position: absolute;
            width: 100%;
            height: 1px;
            background-color: #20797B;
            transition: all .5s;
        }

        & span:nth-of-type(2){
            top: 1rem;
        }

        &--active {
            span:nth-of-type(1) {
                transform: rotate(45deg) translateX(.7rem);
            }
            span:nth-of-type(2) {
                transform: rotate(-45deg) translateX(.7rem);
            }
        }
    }

    .menu {
        position: absolute;
        width: 100%;
        background-color: rgba(255, 255, 255, .95);
        animation: fadeIn .5s linear;
        z-index: 999;

        &__list {
            text-decoration: none;
            padding-left: 10rem;

            a {
                display: block;
                font-size: 2rem;
                color: #2c3e50;
                text-decoration: none;
                margin: 5rem 0;
                position: relative;
                animation: fadeInFromBottom .5s linear both;

                &:nth-of-type(2) {
                    animation-delay: .1s;
                }
                
                &:nth-of-type(3) {
                    animation-delay: .2s;
                }

                &:nth-of-type(4) {
                    animation-delay: .3s;
                }

                &::after {
                    content: '';
                    width: 100%;
                    height: 100%;
                    top: .6rem;
                    left: -4rem;
                    position: absolute;
                    background:  url(../assets/images/active-icon.svg);  
                    background-repeat: no-repeat;
                    animation: fadeInFromTop .5s linear;
                    visibility: hidden;
                }

                &.router-link-exact-active {

                    &::after {
                        visibility: visible;
                    }
                    
                }
            }
        }
    }

    @include lessThan(960px) {
        .nav-sp {
            display: inherit;
        }
    }
</style>
