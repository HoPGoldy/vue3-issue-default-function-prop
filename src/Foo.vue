<template>
<!-- The default value in the template is correct -->
default prop fetchData: {{defaultFunc}}
</template>

<script setup lang="ts">
import { defaultFunc } from './service';
import type { DefaultFunc } from './service';

interface Props {
  fetchData?: DefaultFunc
}

// set default function prop
const props = withDefaults(defineProps<Props>(), {
  fetchData: defaultFunc
});

// Why it's the return value, not the function itself here?
console.log('======> default prop fetchData:', props.fetchData);
</script>