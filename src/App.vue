<template>
  <div class="container">
    <h2>태그 치환하기 - test last</h2>
    <div class="group_inp">
      <input
        type="text"
        v-model="txt"
        @keyup.enter="changeTxt"
        class="inp_txt" />
      <button
        type="button"
        class="btn"
        @click="changeTxt">
        변환
      </button>
    </div>

    <div
      class="result"
      v-if="result">
      {{ result }}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      txt: '',
      result: ''
    }
  },
  methods: {
    changeTxt() {
      this.result = this.txt.replaceAll(' #', ',').replace('#', '')
    }
  }
}
</script>