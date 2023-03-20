<template>
  <div class=" ml-12 d-flex justify-start mb-6 ">
    <v-responsive
          max-width="150"
        >
        <v-switch
        v-model="ex11"
        label="开启推送"
        color="primary"
        value="1"
        hide-details
      ></v-switch>
        </v-responsive>
  
            <v-btn class="align-self-center" variant="outlined"  color="primary">
              新增订阅
            </v-btn>
          </div>
          <v-responsive
          class="ml-12"
          max-width="344"
        >
          <v-text-field
            label="屏蔽词(逗号分隔)"
            hide-details="auto"
            variant="underlined"
          ></v-text-field>
        </v-responsive>
          <v-divider class="mt-5"></v-divider>
    <div class="d-flex align-content-start flex-wrap" >
    
    <v-dialog
      v-model="dialog"
      width="auto"
      v-for="i in 9"
    >
      <template v-slot:activator="{ props }">
        <v-card
        class="mx-auto rounded-lg"
        width="280"
        height="230"
        v-bind="props"
        style="margin-top: 50px;"
      >
      <v-img
          src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
          height="120px"
          class="align-end "
          cover
        >
        <v-card-title  class="mx-auto text-white d-flex align-content-start flex-wrap" >
          <p class=" text-h6">up主名字</p>
          </v-card-title>
        </v-img>
        
    
        <v-card-text>
          最新一期的标题
        </v-card-text>
        <v-card-actions >
          <v-btn class="mx-auto" variant="outlined"  color="primary">
            配置
          </v-btn>
          <v-btn class="mx-auto" variant="outlined" color="red" >
            删除
          </v-btn>
          
        </v-card-actions>
      </v-card>
      </template>

      <v-card>
        <v-card-text>
            修改修改修改
        </v-card-text>
        <v-card-actions>
          <v-btn color="primary" block @click="dialog = false">提交</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>

    
    <div 
    style="height: 0px;width: 280px;"
    class="mx-auto"
    v-for="i in 10"></div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const data=ref(11);
const ex11=ref(11);
const dialog=ref(null);
const linenuber=ref()



</script>
