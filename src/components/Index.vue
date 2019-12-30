<template>
  <div>
    <header>
      <DxToolbar id="munToolbar" @item-click="menuClick" :items="dataSource">
          <template #default="{}">
            <img src="../assets/logo.svg" />
          </template>

      </DxToolbar>
    </header>
  </div>
</template>

<script>
import DxToolbar from 'devextreme-vue/toolbar';
//import DxToolbar, { DxItem } from 'devextreme-vue/toolbar';
// import DropDownButton from "devextreme-vue/drop-down-button";
// import LogoImg from './LogoImg.vue'

import notify from 'devextreme/ui/notify';
import 'devextreme/ui/select_box';

export default {
  components: {
    // DropDownButton,
    // LogoImg,
    DxToolbar//,
    //DxItem
  },
    data(){
        return{
          data:{size:"12",text:"520"},
          dataSource:[{
          location:"before",
          template:"default"
          },{
          location:"after",
          text:"首页"
          },{
          location:"after",
          text:"博客"
          },{
          location:"after",
          text:"社区"
          },{
          location:"after",
          text:"资源"
          },{
          location:"after",
          text:"问答"
          }]
        }
    },
    methods:{
      menuClick(e){
        console.log(e)
        notify(e.value);
      }
    }
}
</script>

<style>
  header{
    box-shadow: 0 1px 1px rgba(0,0,0,.08);
  }
  #munToolbar{
    width: 95%;
    height: 65px;
    margin: 0 auto;
    color:#515a6e;
  }
  #munToolbar img{
    height: 65px;
  }
  .dx-toolbar-after .dx-toolbar-item 
  {
    cursor: pointer;
    line-height: 65px;
    padding:0 10px!important;
    font-size: 14px;
  }
  .navActive,.dx-toolbar-after .dx-toolbar-item:hover{
    border-bottom: 2px solid #2d8cf0;
    color:#2d8cf0;
  }
</style>