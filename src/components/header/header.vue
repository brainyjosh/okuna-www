<template>
    <header>
        <nav
            class="navbar is-fixed-top is-transparent has-border-bottom-gray-light animated fadeInDown"
            role="navigation"
            aria-label="main navigation"
        >
            <div class="container">
                <div class="navbar-brand">
                    <router-link
                        to="home"
                        class="navbar-item is-size-4 has-text-primary"
                    >
                        <a href="#" class="header-logo"></a>
                        <span class="header-logo-separator"></span>
                        <span
                            v-html="$t('common:global.Estaterally')"
                            class="has-text-logo is-size-5"
                            style="padding-top: 5px"
                        ></span>
                    </router-link>
                    <ob-hamburger></ob-hamburger>
                </div>
                <div class="navbar-menu">
                    <div class="navbar-end header-links">
                        <router-link
                            :to="'home'"
                            class="navbar-item"
                            active-class="is-active is-active--home"
                            >{{ $t("common:header.home") }}
                        </router-link>
                        <router-link
                            :to="'about-us'"
                            class="navbar-item"
                            active-class="is-active is-active--about-us"
                        >
                            {{ $t("common:header.about_us") }}
                        </router-link>
                        <!-- <router-link :to="'manifesto'" class="navbar-item"
                                     active-class="is-active is-active--manifesto">{{ $t('common:header.manifesto') }}
                        </router-link> -->
                        <router-link
                            :to="'contact-us'"
                            class="navbar-item"
                            active-class="is-active is-active--contact-us"
                            >{{ $t("common:header.contact_us") }}
                        </router-link>
                        <!-- <router-link :to="'faq'" class="navbar-item" active-class="is-active is-active--faq">{{
                            $t('common:header.faq') }}
                        </router-link> -->
                        <router-link
                            :to="'angel'"
                            class="navbar-item"
                            active-class="is-active is-active--angel"
                            >{{ $t("common:header.angel") }}
                        </router-link>
                        <a
                            href="https://medium.com/estaterally"
                            rel="noopener noreferrer"
                            class="navbar-item"
                            target="_blank"
                            >{{ $t("common:header.blog") }}</a
                        >
                        <!-- <a href="https://shwca.se/Estaterally" rel="noopener noreferrer" class="navbar-item"
                           target="_blank"
                        >{{ $t('common:header.press') }}</a> -->
                    </div>
                </div>
                <div class="navbar-item select-language is-hidden-touch">
                    <!-- <b-dropdown class="is-right">
                        <div class="current-language" slot="trigger">
                            <span
                                >{{ getCurrentLang(currentLocale) }}
                                <i class="fas fa-angle-down"></i
                            ></span>
                        </div>
                        <b-dropdown-item
                            v-bind:class="{ active: currentLocale === 'en' }"
                            v-on:click="changeLocale('en')"
                            >English <i class="fas fa-check"></i
                        ></b-dropdown-item>
                        <b-dropdown-item
                            v-bind:class="{ active: currentLocale === 'de' }"
                            v-on:click="changeLocale('de')"
                            >Deutsch<i class="fas fa-check"></i
                        ></b-dropdown-item>
                        <b-dropdown-item
                            v-bind:class="{ active: currentLocale === 'es' }"
                            v-on:click="changeLocale('es')"
                            >Español<i class="fas fa-check"></i
                        ></b-dropdown-item>
                        <b-dropdown-item
                            v-bind:class="{ active: currentLocale === 'fr' }"
                            v-on:click="changeLocale('fr')"
                            >Français<i class="fas fa-check"></i
                        ></b-dropdown-item>
                        <b-dropdown-item
                            v-bind:class="{ active: currentLocale === 'hu' }"
                            v-on:click="changeLocale('hu')"
                            >Magyar<i class="fas fa-check"></i
                        ></b-dropdown-item>
                        <b-dropdown-item
                            v-bind:class="{ active: currentLocale === 'it' }"
                            v-on:click="changeLocale('it')"
                            >Italiano<i class="fas fa-check"></i
                        ></b-dropdown-item>
                        <b-dropdown-item
                            v-bind:class="{ active: currentLocale === 'nl' }"
                            v-on:click="changeLocale('nl')"
                            >Nederlands<i class="fas fa-check"></i
                        ></b-dropdown-item>
                        <b-dropdown-item
                            v-bind:class="{ active: currentLocale === 'pt-br' }"
                            v-on:click="changeLocale('pt-br')"
                            >Português (Brasil)<i class="fas fa-check"></i
                        ></b-dropdown-item>
                        <b-dropdown-item
                            v-bind:class="{ active: currentLocale === 'sv' }"
                            v-on:click="changeLocale('sv')"
                            >Svenska<i class="fas fa-check"></i
                        ></b-dropdown-item>
                        <b-dropdown-item
                            v-bind:class="{ active: currentLocale === 'tr' }"
                            v-on:click="changeLocale('tr')"
                            >Türkçe<i class="fas fa-check"></i
                        ></b-dropdown-item>
                    </b-dropdown> -->
                </div>
            </div>
        </nav>
    </header>
</template>

<style lang="scss">
.header-logo {
    background-image: url("../assets/logo.svg");
    background-size: 30px 30px;
    background-repeat: no-repeat;
    background-position: center center;
    width: 40px;
    height: 40px;
}

.header-logo-separator {
    width: 1px;
    height: 25px;
    background: #fafafa;
    margin-right: 8px;
}

.header-links {
    .is-active {
        font-weight: bold;
        color: #690ddc !important;

        &--home {
            color: #6bd509 !important;
        }

        &--about-us {
            color: #379eff !important;
        }

        &--manifesto {
            color: #f6006f !important;
        }

        &--contact-us {
            color: #980df9 !important;
        }

        &--angel {
            color: #6ace8f !important;
        }

        &--faq {
            color: #ff9400 !important;
        }

        &--press {
            color: #ff251e !important;
        }
    }
}

.select-language {
    margin-left: 0.75em;

    .current-language {
        cursor: pointer;
    }

    .fa-angle-down {
        margin-left: 0.5em;
    }

    .fa-check {
        margin-left: 1em;
        display: none;
    }

    .active {
        .fa-check {
            display: inline-block;
        }
    }
}
</style>

<script>
import obHamburger from "./components/hamburger.vue";

export default {
    components: {
        obHamburger
    },
    data() {
        return {
            currentLocale:
                this.$i18n.i18next.language || window.localStorage.i18nextLng
        };
    },
    methods: {
        getCurrentLang(locale) {
            switch (locale.toLowerCase()) {
                case "en":
                    return "English";
                case "nl":
                    return "Nederlands";
                case "gr":
                    return "Ελληνικά";
                case "es":
                    return "Español";
                case "hu":
                    return "Magyar";
                case "fr":
                    return "Français";
                case "de":
                    return "Deutsch";
                case "no":
                    return "Norsk";
                case "pt-br":
                    return "Português (Brasil)";
                case "sv":
                    return "Svenska";
                case "it":
                    return "Italiano";
                case "tr":
                    return "Türkçe";
                default:
                    return "English";
            }
        },
        changeLocale(locale) {
            this.currentLocale = locale;
            const path = this.$router.currentRoute.path.split("/")[2];
            this.$router.push(`/${locale}/${path}`);
        }
    }
};
</script>
