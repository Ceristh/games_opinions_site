<template>
    <div class="container mt-5">
        <div class="row">
            <Card
                v-for="(game, i) in games"
                :key="i"
                :id="game.id"
                :backgroundImage="game.background_image"
                :name="game.name"
                :rating="game.rating"
                :released="game.released"
                :updated="game.updated"
                class="col-md-4"
            ></Card>
        </div>
    </div>
</template>

<script>
import Card from "@/components/Card.vue";
import { mapState } from "vuex";
export default {
    name: "component-name",
    data: function () {
        return {};
    },
    computed: {
        ...mapState(["games"]),
    },
    methods: {
        fetchGames() {},
    },
    components: {
        Card,
    },
    created() {
        this.fetchGames();
    },
};
</script>