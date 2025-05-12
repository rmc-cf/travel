<template>
	<view class="content">
		<up-search placeholder="搜索经典" bg-color="#e3e3e3" v-model="keyword"></up-search>
	</view>
</template>

<script setup>
import { ref } from 'vue';
import { getBanner } from '../../api/api';
import {onLoad} from '@dcloudio/uni-app'
const keyword = ref('')
onLoad(async()=>{
	const res = await getBanner()||[{image:'http://159.75.169.224:5500/ComfyUI_00012_.png',title:'123'}]
	console.log(res);
})
	
</script>

<style>

</style>
