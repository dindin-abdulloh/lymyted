<template>
    <div :class="currentColorClass" class="color-transition p-3">
      <p class="text-transition text-xl font-semibold" :class="currentTextColorClass">
        {{ currentText }}
      </p>
    </div>
  </template>
  
  <script>
  import { ref, onMounted, computed } from 'vue';
  
  export default {
    setup() {
      const colors = ref([
        { background: "bg-[#fe3ca7]", text: "Get free delivery on orders over $100" },
        { background: "bg-[#cdff63]", text: "Get free delivery on orders over $10" },
      ]);
      const currentColorIndex = ref(0);
  
      const currentColorClass = computed(() => colors.value[currentColorIndex.value].background);
      const currentText = computed(() => colors.value[currentColorIndex.value].text);
      const currentTextColorClass = computed(() =>
        currentColorClass.value.includes("fe3ca7") ? "text-white" : "text-black"
      );
  
      const changeColor = () => {
        currentColorIndex.value = (currentColorIndex.value + 1) % colors.value.length;
      };
  
      onMounted(() => {
        setInterval(changeColor, 3000);
      });
  
      return {
        currentColorClass,
        currentText,
        currentTextColorClass,
      };
    },
  };
  </script>
  
  <style scoped>
  .color-transition {
    display: flex;
    align-items: center;
    justify-content: center;
    transition: background-color 0.5s ease; /* Sesuaikan durasi dan fungsi timing sesuai keinginan Anda */
  }
  
  .text-transition {
    transition: color 0.5s ease; /* Sesuaikan durasi dan fungsi timing sesuai keinginan Anda */
  }
  </style>