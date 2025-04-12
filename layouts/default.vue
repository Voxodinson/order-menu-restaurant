<template>
    <div    
        class="w-full h-fit">
        <UApp>
            <NavBar/>
            <NuxtPage />
        </UApp>
    </div>
</template>

<script lang="ts" setup>
import { NavBar } from '~/components';
</script>