<template>
  <div>
    <h1>Pagina dei tags</h1>

    <TagsList />
  </div>
</template>

<script>
import TagsList from "../../../components/tags/TagsList.vue";

export default {
  name: "TagsIndex",
  components: {
    TagsList,
  },
};
</script>
