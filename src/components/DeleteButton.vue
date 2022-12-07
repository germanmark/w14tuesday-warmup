<template>
    <div>
        <button @click="toastNotify">Delete</button>
    </div>
</template>

<script>
    export default {
        name: "DeleteButton",
        data() {
            return {
                message: `Successfully deleted!`
            }
        },
        methods: {
            toastNotify() {
                this.$root.$emit(`toastNotify`, this.message)
            }
        },
    }
</script>

<style scoped>

</style>