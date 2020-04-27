<template>
    <div class="container">
                <div class="card card-default">
                    <div class="card-header">Create New Post</div>

                    <div class="card-body">
                        <form v-on:submit="submitPost()">
                            <div class="form-group">
                                <input type="text" v-model="posts.title" placeholder="Title..." class="form-control">
                            </div>
                            <div class="form-group">
                                <textarea rows="5" v-model="posts.description" placeholder="Description..." class="form-control"></textarea>
                            </div>
                            <router-link to="/" class="btn btn-warning">Cancel</router-link>
                            <button class="btn btn-success">Create</button>
                        </form>
                    </div>
                </div>
        </div>
</template>

<script>
import axios from 'axios';

export default {
  data:function() {
    return {
      posts: {
          title:'',
          description:'',
      },
      errors: []
    }
  },

  methods:{
        submitPost() {
        axios.post('/posts', this.posts)
        .then(response => {
            console.log(response)
            this.$router.push({path:'/'})
            this.posts = response.data
        })
            .catch(e => {
            this.errors.push(e)
        })
    }
  }
}
</script>
