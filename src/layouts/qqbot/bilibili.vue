<template>
    <div style="margin-top: 100px;">
    <v-dialog
      v-model="dialog"
      width="auto"
      
    >
      <template v-slot:activator="{ props }">
        <v-card
        class="mx-auto rounded-lg "
        width="280"
        height="200"
        v-bind="props"
      >
      <v-img
          src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
          height="120px"
          class="align-end"
          cover
        ><v-card-title  class="text-white">
            biaoti
          </v-card-title>
        </v-img>
        
    
        <v-card-text>
          内容内容内容
        </v-card-text>
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

    <div class=' mx-auto d-flex justify-space-around mb-6'></div>
    </div>
</template>

<script setup>
import { ref } from 'vue'
const w=ref(11);
const dialog=ref(null);
if(w.value%4!=0){
    w.value=w.value+4-w.value%4;
    console.log(w.value)
}
</script>
