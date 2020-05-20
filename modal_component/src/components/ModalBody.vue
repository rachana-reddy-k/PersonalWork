<template>
    <div v-bind:class="{ bottom_border: (selected === 'Yes') }">
        <div class="bottom_border">
            <b-form-group>
                <b-form-radio-group
                    v-model="selected"
                    :options="options"
                    name="radios-stacked"
                    stacked                    
                ></b-form-radio-group>
            </b-form-group>
        </div>
        <div>
            <SubOptions v-bind:selected="selected" />
        </div>
    </div>
</template>

<script>

import SubOptions from "./SubOptions.vue"
  export default {
      name:"ModalBody",
      components :{
          SubOptions
      },
    data() {
      return {
        selected: 'Yes',
        options: [
          { text: 'Yes', value: 'Yes' },
          { text: 'No', value: 'No' }
        ]
      }
    }
  }
</script>

<style scoped>
.bottom_border{
    border-bottom:1px solid #dee2e6;
    margin: 10px 0;
}

</style>