<template>
  <!-- Modal Background Overlay -->
  <div
    class="fixed inset-0 bg-gray-800 bg-opacity-75 flex items-center justify-center z-50"
  >
    <!-- Modal Window -->
    <div
      class="bg-white rounded-lg overflow-hidden shadow-xl w-1/2 max-h-[510px] flex flex-col"
    >
      <!-- Modal Header -->
      <div class="p-4 border-b flex justify-between items-center">
        <h3 class="text-lg font-semibold">Modal Title</h3>
        <button
          @click="$emit('close')"
          class="text-gray-400 hover:text-gray-600"
        >
          &times;
        </button>
      </div>

      <!-- Modal Body -->
      <div class="p-6 overflow-y-auto flex-grow">
        <p>
          This is the modal content. It will adjust its height based on the
          content but won't exceed 510px. If the content is too long, this
          section will be scrollable.
        </p>
        <p>
          Add a lot more content here to see the scrollable effect in action.
        </p>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum
          nec nulla ac urna tincidunt pharetra non id est. Nullam dictum nec
          turpis ac egestas. Integer sit amet aliquet ipsum, a cursus justo.
          Duis sed nibh nec leo volutpat posuere.
        </p>
        <p>Continue adding more content to test the scrolling effect.</p>
        <p>
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Omnis
          perspiciatis molestiae nobis sint ducimus expedita est dignissimos,
          alias amet consectetur obcaecati, libero aliquid maiores corporis?
          Distinctio quae nemo, consectetur itaque impedit aut. Quaerat,
          eligendi, unde quidem labore distinctio, tempore eos exercitationem
          soluta rem nisi molestias vero fugiat sint quo! Quo reiciendis
          recusandae sapiente itaque, aliquam voluptatem similique id tenetur
          porro dolores. Odio, sed consequatur! Fugiat voluptas, architecto
          vitae nemo asperiores officiis odio quisquam quae suscipit
          repellendus. Quidem eveniet voluptatum modi, dolorem delectus autem
          cumque, sapiente qui nemo excepturi eaque distinctio culpa unde
          possimus quia deserunt eum. Accusamus est alias ab vel sunt, modi odit
          error fugiat ad voluptatum! Consectetur dolor quo aliquam, delectus
          fugit voluptatem aut quod ipsum ut sequi consequuntur vero eaque cum
          recusandae numquam qui, deleniti minima? Dolore provident tenetur iste
          error modi animi ab cumque iure minus quibusdam. Odit deleniti at
          alias. Harum non quaerat unde voluptatibus?
        </p>
      </div>

      <!-- Modal Footer -->
      <div class="p-4 border-t text-right">
        <button
          @click="$emit('close')"
          class="bg-gray-500 text-white px-4 py-2 rounded"
        >
          Close
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
defineEmits(["close"]);
</script>

<style scoped>
/* Add fade-in/fade-out transitions */
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active in <2.1.8 */ {
  opacity: 0;
}
</style>
