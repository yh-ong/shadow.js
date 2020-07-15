<template>
    <div class="form">
        <div class="form-group">
            <label for="name">Border Radius</label>
            <input type="range" class="range-field" v-model="inputValue.radius" @input="updateInput()" />
            <input type="number" class="input-field" v-model="inputValue.radius" @input="updateInput()" />
        </div>
        <div class="form-group">
            <label for="name">Offset X</label>
            <input type="range" class="range-field" v-model="inputValue.x" @input="updateInput()">
            <input type="number" class="input-field" v-model="inputValue.x" @input="updateInput()">
        </div>
        <div class="form-group">
            <label for="name">Offset Y</label>
            <input type="range" class="range-field" v-model="inputValue.y" @input="updateInput()">
            <input type="number" class="input-field" v-model="inputValue.y" @input="updateInput()">
        </div>
        <div class="form-group">
            <label for="name">Blur</label>
            <input type="range" class="range-field" v-model="inputValue.blur" @input="updateInput()">
            <input type="number" class="input-field" v-model="inputValue.blur" @input="updateInput()">
        </div>
        <div class="form-group">
            <label for="name">Spread</label>
            <input type="range" class="range-field" v-model="inputValue.spread" @input="updateInput()">
            <input type="number" class="input-field" v-model="inputValue.spread" @input="updateInput()">
        </div>
        <div class="form-group">
            <label for="name">Color</label>
            <input type="color" class="color-field" v-model="inputValue.color" @input="updateInput()">
        </div>
    </div>
</template>

<script>
export default {
    name: 'form-field',
    data() {
        return {
            inputValue: {
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
        updateInput() {
            this.$emit('input', this.inputValue)
        }
    }
}
</script>