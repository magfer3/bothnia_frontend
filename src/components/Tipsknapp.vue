<template>
  <div class="hello">
    <p>
      <button type="button" class="btn btn-default btn-sm">
        <span class="glyphicon glyphicon-envelope"></span>
      </button>
    </p>
  </div>
</template>

<script>
export default {
  name: "Tipsknapp",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss"></style>
