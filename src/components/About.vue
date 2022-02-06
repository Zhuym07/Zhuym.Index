<template>
    <v-card class="pt-4" :dark="dark" elevation="0" style="background: none;">
        <v-list-item>
            <v-list-item-content>
                <v-list-item-title class="headline">关于我</v-list-item-title>
                <v-list-item-subtitle>About ME</v-list-item-subtitle>
            </v-list-item-content>
        </v-list-item>
        <v-card-text class="f-text" style="max-width: 400px;">
            这里是 Zhuym
            <br /><br />
            只是一个学生，喜欢整点无聊的小东西和设计
            会一些安卓方面的搞机技能，会把自己感兴趣的东西研究的很彻底
            更喜欢研究某些东西的本质，并从中学到知识，运用到其他地方
        </v-card-text>
    </v-card>
</template>

<script>
    export default {
        props: {
            dark: {
                type: Boolean,
                required: true,
            },
        },
    };
</script>