<template>
  <header class="header">
    <a href="#" class="logo"><h1 class="logo__name">A qua</h1></a>
    <NavSP />
    <div class="heading-primary">
        <h1 class="heading-primary--main">High Quality Ocean Water</h1>
        <h1 class="heading-primary--main">& Clean Air</h1>
        <h2 class="heading-primary--sub">優質海洋水 ＆ 乾淨空氣</h2>
    </div>
    <NavBar />
    <div class="heading-secondary">
        <h3 class="heading-secondary--main">乾淨又衛生高級海洋水，鹹得很，殺菌，喝了沒病。</h3>
    </div>
  </header>
</template>

<script>
// @ is an alias to /src
import NavBar from '@/components/NavBar.vue'
import NavSP from '@/components/NavSP.vue'

export default {
  name: 'Home',
  components: {
    NavBar,
    NavSP    
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
        text-align: left;
        animation: fadeIn 1s linear;
    }

    .logo {
        display: inline-block;
        text-decoration: none;
        color: #02696C;
        margin: 4.2rem;
        animation: fadeIn .8s linear;

        &__name {
            text-transform: uppercase;
            font-size: 2rem;
           
        }
    }

    .heading-primary {
        color: #383838;
        animation: fadeInFromRight .8s linear;
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
        animation: fadeInFromRight 1.2s linear;
        transition: all 2s;
        margin: 5rem 0 0 15rem;
        display: inline-block;
        padding: 1rem;
        background-color: #A6D7DE;
        
        &--main {
            font-weight: 2rem;
            font-size: 1.5rem;
        }
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
            background-size: 400%;
        }

        .heading-primary {
            text-align: center;
            padding: 1rem;
            margin: 10rem auto;
            
            &--main {
                font-size: 3rem;
                line-height: 3.5rem;
            }

            &--sub {
                margin-top: 2rem;
                font-size: 2rem;
            }
        }

        .heading-secondary {
            animation: fadeOut 1s;
            opacity: 0;
        } 
    }
</style>
