<template>
    <div class="container">
                <div class="card card-default">
                    <div class="card-header">Create New Post</div>

                    <div class="card-body">
                        <form>
                            <div class="form-group">
                                <input type="text" name="" placeholder="Title..." class="form-control">
                            </div>
                            <div class="form-group">
                                <textarea rows="5" name="" placeholder="Description..." class="form-control"></textarea>
                            </div>
                            <router-link to="/" class="btn btn-warning">Cancel</router-link>
                            <button class="btn btn-success">Create</button>
                        </form>
                    </div>
                </div>
        </div>
</template>

<script>
    export default {
        mounted() {
            console.log('Component mounted.')
        }
    }
</script>
