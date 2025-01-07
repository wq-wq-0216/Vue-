<template>
  <Suspense>
    <template #default>
      <HelloWorldComponent />
    </template>
    <template #fallback>
      <div>加载中...</div>
    </template>
  </Suspense>
</template>

<script>
import { defineAsyncComponent } from 'vue';

export default {
  components: {
    HelloWorldComponent: defineAsyncComponent(() => import('@/components/HelloWorld.vue'))
  }
};
</script>
