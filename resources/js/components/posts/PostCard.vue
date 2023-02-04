<template>
    <div class="container">
        <h1 class="text-danger mb-4">Sono la pagina del singolo post: <h2 class="text-white d-inline">{{ posts.title }}</h2> </h1>

        <h3>{{ posts.body }}</h3>

    </div>
</template>

<script>

export default {
    name: 'PostCard',
    components: {
    },
    data() {
        return {
            posts: null,
        }
    },
    mounted() {
        this.getPost();
    },
    methods: {
        getPost() {
            axios.get('http://localhost:8000/api/posts/' + this.$route.params.id)
                .then((res) => {
                    console.log(res.data);
                    this.posts = res.data;
                }).catch(err => {
                    console.log(err)
                })
        }
    }
}
</script>
