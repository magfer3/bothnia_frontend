<template>
  <div>
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
  name: "PopUpInfo",
  computed: {
    modalId() {
      return `modal-${this.id}`;
    }
  }
};
</script>

<style lang="scss" scoped></style>
