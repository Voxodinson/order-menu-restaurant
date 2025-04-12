<template>
    <div 
        class="w-full h-fit flex items-center justify-start flex-col mb-[10vh]">
        <div class="w-[80%] bg-red-500 flex items-center text-white p-3 rounded-md mt-3">
            <UIcon 
                name="material-symbols:arrow-right-rounded" 
                class="w-8 h-8" />
            <h3
                class="text-[1.2rem]">
                គុយទាវ
            </h3>
        </div>
        <div 
            class="w-[80%] grid grid-cols-3 gap-3 mt-3">
            <div 
                v-for="(item, idx) in MenuData.menu_data"
                :key="idx"
                class="w-full h-fit gap-3 rounded-md border-gray-300 flex flex-col border-[1px] p-2">
                <div 
                    class="h-[250px] w-full overflow-hidden rounded-md">
                    <img 
                        :src="item.image" 
                        alt="image"
                        class=" w-full h-full object-cover">
                </div>
                <div 
                    class=" ">
                    <h3
                        class="font-semibold text-[1.2rem] text-gray-600">
                        {{ item.name }}</h3>
                    <span
                        class="text-red-500">
                        ${{ item.price }}</span>
                </div>
                <button
                    class="w-full py-2 cursor-pointer text-center bg-blue-500 text-white hover:bg-blue-400 transition rounded-md">
                    Add Order
                </button>
            </div>
        </div>
        <div class="w-[80%] bg-red-500 flex items-center text-white p-3 rounded-md mt-3">
            <UIcon 
                name="material-symbols:arrow-right-rounded" 
                class="w-8 h-8" />
            <h3
                class="text-[1.2rem]">
                បាយ​
            </h3>
        </div>
        <div 
            class="w-[80%] grid grid-cols-3 gap-3 mt-3">
            <div 
                v-for="(item, idx) in MenuData.menu_data"
                :key="idx"
                class="w-full h-fit gap-3 rounded-md border-gray-300 flex flex-col border-[1px] p-2">
                <div 
                    class="h-[250px] w-full overflow-hidden rounded-md">
                    <img 
                        :src="item.image" 
                        alt="image"
                        class=" w-full h-full object-cover">
                </div>
                <div 
                    class=" ">
                    <h3
                        class="font-semibold text-[1.2rem] text-gray-600">
                        {{ item.name }}</h3>
                    <span
                        class="text-red-500">
                        ${{ item.price }}</span>
                </div>
                <button
                    class="w-full py-2 cursor-pointer text-center bg-blue-500 text-white hover:bg-blue-400 transition rounded-md">
                    Add Order
                </button>
            </div>
        </div>
    </div>
    <div 
        class=" fixed bottom-0 flex items-center justify-center left-0 w-full h-[8vh] z-30 bg-red-500">
        <div 
            class="w-[80%] h-full flex items-center justify-between">
            <h6
                class="text-white text-[1.2rem]">
                Total Items: 10
            </h6>
            <div class="flex gap-3">
                <button
                    class="px-6 rounded-full py-2 bg-white text-black hover:bg-blue-600 hover:text-white cursor-pointer">
                    View Items
                </button>
                <button
                    class="px-6 py-2 rounded-full bg-blue-600 text-white hover:bg-white hover:text-black cursor-pointer">
                    Save Order
                </button>
            </div>
        </div>
    </div>
</template>

<script lang="ts" setup>
import { 
    MenuData 
} from '~/public/data';
</script>