<script setup lang="ts">
import { VxButton, VxEmptyState, VxSiteShell } from '@vex/ui'
import RootAccount from '@/components/RootAccount.vue'
import { useRoute } from 'vue-router'

const route = useRoute()
</script>

<template>
  <VxSiteShell site="root">
    <template #account><RootAccount /></template>
    <VxEmptyState code="404" title="Not found">
      Nothing lives at <span class="vx-mono">{{ route.path }}</span>. It was probably never real.
      <template #actions>
        <VxButton variant="primary" to="/">Back to the links</VxButton>
      </template>
    </VxEmptyState>
  </VxSiteShell>
</template>
