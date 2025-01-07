<template>
  <div>
    <div>
      <defaultSlot>
        <p>默认插槽</p>
      </defaultSlot>
    </div>
    <div>
      <nameSlot>
        <p>默认插槽</p>
        <template v-slot:content>具名插槽</template>
      </nameSlot>
    </div>

    <div>
      <FieldSlot> 
        <!-- 把v-slot的值指定为作⽤域上下⽂对象 -->
        <template v-slot:footer="slotProps">
          来⾃⼦组件数据：{{slotProps.testProps}}
        </template>

        <!-- <template v-slot:footer><p>yes</p></template> -->
      </FieldSlot>
    </div>
  </div>
</template>

<script setup>
import nameSlot from './components/nameSlot.vue';
import defaultSlot from './components/defaultSlot.vue';
import FieldSlot from './components/fieldSlot.vue';
</script>