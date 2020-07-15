<template>
  <div id="result">
      <div class="box" v-bind:style="styles"></div>
  </div>
</template>

<script>
export default {
    name: 'result',
    props: ['itemsData'],
    computed: {
        styles() {
            var unit = 'px';
            return {
                'border-radius': this.itemsData.radius + unit,
                'box-shadow': this.itemsData.x + unit + ' ' + this.itemsData.y + unit + ' ' + this.itemsData.blur + unit + ' ' + this.itemsData.spread + unit + ' ' + this.itemsData.color
            }
        }
    }
}
</script>