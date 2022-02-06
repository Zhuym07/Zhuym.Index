<template>
    <div class="my-12 px-4 text-caption" style="opacity: .75">
        <b>Zhuym's Home</b>
        <br />Created by Zhuym with ♥ since 2022.
        <br /><a href="https://icp.gov.moe/?keyword=20220114" target="_blank">萌ICP备20220114号</a>
        <br /><a href="https://beian.miit.gov.cn/#/Integrated/index" target="_blank">赣ICP备20004742号-1</a>
        <br /><a href="http://www.beian.gov.cn/portal/registerSystemInfo?recordcode=36010602000076" target="_blank">赣公网安备36010602000076号</a>
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