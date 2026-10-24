<script setup lang="ts">
import { VxAccount, VxMenuItem } from '@vex/ui'
</script>

<!-- The header's account menu, with root's own Profile entry (vex-ui's menu has none in the pinned version). -->
<template>
  <VxAccount v-slot="{ close }">
    <VxMenuItem to="/account" @click="close()">Profile</VxMenuItem>
  </VxAccount>
</template>
