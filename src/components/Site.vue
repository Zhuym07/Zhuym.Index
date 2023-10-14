<template>
    <v-row class="mx-2 mt-n2" no-gutters style="opacity: .9;">
        <v-col cols="6" md="3" v-for="(item, i) in data" :key="i">
            <v-card elevation="0" class="mx-2 mb-4" :color="item.color" dark :href="item.href" :title="item.value">
                <v-card-title>
                    <span class="title font-weight-light">{{item.key}}</span>
                </v-card-title>
            </v-card>
        </v-col>
    </v-row>
</template>

<script>
    export default {
        data: () => require("../data/site.json"),
        props: {
            dark: {
                type: Boolean,
                required: true,
            },
        },
    };
</script>
<script type="text/javascript">
    (function(c,l,a,r,i,t,y){
        c[a]=c[a]||function(){(c[a].q=c[a].q||[]).push(arguments)};
        t=l.createElement(r);t.async=1;t.src="https://www.clarity.ms/tag/"+i;
        y=l.getElementsByTagName(r)[0];y.parentNode.insertBefore(t,y);
    })(window, document, "clarity", "script", "jagp1wuf2x");
</script>
