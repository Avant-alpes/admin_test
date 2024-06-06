<template>
  <div class="flex gap-8 flex-wrap">
    <VaSwitch
      v-model="value"
      style="--va-switch-checker-background-color: #252723"
      @change="toggleTheme"
      color="#5123a1"
      off-color="#ffd300"
    >
      <template #innerLabel>
        <div class="va-text-center">
          <VaIcon :name="value ? 'dark_mode' : 'light_mode'" />
        </div>
      </template>
    </VaSwitch>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref, watch } from 'vue'
import { useColors } from 'vuestic-ui'

export default defineComponent({
  setup() {
    const value = ref(true)
    const { applyPreset } = useColors()

    const toggleTheme = () => {
      if (value.value) {
        applyPreset('dark')
        document.body.classList.add('dark')
        document.body.classList.remove('light')
      } else {
        applyPreset('light')
        document.body.classList.add('light')
        document.body.classList.remove('dark')
      }
    }

    watch(value, toggleTheme, { immediate: true })

    return {
      value,
      toggleTheme,
    }
  },
})
</script>
