<template>
    <address>
        <div class="columns is-vcentered is-multiline is-mobile">
            <div class="column is-2">
                <span class="icon">
                    <i class="fas fa-building"></i>
                </span>
            </div>
            <div class="column is-10">
                <strong>{{ $t("contact:address.name") }}</strong
                ><br />
                {{ $t("contact:address.ob_organization") }}
            </div>
            <div class="column is-2">
                <span class="icon">
                    <i class="fas fa-map-marker-alt"></i>
                </span>
            </div>
            <div class="column is-10">
                <strong>{{ $t("contact:address.address") }}</strong
                ><br />
                {{ $t("contact:address.ob_address") }}
            </div>
            <div class="column is-2">
                <span class="icon">
                    <i class="fas fa-envelope"></i>
                </span>
            </div>
            <div class="column is-10">
                <strong>{{ $t("contact:address.email") }}</strong
                ><br />
                <a href="mailto:info@Estaterally.io">
                    info@estaterally.com
                </a>
            </div>
            <div class="column is-2">
                <span class="icon">
                    <i class="fas fa-globe"></i>
                </span>
            </div>
            <div class="column is-10">
                <strong>{{ $t("contact:address.website") }}</strong
                ><br />
                <a
                    href="https://about.estaterally.com"
                    target="_blank"
                    rel="noopener noreferrer"
                >
                    about.estaterally.com
                </a>
            </div>
        </div>
    </address>
</template>

<script>
export default {
    name: "ob-address"
};
</script>
