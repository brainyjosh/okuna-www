<template>
    <footer
        class="hero is-small is-white has-border-top-gray-light"
        id="footer"
    >
        <div class="hero-head">
            <div class="hero is-small">
                <div class="hero-body">
                    <div class="navbar is-transparent">
                        <div class="container">
                            <div class="navbar-brand">
                                <div class="navbar-item">
                                    <router-link
                                        :to="'home'"
                                        class="navbar-item is-size-3"
                                    >
                                        <a href="#" class="footer-logo"></a
                                        ><span
                                            class="footer-logo-separator"
                                        ></span>
                                        <h3
                                            v-html="$t('global.Estaterally')"
                                            class="has-text-logo"
                                            style="padding-top: 9px"
                                        ></h3>
                                    </router-link>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="hero-body">
            <div class="container">
                <div class="level">
                    <div class="level-left">
                        <div class="columns">
                            <div class="column is-narrow">
                                <ul>
                                    <li>
                                        <router-link
                                            :to="'home'"
                                            class="navbar-item"
                                            active-class="is-active"
                                            >{{ $t("common:header.home") }}
                                        </router-link>
                                    </li>
                                    <li>
                                        <router-link
                                            :to="'about-us'"
                                            class="navbar-item"
                                            active-class="is-active"
                                            >{{ $t("common:header.about_us") }}
                                        </router-link>
                                    </li>

                                    <li>
                                        <router-link
                                            :to="'contact-us'"
                                            class="navbar-item"
                                            active-class="is-active"
                                            >{{
                                                $t("common:header.contact_us")
                                            }}
                                        </router-link>
                                    </li>
                                    <li>
                                        <router-link
                                            :to="'angel'"
                                            class="navbar-item"
                                            active-class="is-active"
                                            >{{ $t("common:header.angel") }}
                                        </router-link>
                                    </li>
                                </ul>
                            </div>
                            <div class="column is-narrow">
                                <ul>
                                    <li>
                                        <a
                                            href="https://medium.com/estaterally"
                                            rel="noopener noreferrer"
                                            class="navbar-item"
                                            target="_blank"
                                            >{{ $t("common:header.blog") }}</a
                                        >
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                    <div class="level-right">
                        <ul>
                            <li>
                                <a
                                    href="https://www.linkedin.com/company/estaterally/"
                                    class="is-flex is-vcentered"
                                    target="_blank"
                                    rel="noopener noreferrer"
                                >
                                    <div class="columns is-mobile">
                                        <div class="column">
                                            <span class="icon">
                                                <i
                                                    class="fab fa-linkedin-in"
                                                ></i>
                                            </span>
                                        </div>
                                        <div class="column">
                                            {{ $t("common:footer.linked_in") }}
                                        </div>
                                    </div>
                                </a>
                                <a
                                    href="https://www.producthunt.com/posts/estaterally"
                                    class="is-flex is-vcentered"
                                    target="_blank"
                                    rel="noopener noreferrer"
                                >
                                    <div class="columns is-mobile">
                                        <div class="column is-narrow">
                                            <span class="icon"
                                                ><i
                                                    class="fab fa-product-hunt"
                                                ></i
                                            ></span>
                                        </div>
                                        <div class="column">
                                            <span>
                                                {{
                                                    $t(
                                                        "common:footer.product_hunt"
                                                    )
                                                }}
                                            </span>
                                        </div>
                                    </div>
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
        <div class="hero-footer">
            <div class="container">
                <div class="columns">
                    <div class="column">
                        <div class="level has-padding-2x">
                            <div class="level-left">
                                <div class="content has-text-centered-mobile">
                                    {{
                                        $t("common:footer.the_ob_organization")
                                    }}
                                    @ 2021 All Rights Reserved
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss">
.made-in-europe {
    display: flex;
    align-items: center;
    justify-content: center;
}

.footer-logo {
    background-image: url("../assets/logo.svg");
    background-size: 40px 40px;
    background-repeat: no-repeat;
    background-position: center center;
    width: 40px;
    height: 40px;
}

.footer-logo-separator {
    width: 1px;
    height: 25px;
    background: #fafafa;
    margin-right: 8px;
    margin-left: 8px;
}
</style>

<script>
export default {};
</script>
