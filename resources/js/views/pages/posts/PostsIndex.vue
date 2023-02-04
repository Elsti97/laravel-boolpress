<template>
  <div>
    <h1 class="text-center my-5">List posts:</h1>
    <PostsList />
  </div>
</template>

<script>
import PostsList from "../../../components/posts/PostsList.vue";

export default {
  name: "Posts",
  components: {
    PostsList,
  },
  data() {
    return {};
  },
  methods: {},
};
</script>
