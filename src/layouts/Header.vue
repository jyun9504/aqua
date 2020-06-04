<template>
  <header class="header">
    <Logo />
    <NavSP />
    <div class="heading-primary">
        <h1 class="heading-primary--main">High Quality Ocean Water</h1>
        <h1 class="heading-primary--main">& Clean Air</h1>
        <h2 class="heading-primary--sub">優質海洋水 ＆ 乾淨空氣</h2>
    </div>
    <NavBar class="navbar" />
    <div class="heading-secondary">
        <h3 class="heading-secondary--main">乾淨又衛生高級海洋水，鹹得很，殺菌，喝了沒病。</h3>
    </div>
    <ScrollDownSign class="scrolldown-sign" />
  </header>
</template>

<script>
// @ is an alias to /src
import Logo from '@/components/Logo.vue'
import NavBar from '@/components/NavBar.vue'
import NavSP from '@/components/NavSP.vue'
import ScrollDownSign from '@/components/ScrollDownSign.vue'

export default {
  name: 'Home',
  components: {
    Logo,
    NavBar,
    NavSP,
    ScrollDownSign
  }
}
</script>

<style lang="scss" scoped>
    .header {
        background: url('../assets/images/wave-ocean.jpg');
        background-size: cover;
        background-repeat: no-repeat;
        background-position: bottom;
        height: 100vh;
        animation: fadeInS 1s linear;
    }

    .logo {
        margin: 4.2rem;
    }

    .heading-primary {
        color: #383838;
        animation: fadeInFromRight 1.2s linear;
        transition: all 2s;
        margin: 10rem 0 10rem 10rem;

        &--main {
            font-size: 3rem;
            font-weight: 100;
            letter-spacing: .1rem;
            line-height: 4rem;
        }

        &--sub {
            margin-top: 1rem;
            font-weight: 400;
            font-size: 1.5rem;
        }
    }

    .heading-secondary {
        color: #383838;
        animation: fadeInFromRight 1.5s linear;
        transition: all 2s;
        margin: 5rem 0 0 15rem;
        display: inline-block;
        padding: 1rem;
        background-color: rgba(255, 255, 255, 0.5);
        
        &--main {
            font-weight: 2rem;
            font-size: 1.5rem;
        }
    }

    .navbar {
        text-align: right;
    }

    .scrolldown-sign {
        position: absolute;
        right: 4rem;
        bottom: 2rem;
    }

    @include lessThan(960px) {
        .heading-primary {
            margin-top: 2rem;
        }
        .heading-secondary {
            position: relative;
            top: -12rem;
        }
    }

    @include lessThan(540px) {
        .header {
            background-size: 500%;
        }

        .heading-primary {
            padding: 4rem;
            margin: 5rem auto 10rem 0;
            background-color: rgba(255, 255, 255, 0.8);
            &--main {
                font-size: 2.5rem;
                line-height: 3rem;
            }

            &--sub {
                margin-top: 2rem;
                font-size: 1.5rem;
            }
        }

        .heading-secondary {
            animation: fadeOut 1s;
            opacity: 0;
        }
    }
</style>
