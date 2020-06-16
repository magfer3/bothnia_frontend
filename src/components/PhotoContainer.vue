<template>
  <div>
    <b-col>
      <b-card
        :img-src="locationOnDisc"
        img-alt="Image"
        img-top
        tag="article"
        style="max-width: 20rem;"
        class="mb-2"
      >
        <b-button
          v-b-tooltip.hover
          title="Bildinformation"
          variant="primary"
          data-toggle="modal"
          :data-target="modalTarget"
          >Info</b-button
        >
      </b-card>
    </b-col>
    <PopUpInfo
      :id="modalId"
      :piNo="piNo"
      :locationOnDisc="locationOnDisc"
    ></PopUpInfo>
  </div>
</template>

<script>
import PopUpInfo from "@/components/PopUpInfo.vue";

export default {
  name: "PhotoContainer",
  props: ["piNo", "locationOnDisc"],
  components: { PopUpInfo },
  computed: {
    modalId() {
      return `modal-${this.piNo}`;
    },
    modalTarget() {
      return `#modal-${this.piNo}`;
    }
  },
  data: function() {
    return {};
  }
};
</script>

<style lang="scss" scoped>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
</style>
