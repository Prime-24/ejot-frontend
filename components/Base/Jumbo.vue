<script setup lang="ts">
let images = ["ejot-teaser-1.jpg", "ejot-teaser-2.jpg", "ejot-teaser-1.jpg", "ejot-teaser-2.jpg"];
let counter = ref(0);
let xPosition = reactive({ start: 0, end: 0 });

const moveStart = (event: DragEvent | TouchEvent) => {
    if (event instanceof DragEvent) {
        xPosition.start = event.clientX;

    } else {
        xPosition.start = event.touches[0].clientX;
    }
}
const moveOver = (event: DragEvent | TouchEvent) => {
    if (event instanceof DragEvent) {
        xPosition.end = event.clientX;
    } else {
        xPosition.end = event.touches[0].clientX;
    }
}
const moveEnd = () => {

    if (images.length === 1) return;

    let xDelta = xPosition.start - xPosition.end;

    if (xDelta > 50) {
        nextImg();
    }
    if (xDelta < -50) {
        prevImg();
    }
}

const indicator = (index: number) => {
    counter.value = index;
}

const nextImg = () => {
    counter.value < images.length - 1 ? counter.value++ : counter.value = 0;
}
const prevImg = () => {
    counter.value <= 0 ? counter.value = images.length - 1 : counter.value--;
}

const translateStyle = computed(() => {
    return `transform: translateX(${-(counter.value) * 100}%)`;
});


</script>


<template>
    <div class="slider relative">

        <div class="slides flex overflow-hidden">

            <div class="slide flex-shrink-0 w-full transition-transform" v-for="image in images"
                :style="[translateStyle]">

                <img class="w-full aspect-video object-cover" @touchstart="moveStart($event)"
                    @touchmove="moveOver($event)" @touchend="moveEnd()" :src="'/img/' + image">

                <div class="absolute bottom-0 w-full bg-white bg-opacity-75 p-4">
                    <h1>Heading goes here</h1>
                    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Possimus suscipit quia recusandae sed
                        culpa
                    </p>
                    <BaseLinkButton :link-type="'primary'" :link-icon="true">Click here</BaseLinkButton>
                </div>

            </div>

        </div>

        <button v-if="images.length > 1" @click="nextImg"
            class="absolute top-1/2 transform -translate-y-1/2 p-4 bg-blue-900 text-white right-0 z-10 cursor-pointer">Next</button>
        <button v-if="images.length > 1" @click="prevImg"
            class="absolute top-1/2 transform -translate-y-1/2 p-4 bg-blue-900 text-white left-0 z-10 cursor-pointer">Prev</button>

        <div v-if="images.length > 1" class="absolute bottom-4 left-1/2 transform -translate-x-1/2 flex gap-4 z-10">
            <span v-for="(image, index) in images" :key="index" @click="indicator(index)"
                :class="[index === counter ? 'bg-red-600' : 'bg-black', 'h-2 w-8 cursor-pointer']"></span>
        </div>

    </div>
</template>

<style></style>

