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

    .security-icon{
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        
    }

    .face {
        width: 9rem;
        height: 9rem;
        border-radius: 100%;
        background-color: #e8e8e8;
        background-size: cover;
        animation: face 3s infinite ease;
        position: relative;
    }

    .face:before {
        position: absolute;
        height: 100%;
        width: 100%;
        background-color: #cacaca;
        content: '';
        border-radius: 100%;
        animation: radar 3s infinite ease;
        z-index: -1;
        opacity: .2;
    }

    @keyframes face {
        0% {
            transform: scale(1);
        }

        50% {
            transform: scale(1.05);
        }

        100% {
            transform: scale(1);
        }
    }

    @keyframes radar {
        0% {
            transform: scale(1);
            opacity: 0;
        }

        60% {
            opacity: .2;
        }

        100% {
            transform: scale(1.6);
            opacity: 0;
        }
    }

</style>

<script>
import image from "../estaterally-listed-property.png";
    export default {
        name: 'ob-secure-icon',
         data() {
                return {
                    image: image
                };
            }
    }
</script>
