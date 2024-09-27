<template>
  <div class="container" @click="handleClick">
    <img :src="img" height="300px" />
  </div>
</template>
<script setup lang="ts">
interface Props {
  img: string
  text: string
  id: string
}

const props = defineProps<Props>()

const emit = defineEmits<{
  hoverCompClick: [id: string]
}>()

const handleClick = () => {
  emit('hoverCompClick', props.id)
}
</script>
<style scoped>
.container {
  height: fit-content;
  width: fit-content;
  padding: 8px;
  overflow: hidden;
}

.container img {
  transition: transform 0.5s ease;
  border-radius: 10px;
}

.container:hover img {
  transform: scale(1.1);
  border-radius: 10px;
  cursor: pointer;
}
</style>
