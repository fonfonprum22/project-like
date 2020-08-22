<template>
  <div>
      <button 
        class="rounded-0 btn btn-link"
        @click="emitValue(couter)"
        >
            <img :src="require(`../assets/icon/${data}.png`)" 
                  style="width:30px">
        </button>
  </div>
</template>

<script>
export default {
    props: ['data', 'couter'],
    methods: {
        emitValue (value) {
            this.$emit('toParent',value)
            }
          },
}
</script>