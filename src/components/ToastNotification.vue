<template>
    <div class="baseDiv">
        <div v-for="(msg, index) in msgQueue" :key="index">
            <h1>{{msg}}</h1>
            <button @click="clearMessage(index)">Dismiss</button>
        </div>
        
    </div>
</template>

<script>
    export default {
        name : "ToastNotification",
        data() {
            return {
                msgQueue: []
            }
        },
        methods: {
            handleNotification(message) {
                this.msgQueue.push(message);
            },
            clearMessage(index){
                this.msgQueue.splice(index, 1);
            }
        },
        mounted () {
            this.$root.$on(`toastNotify`, this.handleNotification)
        },
    }
</script>

<style scoped>
.baseDiv{
    border: 2px dotted green;
    width: 20vw;
    position: fixed;
    right: 5px;
    top: 5px;
}

</style>