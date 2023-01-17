<template>

  <div class="flex justify-center items-center h-screen" style="position: relative">
    <div class="shadow-xl sm:overflow-hidden sm:rounded-lg ">
      <div class="bg-[#fcfbfa] px-4 py-6 sm:p-6 bg-opacity-100">

      <n-space vertical class="grid gap-4 place-items-center">
        <img :src="logo" class="h-14 w-60">
        <h1 class="font-bold text-lg" style="margin-top:-5px">Oracle APEX</h1>
        <n-input type="text" size="large" placeholder="工作区" class="shadow-sm border-slate-300 placeholder-slate-400 focus:outline-none block w-full rounded-md sm:text-sm focus:ring-1"/>
        <n-input type="text" size="large" placeholder="用户名" class="shadow-sm border-slate-300 placeholder-slate-400 focus:outline-none block w-full rounded-md sm:text-sm focus:ring-1"/>
        <n-input type="password" size="large" placeholder="密码" class="shadow-sm border-slate-300 placeholder-slate-400 focus:outline-none block w-full rounded-md sm:text-sm focus:ring-1"/>
        <n-checkbox value="Option 1" class="text-xs " style="margin-right: 200px;">
          记住工作区和用户名
        </n-checkbox>
        <n-button class="bg-[#10499B] rounded-lg" type="info" style="width: 350px;height: 45px;">登录</n-button>
        <a href="" class="text-[#ae562c] text-xs no-underline hover:underline">重置密码</a>

      </n-space>

    </div>
      <div class="bg-[#f1efed] flex justify-center items-center h-10">
      <a href="" class="text-[#ae562c] text-xs no-underline hover:underline">English</a>
        <p style="margin:5px"> · </p>
      <a href="" class="text-[#ae562c] text-xs no-underline hover:underline">中文（简体)</a>
    </div>

  </div>
  </div>


</template>

<script>

import {NButton} from 'naive-ui'
import {NInput} from "naive-ui"
import {NCheckbox} from "naive-ui"
import Logo from "/src/assets/ja-solar-logo-vector.png"

export default {
  name: "InputField",
  components:{
  NButton,
    NInput,
    NCheckbox,
  },
  data:function (){
    return{
      logo:Logo
    }
  }
}
</script>