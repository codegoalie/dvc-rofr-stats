<template>
  <a @click="showFeedbackDialog"><slot /></a>
</template>

<script>
export default {
  props: {
    text: String,
  },
  methods: {
    showFeedbackDialog() {
      this.$modal.open({
        parent: this,
        content:
          '<iframe src="https://docs.google.com/forms/d/e/1FAIpQLSfQCt28Gxr5VfS_bi0vjN1FSRk2Q4XLOXkKU7vWOasFF3bE3Q/viewform?embedded=true" width="100%" height="100%" frameborder="0" marginheight="0" marginwidth="0">Loading...</iframe>',
      });
    },
  },
};
</script>

<style lang="scss">
.modal-card-body {
  padding: 0;
}
// .modal,
// .modal-content {
//   --webkit-overflow-scrolling: touch;
//   overflow-y: scroll;
// }
.modal-content div {
  height: 1200px;
}
</style>
