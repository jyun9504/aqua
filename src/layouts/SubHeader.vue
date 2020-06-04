<template>
    <header class="sub-header">
        <Logo class="logo" />
        <NavSP />
        <div class="heading-primary">
            <h1 class="heading-primary--main">High Quality Ocean Water</h1>
            <h1 class="heading-primary--main">& Clean Air</h1>
            <h2 class="heading-primary--sub">優質海洋水 ＆ 乾淨空氣</h2>
        </div>
        <NavBar class="navbar" />
    </header>
</template>

<script>
// @ is an alias to /src
import Logo from '@/components/Logo.vue'
import NavBar from '@/components/NavBar.vue'
import NavSP from '@/components/NavSP.vue'

export default {
  name: 'SubHeader',
  components: {
    Logo,
    NavBar,
    NavSP    
  }
}
</script>

<style lang="scss" scoped>

    .logo {
        margin: 4.2rem;
    }

    .heading-primary {
        color: #383838;
        animation: fadeIn 1s linear;
        transition: all 2s;
        margin: 5rem 0 15rem 10rem;

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

    .navbar {
        text-align: right;
    }
    
    @include lessThan(960px) {
        .heading-primary {
            margin-top: 2rem;
        }
    }

    @include lessThan(540px) {
        .header {
            background-size: 400%;
        }

        .heading-primary {
            padding: 4rem;
            margin: 5rem auto 10rem 0;
            
            &--main {
                font-size: 2.5rem;
                line-height: 3rem;
            }

            &--sub {
                margin-top: 2rem;
                font-size: 1.5rem;
            }
        }
    }
</style>
