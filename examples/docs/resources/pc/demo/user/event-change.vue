<template>
  <tiny-user v-model="user" multiple @change="change"></tiny-user>
</template>

<script lang="jsx">
import { User, Modal } from '@opentiny/vue'

export default {
  components: {
    TinyUser: User
  },
  data() {
    return {
      user: '441047913162396,702973890055088,421000103624183'
    }
  },
  methods: {
    change(val) {
      Modal.message({ message: `${val}`, status: 'info' })
    }
  }
}
</script>
