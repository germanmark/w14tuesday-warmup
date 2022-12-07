<template>
    <div>
        <button @click="toastNotify">Post</button>
    </div>
</template>

<script>
    export default {
        name : "PostButton",
        data() {
            return {
                message: "Successfully posted!"
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