<template>
    <div class="ads-free-symbol">
        <Investor />
    </div>
</template>

<style lang="scss">
.ads-free-symbol {
    img {
        width: 140px !important;
        height: auto !important;
    }
}
</style>

<script>
import Investor from "./investor.vue";
export default {
    name: "ob-sunglasses",
    data() {
        return {
            Investor: Investor
        };
    }
};
</script>
