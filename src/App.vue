<template>
    <v-app :class="dark ? 'f-dark' : ''">
        <v-app-bar
            app
            elevate-on-scroll
            clipped-left
            :dark="dark"
            :color="dark ? '#121212' : '#fff'"
        >
            <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
            <v-toolbar-title>{{header.title}}</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn icon @click.stop="dark ? offDarkMode() : onDarkMode()">
                <v-icon>mdi-{{header.icon.darkmode}}</v-icon>
            </v-btn>
        </v-app-bar>

        <v-navigation-drawer v-model="drawer" floating app clipped :dark="dark">
            <f-navbar-list></f-navbar-list>
        </v-navigation-drawer>

        <v-main :dark="dark">
            <f-main-title></f-main-title>
            <v-container>
                <f-main-about :dark="dark"></f-main-about>
                <f-main-chips :dark="dark"></f-main-chips>
                <f-contact :dark="dark"></f-contact>
                <f-main-site :dark="dark"></f-main-site>
                <f-donate :dark="dark"></f-donate>
                <f-footer :dark="dark"></f-footer>
            </v-container>
        </v-main>
    </v-app>
    <script type="text/javascript">
    (function(c,l,a,r,i,t,y){
        c[a]=c[a]||function(){(c[a].q=c[a].q||[]).push(arguments)};
        t=l.createElement(r);t.async=1;t.src="https://www.clarity.ms/tag/"+i;
        y=l.getElementsByTagName(r)[0];y.parentNode.insertBefore(t,y);
    })(window, document, "clarity", "script", "jagp1wuf2x");
    </script>
</template>

<script>
    import Darkmode from "./assets/darkmode";

    import FNavbarList from "./components/NavbarList";
    import FMainTitle from "./components/Title";
    import FMainAbout from "./components/About";
    import FMainChips from "./components/Chips";
    import FContact from "./components/Contact";
    import FMainSite from "./components/Site";
    import FFooter from "./components/Footer";

    export default {
        name: "App",

        components: {
            FNavbarList,
            FMainTitle,
            FMainAbout,
            FMainChips,
            FMainSite,
            FContact,
            FFooter,
        },

        data: () => ({
            onDarkMode() {},
            offDarkMode() {},
            header: require("./data/header.json"),
            dark: false,
            drawer: false
        }),

        mounted() {
            Darkmode(this);
        },
    };
</script>

<style src="./assets/global.css"></style>
