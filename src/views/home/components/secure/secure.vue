<template>
    <section class="section">
        <div>
            <div class="container">
                <div class="columns is-height-100 has-reverse-row-order-mobile">
                    <div class="column">
                        

                        <div class="column padding-top-2x-mobile">
                            <div class="columns is-centered is-vcentered is-height-100 is-mobile">
                                <div class="column is-10">
                                    <ob-secure-icon></ob-secure-icon>
                                </div>
                            </div>
                        </div>

                    </div>
                    <div class="column">
                        <div class="columns is-centered is-vcentered is-height-100 is-mobile">
                            <div class="column content is-medium secure-text">
                                <h3>{{ $t('home:secure.title') }}</h3>
                                <p>
                                    {{ $t('home:secure.description') }}
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss">

    .secure-text {
        @media (min-width: 768px) {
            max-width: 400px;
        }
    }

    .secure-heart {

    }
</style>

<script>
    import ObCuteRobot from "../../../../components/cute-robot.vue";
    import ObSecureIcon from "./components/secure-icon.vue";

    export default {
        components: {
            ObSecureIcon,
            ObCuteRobot
        },
        name: 'ob-secure'
    }
</script>

