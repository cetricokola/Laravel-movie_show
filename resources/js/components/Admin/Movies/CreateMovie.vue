<template>
    <div class="container">
        <h1 class="my-4">Create A Movie</h1>
        <div class="col-md-8">
            <form action="">
                <div class="mb-4">
                    <label for="name">Title of the Movie:</label>
                    <input type="text" id="name" class="form-control form-control-lg " v-model="name">
                </div>
                <div class="mb-4">
                    <label for="genre">Genre:</label>
                    <select name="" id="genre" class="form-control form-control-lg">
                        <option value="">1</option>
                    </select>
                </div>
                <div class="mb-4">
                    <label for="description">Description:</label>
                    <textarea type="text" id="description" class="form-control form-control-lg"
                              v-model="description"></textarea>
                </div>
                <button type="submit" class="btn btn-success">Submit</button>
            </form>
        </div>
        <div class="col-md-8">
            <h5 class="my-5">Add Actors</h5>
            <form action="">
                <div class="mb-4">
                    <label for="actor">Actors:</label>
                    <input type="text" id="actor" class="form-control form-control-lg " v-model="name">
                </div>
                <button class="btn btn-success">Add</button>
            </form>
        </div>
        <div>

            <div>
                <div class="h6 my-4 font-bold">
                    <p>Image Burner Upload</p>

                </div>
                <form @submit="formSubmit" enctype="multipart/form-data">
                    <div id="preview">
                        <img v-if="url" :src="url"/>
                    </div>
                    <div class="row">
                        <div class="col-md-6">
                            <input type="file" accept="image/*"
                                   class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
                                   v-on:change="onFileChange">
                        </div>
                        <div class="col-md-3">
                            <button
                                class="py-2 px-4 btn btn-success"
                                type="submit">Upload Movie Burner
                            </button>
                        </div>
                    </div>
                </form>
            </div>
        </div>
        <div>
            <div>
                <div class="h6 my-4 font-bold">
                    <p>Movie Trailer Upload</p>

                </div>
                <form @submit="formSubmit" enctype="multipart/form-data">
                    <div class="row">
                        <div class="col-md-6">
                            <input type="file" accept="video/*"
                                   class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
                                   v-on:change="onFileChange">
                        </div>
                        <div class="col-md-3">
                            <button
                                class="py-2 px-4 btn btn-success"
                                type="submit">Upload Movie Trailer
                            </button>
                        </div>
                    </div>
                </form>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "CreateMovie",
        data: () => {
            return {
                name: '',
                description: '',
                url: null,
            }
        },
        methods: {
            onFileChange(e) {
                this.file = e.target.files[0];
                this.url = URL.createObjectURL(this.file);
            },
            formSubmit(e) {
                e.preventDefault();
                const config = {
                    headers: {'content-type': 'multipart/form-data'}
                };
                // let formData = new FormData();
                // formData.append('file', this.file);
                // HTTP.post(`add_image/${this.new_project.id}`, formData, config)
                //     .then(function (response) {
                //         if (response.data.success) {
                //             swal(response.data.message);
                //             window.location.href = "/dashboard";
                //         } else {
                //             swal(response.data.error);
                //         }
                //     })
                //     .catch(function (error) {
                //         console.log(e)
                //     });
            }
        }
    }
</script>

<style scoped>

</style>
