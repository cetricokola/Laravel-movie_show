<template>
    <div>
        <h1 class="my-4 text-primary">Admin Dashboard</h1>
        <div class="col-md-8 mb-4 card p-4 ml-auto mr-auto">
            <h3>Movies</h3>
            <h3>Active subscriptions</h3>
            <h3>Active Customers</h3>
        </div>
        <hr>
        <div class="row mb-4 ml-auto mr-auto">
            <div class="col-md-4 card m-3 ">
                Create a movie
                <button class="btn btn-success text-capitalize">Create</button>
            </div>
            <div class="col-md-3  card my-3 mr-3">
                Manage Movies
                <button class="btn btn-success text-capitalize">Manage</button>
            </div>
            <div class="col-md-4 card my-3 ">
                Subscriptions
                <button class="btn btn-success text-capitalize">Subscriptions</button>
            </div>
        </div>
        <hr>
        <div
            class="ml-auto mr-auto justify-contents-between row col-md-6 font-weight-bold h5 border p-3 rounded-border">
            <div class="col-md-6 text-center">
                <a href=""><p>View Movies</p></a>
            </div>
            <div class="col-md-6 text-center">
                <a href=""><p>View Customers</p></a>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "dashboard"
    }
</script>

<style scoped>
    .card {
        height: 200px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 30px;
    }

    .rounded-border {
        border-radius: 25px;

    }

    .btn {
        border-radius: 25px;
    }
</style>
