<template>
    <figure class="image">
        <img
            class="personal-preview"
            style="border-radius:16px;"
            :src="image"
            alt="Phone with personal features preview"
        />
    </figure>
</template>


<style lang="scss">
    .heart {
        width: 150px;
        height: 90px;

        // &:before,
        // &:after {
        //     content: '';
        //     position: absolute;
        //     top: 0;
        //     background: #fc2e5a;

        //     width: 50px;
        //     height: 80px;
        //     border-radius: 50px 50px 0 0;
        // }

        // &:before {
        //     left: 50px;
        //     transform: rotate(-45deg);
        //     transform-origin: 0 100%;
        // }

        // &:after {
        //     left: 0;
        //     transform: rotate(45deg);
        //     transform-origin: 100% 100%;
        // }

    }

    .heart-main {
        animation: pounding 1.8s linear infinite alternate;
    }

    @keyframes pounding {
        0% {
            transform: scale(1.5);
        }
        100% {
            transform: scale(1);
        }
    }

    @keyframes heart-anim {
        46% {
            transform: scale(1);
        }
        50% {
            transform: scale(1.3);
        }
        52% {
            transform: scale(1.5);
        }
        55% {
            transform: scale(3);
        }
        100% {
            opacity: 0;
            transform: scale(50);
        }
    }
</style>

<script>
import image from "../estaterally-chat.png";
    export default {
        name: 'ob-heart',
        data() {
                return {
                    image: image
                };
            }
    }
</script>
