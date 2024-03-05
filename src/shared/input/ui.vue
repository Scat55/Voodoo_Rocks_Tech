<script setup lang="ts">
interface Props {
  name?: string;
  value?: string;
  type?: string;
  placeholder?: string;
  disabled?: boolean;
  required?: boolean;
}

defineProps<Props>();

const emit = defineEmits(['update:value']);

const updateValue = (e: Event) => {
  emit('update:value', (e.target as HTMLInputElement).value);
};
</script>

<template>
  <div class="input-container">
    <input
      class="input"
      :type="type"
      :value="value"
      :name="name"
      :placeholder="placeholder"
      :disabled="disabled"
      :required="required"
      @input="updateValue"
    />
  </div>
</template>

<style scoped lang="scss">
.input-container {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 1rem;
}
.input {
  width: 100%;
  height: 40px;
  line-height: 28px;
  padding: 0 1rem;
  padding-left: 2.5rem;
  border: 2px solid transparent;
  border-radius: 8px;
  outline: none;
  font-size: 1rem;
  background-color: #f3f3f4;
  color: #0d0c22;
  transition: 0.3s ease;
  &::placeholder {
    color: #9e9ea7;
  }
  &:focus,
  &:hover {
    outline: none;
    border-color: rgba(135, 217, 255, 0.4);
    background-color: #fff;
    box-shadow: 0 0 0 4px rgb(234 76 137 / 10%);
  }
}
</style>
