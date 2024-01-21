<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps({
  mode: {
    default: "武汉",
  },
})
const arrs = ref(<any>[]);
const handleArr = ()=>{
    if(props.mode === '武汉'){
        arrs.value = [
            {
                title:"计划（计划类型 + 前台计划）"
            },
            {
                title:"项目例会纪要"
            },
            {
                title:"工件开发优化、工时组件、测试执行组件、附件上传"
            },
            {
                title:"文档编制"
            },
            {
                title:"测试用例、测试计划、测试步骤"
            },
            {
                title:"链接关系修正、链接版本组件"
            },
            {
                title:"领域需求库、需求入库、需求历史"
            },
            {
                title:"开发库、项目后台维护"
            },
            {
                title:"其他修正..."
            },


        ]
    }else if(props.mode === '北京') {
        arrs.value = [
            {
                title:"列表实时数据展示"
            },
             {
                title:"地图集成与部署、动态轨迹"
            },
            {
                title:"多模式表单切换"
            },
            {
                title:"模块预测窗口、指令历史"
            },
            {
                title:"检测结果动态展示"
            },

        ]
    }
}
handleArr();
</script>

<template>
  <div>
    <div  start="0" v-for="(item,index) in arrs" :key="props.mode">
  <span style="font-size: small;" class="">{{index + 1 + '.'}}{{ item.title }}</span>
    </div>
  </div>
</template>
