<template>
  <Modal
    :title="title"
    :visible="true"
    :footer="null"
    :width="400"
    :closable="false"
    :mask-closable="true"
    class="addliq-modal"
    centered
    @cancel="$emit('onCancel')"
  >
    <img class="modal-close" src="@/assets/icons/close-circle.svg" @click="$emit('onCancel')" />
    <div class="addliq">
      Our pools/farms are currently being audited.<br />
      Please click
      <a
        href="https://raydium.io/liquidity/add/?coin0=buMnhMd5xSyXBssTQo15jouu8VhuEZJCfbtBUZgRcuW&coin1=EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v&fixed=coin0&ammId=3aBomPsmJc5wBsYQQffQXtXWiS6pw4hbGv29Dai8DkiY"
        target="_blank"
        >here</a
      >
      to add liquidity.
    </div>
  </Modal>
</template>

<script lang="ts">
import Vue from 'vue'
import { Modal } from 'ant-design-vue'

Vue.use(Modal)

export default Vue.extend({
  components: {
    Modal
  },
  props: {
    title: {
      type: String,
      default: ''
    }
  }
})
</script>
