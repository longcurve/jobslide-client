<template>
  <teleport to="body">
     <div
     v-if="showModal"
      ref="modal-backdrop"
      class="fixed z-10 inset-0 overflow-y-auto bg-black bg-opacity-50">
        <div
          class="flex items-start justify-center min-h-screen pt-24 text-center">
          <div
            class="w-1/2 bg-white rounded-lg text-left overflow-hidden shadow-xl"
            role="dialog"
            ref="modal"
            aria-modal="true"
            aria-labelledby="modal-headline">
            This is a modal
          </div>
        </div>
      </div>
  </teleport>
</template>