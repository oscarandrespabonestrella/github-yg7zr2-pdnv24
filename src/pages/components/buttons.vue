<script setup lang="ts">
import { ref } from 'vue';
import CodeBox from '../../components/CodeBox.vue';
</script>

<template>
  <div class="grid grid-cols-2">
    <CodeBox>
      <button type="button" class="btn btn-primary">Primary</button>
      <button type="button" class="btn btn-secondary">Secondary</button>
      <button type="button" class="btn btn-success">Success</button>
      <button type="button" class="btn btn-danger">Danger</button>
      <button type="button" class="btn btn-warning">Warning</button>
      <button type="button" class="btn btn-info">Info</button>
      <button type="button" class="btn btn-light">Light</button>
      <button type="button" class="btn btn-dark">Dark</button>
      <button type="button" class="btn btn-link">Link</button>
    </CodeBox>
    <CodeBox>
      <h2>rtreas</h2>
    </CodeBox>
  </div>
</template>
