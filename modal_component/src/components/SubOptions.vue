<template>
     <div class="margin_left child_ele" style="display:none" v-bind:class="{ show: (selected === 'Yes') }">
        <b-form-group label="But, Unlimited or Limited is a relative term! is it not?">
            <b-form-radio v-model="selected" name="some-radios" value="A">Yes</b-form-radio>
            <b-form-radio v-model="selected" name="some-radios" value="B">No</b-form-radio>
        </b-form-group>
    </div>
</template>
<script>
export default {
    name:"SubOptions",    
    props:['selected']
}
</script>
<style scoped>
.margin_left{
    margin-left: 10%;
}
.show{
    display:block !important;
}
</style>