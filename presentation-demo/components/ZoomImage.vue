<script setup lang="ts">
import { nextTick, ref } from 'vue'

const props = defineProps<{
  src: string
  alt: string
  previewClass: string
}>()

const isOpen = ref(false)
const trigger = ref<HTMLButtonElement | null>(null)
const overlay = ref<HTMLDivElement | null>(null)

async function openImage() {
  isOpen.value = true
  await nextTick()
  overlay.value?.focus()
}

async function closeImage() {
  isOpen.value = false
  await nextTick()
  trigger.value?.focus()
}
</script>

<template>
  <button
    ref="trigger"
    type="button"
    class="group relative block w-full cursor-zoom-in appearance-none border-0 bg-transparent p-0 text-left focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-blue-500"
    :aria-label="'Perbesar gambar: ' + props.alt"
    @click.stop="openImage"
  >
    <img :src="props.src" :alt="props.alt" :class="props.previewClass" />
    <span class="pointer-events-none absolute bottom-2 right-2 rounded-full bg-slate-950/80 px-2.5 py-1 text-[9px] font-semibold text-white opacity-0 shadow transition-opacity group-hover:opacity-100 group-focus-visible:opacity-100">
      Klik untuk perbesar
    </span>
  </button>

  <Teleport to="body">
    <div
      v-if="isOpen"
      ref="overlay"
      class="fixed inset-0 z-[99999] flex items-center justify-center bg-slate-950/90 p-6 backdrop-blur-sm"
      role="dialog"
      aria-modal="true"
      :aria-label="'Gambar diperbesar: ' + props.alt"
      tabindex="-1"
      @click.self.stop="closeImage"
      @keydown.esc.stop.prevent="closeImage"
    >
      <button
        type="button"
        class="absolute right-5 top-5 rounded-full border border-white/20 bg-white/10 px-4 py-2 text-sm font-semibold text-white shadow-lg hover:bg-white/20 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-white"
        @click.stop="closeImage"
      >
        Tutup <span class="ml-1 text-xs text-slate-300">Esc</span>
      </button>

      <figure class="m-0 flex max-h-full max-w-full flex-col items-center gap-3" @click.stop>
        <img
          :src="props.src"
          :alt="props.alt"
          class="block max-h-[86vh] max-w-[94vw] rounded-lg object-contain shadow-2xl"
        />
        <figcaption class="text-center text-xs text-slate-300">
          Tekan Esc atau klik area gelap untuk menutup
        </figcaption>
      </figure>
    </div>
  </Teleport>
</template>
