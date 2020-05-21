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
    <div
      class="modal fade"
      id="exampleModalCenter"
      tabindex="-1"
      role="dialog"
      aria-labelledby="exampleModalCenterTitle"
      aria-hidden="true"
    >
      <div class="modal-dialog modal-xl modal-dialog-centered" role="document">
        <div class="modal-content">
          <b-tabs content-class="mt-3">
            <b-tab title="Beskrivning" active><p>Beskrivning</p></b-tab>
            <b-tab title="Specifikation"><p>Specifikation</p></b-tab>
            <b-tab title="Nyckelord"><p>Nyckelord</p></b-tab>
            <b-tab title="Publikationer"><p>Publikationer</p></b-tab>
            <b-tab title="Versioner"><p>Versioner</p></b-tab>
          </b-tabs>
          <div class="modal-footer">
            <button
              type="button"
              class="btn btn-outline-info waves-effect ml-auto"
              data-dismiss="modal"
            >
              Close
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PhotoContainer",
  props: ["name", "imgsrc"],
  computed: {
    modalId() {
      return `modal-${this.id}`;
    }
  }
};
</script>

<style lang="scss" scoped></style>
