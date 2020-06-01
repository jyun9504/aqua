<template>
  <header class="header">
    <a href="#" class="logo"><h1 class="logo__name">A qua</h1></a>
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

export default {
  name: 'Home',
  components: {
    NavBar,
    
  }
}
</script>

<style lang="scss" scoped>
    .header {
        background: url('../assets/images/wave-ocean.jpg');
        background-size: cover;
        background-position: center;
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
        padding: 9rem 0 0 12rem;
        animation: fadeInFromRight .8s linear;
        transition: all 2s;

        &--main {
            font-size: 3rem;
            font-weight: 100;
            letter-spacing: .1rem;
            line-height: 4rem;
        }

        &--sub {
            font-weight: 400;
            font-size: 1.5rem;
        }
    }

    .heading-secondary {
        color: #383838;
        padding: 10rem 0 0 15rem;
        width: 50rem;
        animation: fadeInFromRight 1.2s linear;
        transition: all 2s;

        &--main {
            font-weight: 400;
            font-size: 1.5rem;
        }
    }

    @include lessThan(960px){
        .heading-secondary {
            position: absolute;
            transform: translate(20px, 20px);
        }

        .heading-primary {
            transform: translate(50px, 50px);
        }
    }
</style>
