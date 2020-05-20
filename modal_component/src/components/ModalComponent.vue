<template>
    <div>
        <b-modal id="modal-lg" size="lg" v-model="modalShow " hide-footer>           
        <template v-slot:modal-title>
                <span class="side_panel">
                    <img class="profile" src="../assets/profile.png" width="100" height="100">
                </span>
            <ModalHeader />
        </template>
        <div class="d-block text-left">
            <ModalBody />
        </div>
        <b-button variant="danger" class="btn_align">Button</b-button>
    </b-modal>       
    </div>
</template>

<script>
import ModalHeader from './ModalHeader.vue';
import ModalBody from './ModalBody.vue';

export default {
    name:'ModalComponent',
    components: {
    ModalHeader,
    ModalBody
  },
  data() {
      return {
        modalShow: true
      }
    }
}
</script>
<style scoped>
.btn_align{
    float:right;
}
.side_panel{    
    right: 99%;
    position: absolute;
    top: 0;
    bottom: 0px;
    background: #F1F1F1;
    height: auto;
    width: 180px;
}
.profile{
    position: absolute;
    top:10%;
    left: 23%; 
}
</style>