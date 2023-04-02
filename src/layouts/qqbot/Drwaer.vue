<template>
  
    <div class="mx-auto text-h6 mt-0 mb-0 pt-4 pb-4"  style='text-align: center;' >赛博曹宇</div>
    <v-list lines="two" style='text-align: center;'>
      <v-list-item><v-list-subheader>订阅源</v-list-subheader></v-list-item>
        
        <v-list-item
          v-for="item in items"
          :key="item.title"
          :title="item.title"
          :subtitle="item.subtitle"
          @click="goto(item.link)"
        >
            
        <template v-slot:prepend>
            <v-avatar :image="item.avatar" rounded="0"></v-avatar>
          </template>
          
        </v-list-item>
        
      </v-list>
      
</template>

<script setup>
   import { ref } from 'vue'
   import bilibili from '@/assets/bilibili.png'
   import gcores from '@/assets/gcores.png'
   import router from '@/router/index.js'
   const items=[{'title':'bilibili弹幕网','avatar':bilibili,'subtitle':'你所热爱的,就是你的生活','link':'bilibili'},
   {'title':'机核','avatar':gcores,'subtitle':'不止游戏','link':'gcores'}]
   function goto(url){
    router.push('/QQbot/'+url);
    console.log(url);
   }

</script>
