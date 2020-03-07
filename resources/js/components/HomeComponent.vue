<template>
    <b-row>
        <b-col>
            <b-card header="Home Component">
                <b-card-text>
                    I'm the Home Component component.
                </b-card-text>
            </b-card>
        </b-col>
    </b-row>
</template>

<script>
    export default {
        mounted() {
            console.log('Home Component mounted');
        },
        name: "HomeComponent"
    }
</script>

<style scoped>

</style>
