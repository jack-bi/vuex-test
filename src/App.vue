<template>
    <div id="app">
        <HelloWorld />
    </div>
</template>

<script>
import HelloWorld from "./component/HelloWorld";

export default {
    name: "App",
    components: {
        HelloWorld,
    },
};
</script>

<style>
#app {}
</style>