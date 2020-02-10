<template>
    <div>
        <div class="row">
            <button @click="selectedComponent = 'CreateActor'" class="btn-success btn">Create</button>
        </div>
        <div class="mt-4">
            <component :is="selectedComponent"/>
        </div>
    </div>
</template>

<script>
    export default {
        name: "ManageActors",
        components: {
            CreateActor: () => import('./Actor/CreateActor'),
        },
        data: () => {
            return {
                selectedComponent: ' CreateActor'
            }
        },
    }
</script>

<style scoped>

</style>
