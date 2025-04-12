<template>
    <div class="w-full bg-red-500 h-[8vh] flex items-center justify-center">
        <div class="w-[80%] flex justify-between items-center">
            <h1 class="uppercase text-white text-[2rem]">
                Logo
            </h1>
            <ul class="flex gap-6">
                <li>
                    <ULink
                    to="/"
                    :class="linkClass('/')">
                    Menu
                    </ULink>
                </li>
                <li>
                    <ULink
                    to="/order"
                    :class="linkClass('/order')">
                    Order
                    </ULink>
                </li>
                <li>
                    <ULink
                    to="/summary"
                    :class="linkClass('/summary')">
                    Summary
                    </ULink>
                </li>
            </ul>
        </div>
    </div>
</template>

<script lang="ts" setup>
import { 
    ULink 
} from '#components'
import { 
    useRoute 
} from 'vue-router'

const route = useRoute()

const linkClass = (path: string) => {
    const baseClass = 'rounded-full px-4 py-2 text-white transition'
    const isActive = route.path === path;
    return `${baseClass} ${isActive ? 'text-red-500 bg-white' : ''}`
}
</script>
  