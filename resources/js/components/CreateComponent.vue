<template>
    <div>
        <h1>Create Post</h1>
        <form @submit.prevent="addPost">
            <b-form-group
                id="post-title"
                label="Post Title"
                label-for="postTitle"
                description="This will be the title of your post">

                <b-form-input
                    id="postTitle"
                    v-model="post.title"
                    type="text"
                    required
                    placeholder="Enter Title">
                </b-form-input>

            </b-form-group>

            <b-form-group
                id="post-body"
                label="Post Body"
                label-for="postBody"
                description="This will be the body of your post">

                <b-form-textarea
                    id="postBody"
                    v-model="post.body"
                    type="text"
                    required
                    placeholder="Describe what your post"
                    rows="5">
                </b-form-textarea>

            </b-form-group>
            <br />

            <b-form-group>
                <button class="btn btn-outline-dark">Create</button>
            </b-form-group>
        </form>
    </div>
</template>

<script>
    export default {
        mounted() {
            console.log('Create Component mounted');
        },
        data(){
            return {
                post:{}
            }
        },
        methods: {
            addPost(){
                let uri = '/api/post/create';
                this.axios.post(uri, this.post).then(() => {
                    this.$router.push({name: 'posts'});
                });
            },
        }
    }
</script>

<style scoped>

</style>
