<template>
    <div class="scrolldown-sign">
        <p class="scrolldown-sign__text">SCROLL</p>
        <div class="scrolldown-sign__line"></div>
    </div>
</template>

<script>
export default {
    name: 'ScrollDownSign',
    props: {},
    data () {
        return {
            
        }
    }
}
</script>

<style scoped lang="scss">
    .scrolldown-sign {
        width: 2rem;
        text-align: center;

        &__text {
            color: white;
            font-size: 1.6rem;
            width: 2rem;
            writing-mode: vertical-rl;
        }

        &__line {
            margin: 1rem auto;
            width: .1rem;
            height: 5rem;
            overflow: hidden;
            position: relative;

            &::after {
                content: "";
                position: absolute;
                width: 100%;
                height: 5rem;
                background-color: white;
                animation: infiniteGoDown 3s linear infinite;
            }
        }
    }
    @include lessThan(960px) {
        .scrolldown-sign {
            &__text {
                display: none;
            }
        }
    }
</style>
