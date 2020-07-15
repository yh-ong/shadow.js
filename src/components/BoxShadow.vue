<template>
  <div>
    <div id="box-shadow">
      <form-field v-on:input="updateChild"></form-field>
      <result :itemsData="boxShadow"></result>
    </div>
    <clipboard :itemsData="boxShadow"></clipboard>
  </div>
</template>

<script>
import FormField from './FormField.vue';
import Result from './Result.vue';
import Clipboard from './Clipboard.vue';

export default {
    name: 'box-shadow',
    components: {
      FormField,
      Result,
      Clipboard
    },
    data() {
      return {
        boxShadow: {
          radius: 0,
          x: 0,
          y: 0,
          blur: 0,
          spread: 0,
          color: '#000'
        }
      }
    },
    methods: {
      updateChild(value) {
        this.boxShadow = value;
      }
    }
}
</script>