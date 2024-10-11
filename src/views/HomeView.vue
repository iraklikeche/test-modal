<script setup>
import Modal from "@/components/Modal.vue"; // Make sure the path is correct

import { ref } from "vue"; // Using ref to toggle modal visibility

const isModalOpen = ref(false);

const openModal = () => {
  isModalOpen.value = true;
};

const closeModal = () => {
  isModalOpen.value = false;
};
</script>

<template>
  <div>
    <!-- Your application routes -->

    <!-- Button to trigger modal -->
    <button @click="openModal" class="bg-blue-500 text-white px-4 py-2 rounded">
      Open Modal
    </button>

    <!-- Modal component -->
    <Modal v-if="isModalOpen" @close="closeModal" />
  </div>
</template>
