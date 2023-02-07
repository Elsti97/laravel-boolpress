<template>
  <div>
      <h3 :key="elem.name" v-for="elem in tag">
        <ul>
          <li :key="post.id" v-for="post in elem.posts">
            {{ post.title }}
          </li>
        </ul>
      </h3>
  </div>
</template>

<script>
export default {
  name: "TagCard",
  components: {},
  data() {
    return {
      tag: [],
    };
  },
  mounted() {
    this.getTag();
  },
  methods: {
    getTag() {
      axios
        .get("http://localhost:8000/api/tags/" + this.$route.params.name)
        .then((res) => {
          console.log(res.data);
          this.tag = res.data;
        })
        .catch((err) => {
          console.log(err);
        });
    },
  },
};
</script>
