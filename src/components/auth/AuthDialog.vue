<template>
  <Teleport to="body">
    <div v-if="modelValue" v-bind="$attrs" class="blind" @click.self="$emit('modalClose')">
      <div class="vModal">
        <div class="modal-close text-end">
          <button type="button" class="modal-btn-close" @click="$emit('modalClose')">X</button>
        </div>
        <component :is="authViewComponents[viewMode]" @change-view="changeViewMode" />
        <div>{{ viewMode }}</div>
      </div>
    </div>
  </Teleport>
</template>

<script setup>
import { defineAsyncComponent, ref } from 'vue';

defineProps(['modelValue', 'update:modelValue'])
defineEmits(['modalClose'])
const viewMode = ref('SignIn')
const changeViewMode = (val) => {
  viewMode.value = val
}

const authViewComponents = {
  SignIn: defineAsyncComponent(() => import('./AuthSignIn.vue')),
  SignUp: defineAsyncComponent(() => import('./AuthSignUp.vue')),
  FindPassword: defineAsyncComponent(() =>
    import('./AuthFindPassword.vue'),
  ),
};

</script>
<style scoped></style>
