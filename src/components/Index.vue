<template>
  <div>
    <header>


    <DxToolbar>
      <DxItem
        location="before"
      />
      <template #item="{ data: item }">
        <LogoImg></LogoImg>
      </template>
    </DxToolbar>
        </header>
    </div>
</template>

<script>
import DxToolbar, { DxItem } from 'devextreme-vue/toolbar';
import LogoImg from './LogoImg.vue'

import notify from 'devextreme/ui/notify';
import 'devextreme/ui/select_box';

export default {
  components: {
    LogoImg,
    DxToolbar,
    DxItem
  },
    data(){
        return{
          logoButtonOption:{
            icon: '../../assets/logo.png',
            onClick: () => {
              notify('Back button has been clicked!');
            }
          }
        }
    },
    methods:{

    }
}
</script>

<style scoped>
  header {
    background: blueviolet;
  }
</style>