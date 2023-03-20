<template>
  <div class="  d-flex align-content-start flex-wrap mt-5">
  <v-responsive max-width="400px" min-width="400px">
  <div class=" ml-9 d-flex justify-start mb-1 ">
    <v-responsive
    
        >
        <v-switch
        v-model="ex11"
        label="开启推送"
        color="primary"
        value="1"
        class="pl-3"
        hide-details
      ></v-switch>
        </v-responsive>
  
            <v-btn class="align-self-center" variant="outlined"  color="primary">
              新增订阅
            </v-btn>
  </div>



    <v-responsive
          max-width="390"
          class="ml-6"
          thumb-label>
          <div class="text-caption ml-6" style="position: absolute;top: 5px;">自动更新时间</div>
          <v-slider
        v-model="value"
          :min="10"
          :max="60"
          :step="10"
          class="mx-auto pt-3 pb-3 pl-6 pr-6"
          hide-details>
          <template v-slot:append>
            <v-text-field
              v-model="value"
              hide-details
              single-line
              density="compact"
              type="number"
              variant="underlined"
              style="width: 70px"
            ></v-text-field>
          </template>
        </v-slider>
        
    </v-responsive>
    



    <v-responsive
          class="ml-12"
          max-width="344"
        >
          <v-text-field
            label="屏蔽词(逗号分隔)"
            hide-details="auto"
            clearable
            variant="underlined"
            hint="含有含有屏蔽词的稿件将不会被推送"
          ></v-text-field>
    </v-responsive>
  </v-responsive>
  <v-divider vertical class="ml-12"></v-divider>
  <v-responsive max-width="600px" min-width="400px">
<div class="text-h6 ml-3">服务器监控</div>
<v-textarea  class="text-h6 ml-3" label="这里是监控内容，应该有更好看的方案" variant="outlined"></v-textarea>

</v-responsive>
</div>

    <v-divider class="mt-5 mb-5"></v-divider>
    <v-responsive
          class="ml-6"
          max-width="344"
        >
        <v-text-field clearable label="搜索" variant="underlined"></v-text-field>
  </v-responsive>

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
        style="margin-top: 30px;"
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
  <v-pagination :length="4"></v-pagination>
</template>

<script setup>
import { ref } from 'vue'
const data=ref(11);
const ex11=ref(11);
const value=ref(60);
const dialog=ref(null);
const linenuber=ref()



</script>
