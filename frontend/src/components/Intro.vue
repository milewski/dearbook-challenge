<script setup lang="ts">
    defineProps<{ cover: string, backdrop: string, title: string, subject: string }>()
</script>

<template>

    <div class="flex justify-center p-4">

        <div
            class="relative before:rounded-2xl before:opacity-75 before:absolute before:from-black before:bg-gradient-to-t before:w-full before:h-5/6 before:left-0 before:bottom-0">
            <img class="rounded-2xl" :src="backdrop" alt="">
        </div>

        <div class="absolute flex justify-center items-center flex-column text-white p-4 rounded-2xl bottom-14 sm:bottom-28">

            <img class="rounded-xl h-80 mr-4 shadow-2xl border-4 hidden sm:block" :src="cover" alt="">

            <div class="px-4 sm:w-7/12 text-center sm:text-left">

                <h1 class="text-2xl sm:text-4xl font-bold">
                    {{ title }}
                </h1>

                <p class="sm:text-2xl mt-2 sm:mt-5">
                    {{ subject }}
                </p>

            </div>

        </div>

    </div>

</template>
