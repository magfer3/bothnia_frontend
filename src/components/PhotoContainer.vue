<template>
  <div>
    <b-col>
      <b-card
        :title="name"
        :img-src="imgsrc"
        img-alt="Image"
        img-top
        tag="article"
        style="max-width: 20rem;"
        class="mb-2"
      >
        <b-card-text>
          Some quick example text to build on the card title and make up the
          bulk of the card's content.
        </b-card-text>
        <b-button
          v-b-tooltip.hover
          title="Bildinformation"
          v-b-modal="modalId"
          variant="primary"
          data-toggle="modal"
          data-target="#exampleModalCenter"
          >Info</b-button
        >
      </b-card>
    </b-col>
    <PopUpInfo></PopUpInfo>
  </div>
</template>

<script>
import PopUpInfo from "@/components/PhotoPopUpInfo.vue";

export default {
  name: "PhotoContainer",
  props: ["name", "imgsrc"],
  components: { PopUpInfo },
  computed: {
    modalId() {
      return `modal-${this.id}`;
    }
  }
};
</script>

<style lang="scss" scoped></style>
