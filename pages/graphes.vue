<template>
  <b-container>
    <h1 class="mt-5 mb-4">Charts:</h1>
    <div>
      <grapheone></grapheone>
    </div>
    <div>
      <graphetwo></graphetwo>
    </div>
  </b-container>
</template>
<script>
import Grapheone from "../components/graphes/grapheone.vue";
import Graphetwo from "../components/graphes/graphetwo.vue";
export default {
  layout: "loggedIn",
  components: {
    Grapheone,
    Graphetwo
  }
};
</script>
