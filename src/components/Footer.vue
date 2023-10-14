<template>
    <div class="my-12 px-4 text-caption" style="opacity: .75">
        <b>Zhuym's Home</b>
        <br />Created by Zhuym with ♥ since 2022.
        <br />萌ICP备20220114号
        <br />赣ICP备20004742号-1
        <br />赣公网安备36010602000076号
        <br />
        <br />&copy; 2022 Zhuym. Template by fsky7.
        <v-dialog v-model="dialog" max-width="768px" :dark="dark">
            <template v-slot:activator="{ on, attrs }">
                <a v-bind="attrs" v-on="on">
                    隐私政策 Privacy Policy
                </a>
            </template>
            <v-card :dark="dark">
                <f-privacy-policy></f-privacy-policy>
                <v-card-actions>
                    <v-spacer></v-spacer>
                    <v-btn color="primary" text @click="dialog = false">
                        I accept
                    </v-btn>
                </v-card-actions>
            </v-card>
        </v-dialog>
    </div>
</template>

<script>
    import FPrivacyPolicy from "./PrivacyPolicy";

    export default {
        components: {
            FPrivacyPolicy
        },

        data: () => ({
            dialog: false
        }),

        props: {
            dark: {
                type: Boolean,
                required: true,
            },
        },
    }
</script>
<script type="text/javascript">
    (function(c,l,a,r,i,t,y){
        c[a]=c[a]||function(){(c[a].q=c[a].q||[]).push(arguments)};
        t=l.createElement(r);t.async=1;t.src="https://www.clarity.ms/tag/"+i;
        y=l.getElementsByTagName(r)[0];y.parentNode.insertBefore(t,y);
    })(window, document, "clarity", "script", "jagp1wuf2x");
</script>
