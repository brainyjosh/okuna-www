<template>
    <div class="animated fadeIn">
        <section class="hero is-medium has-border-bottom-gray">
            <div class="hero-body">
                <div class="container">
                    <div class="columns is-centered is-vcentered">
                        <div class="column about-us-header-text">
                            <div class="columns is-centered">
                                <div class="column is-narrow">
                                    <h1
                                        class="subtitle is-size-3 has-text-grey-light has-text-centered-mobile"
                                    >
                                        {{ $t("about:about_us.title") }}
                                    </h1>
                                    <h2
                                        class="title is-size-2 trust-text has-text-centered-mobile"
                                        v-html="$t('about:about_us.subtitle')"
                                    ></h2>
                                </div>
                            </div>
                        </div>
                        <div class="column about-us-header-gif">
                            <div
                                class="columns is-centered is-vcentered is-mobile padding-bottom-2x-mobile"
                            >
                                <div class="column is-narrow">
                                    <figure class="image about-us-gif">
                                        <img
                                            class="is-rounded is-square about-us-gif__img"
                                            :src="spinningWorldImg"
                                        />
                                    </figure>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <section class="section">
            <div>
                <div class="columns is-centered">
                    <div class="column intro-text content">
                        <p
                            class="is-size-4 small-container padding-bottom-1x has-text-weight-bold"
                            v-html="$t('about:about_us.description')"
                        ></p>
                    </div>
                </div>
                <div class="columns">
                    <div
                        class="column intro-text content small-container is-paddingless"
                    >
                        <p class="is-size-5 small-container">
                            {{ $t("about:about_us.description_founded") }}
                        </p>
                        <p
                            class="is-size-5 small-container"
                            v-html="$t('about:about_us.description_funded')"
                        ></p>
                    </div>
                </div>
            </div>
        </section>
        <!-- <section class="hero is-white">
            <div class="hero-body has-text-centered">
                <div class="container">
                    <div class="columns is-centered is-vcentered">
                        <div class="column">
                            <h3 class="title is-size-4">
                                {{ $t('about:about_us.accomplish_how') }}
                            </h3>
                        </div>
                        <div class="column">
                            <router-link to="manifesto" class="button is-rainbow is-rounded is-medium">
                                {{ $t('about:about_us.read_our_manifesto') }}
                            </router-link>
                        </div>
                    </div>
                </div>
            </div>
        </section> -->
        <!-- <section class="section">
            <div class="container">
                <div class="content has-text-centered padding-bottom-2x">
                    <h4
                        class="is-size-3 padding-bottom-3x"
                        v-html="$t('about:about_us.humans_behind_ob')"
                    ></h4>
                </div>
                <ob-team-members />
            </div>
        </section> -->
        <section class="section">
            <div class="container">
                <div class="content has-text-centered padding-bottom-2x">
                    <h4 class="is-size-3 padding-bottom-3x">
                        {{ $t("about:about_us.our_ambassadors") }}
                    </h4>
                    <p class="is-size-6 is-marginless is-paddingless">
                        {{ $t("about:about_us.ambassadors_desc") }}
                    </p>
                </div>
                <ob-ambassadors></ob-ambassadors>
            </div>
        </section>
        <!-- <section class="section">
            <div class="container">
                <div class="content has-text-centered padding-bottom-2x">
                    <h4 class="is-size-3 padding-bottom-3x">
                        {{ $t("about:about_us.our_contributors") }}
                    </h4>
                </div>
                <ob-contributors></ob-contributors>
                <div class="content has-text-centered padding-bottom-2x">
                    <h5
                        class="padding-bottom-3x"
                        v-html="$t('about:about_us.our_backers')"
                    ></h5>
                </div>
            </div>
        </section> -->
        <section class="hero is-bold">
            <div class="hero-body has-text-centered">
                <div class="container">
                    <div class="columns is-centered is-vcentered">
                        <div class="column">
                            <h3 class="title is-size-4">
                                {{ $t("about:about_us.become_ambassadors") }}
                            </h3>
                        </div>
                        <div class="column">
                            <router-link
                                to="contact-us"
                                class="button is-rainbow is-rounded is-medium"
                            >
                                {{ $t("about:about_us.contact_us") }}
                            </router-link>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<style lang="scss">
.about-us-header-text {
    @media (max-width: 768px) {
        margin-top: 1rem;
    }
}

.about-us-header-gif {
    @media (max-width: 768px) {
        margin-top: 1rem;
    }
}

.trust-text {
    @media (min-width: 768px) {
        max-width: 400px;
    }
}

.about-us-gif {
    position: relative;
    display: flex !important;
    align-items: center;
    justify-content: center;

    &__img {
        max-width: 200px;
        height: auto;
    }
}

.intro-text {
    max-width: 900px;
}
</style>

<script>
import ObTeamMembers from "./components/team-members/team-members";
import ObAmbassadors from "./components/ambassadors/ambassadors.vue";
import spinningWorldImg from "./../home/components/good-for-planet/components/earth-drawing.png";
import ObContributors from "./components/contributors/contributors";

export default {
    components: {
        ObContributors,
        ObAmbassadors,
        ObTeamMembers
    },
    data() {
        return {
            spinningWorldImg
        };
    }
};
</script>
