<template>
    <div>
        <h1>Error 404 Not Found</h1>
        <button @click="redirectHome">Regresar</button>
    </div>
</template>

<script>
export default {
    methods: {
        redirectHome() {
            this.$router.push("/");
        },
    },
};
</script>