<template>
    <div>
        <div class="col-md-8">
            <form action="">
                <div class="mb-4">
                    <label for="name">Name:</label>
                    <input type="text" id="name" class="form-control form-control-lg " v-model="name">
                </div>

                <button type="submit" class="btn btn-success">Submit</button>
            </form>
        </div>
    </div>
</template>

<script>
    export default {
        name: "CreateGenre",
        data: ()=>{
            return {
                name: ''
            }
        }
    }
</script>

<style scoped>

</style>
