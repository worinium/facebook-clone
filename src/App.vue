<template>
<v-app>
    <Toolbar />
    <DrawerLeft />
    <DrawerRight />

    <v-main>
        <Feed />
    </v-main>
</v-app>
</template>

<script>
import Toolbar from './components/ToolBar'
import DrawerLeft from './components/DrawerLeft'
import DrawerRight from './components/DrawerRight'
import Feed from './components/UpdateFeeds'

export default {
    name: 'App',
    components: {
        Toolbar,
        DrawerLeft,
        DrawerRight,
        Feed
    },
    data: () => ({
        //
    }),
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Questrial");

.questrial {
    font-family: "Questrial";
}
</style>
