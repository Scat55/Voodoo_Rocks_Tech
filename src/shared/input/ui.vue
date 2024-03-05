<script setup lang="ts">
interface Props {
  name?: string;
  value?: string;
  type?: string;
  placeholder?: string;
  disabled?: boolean;
  required?: boolean;
}

const props = defineProps<Props>();

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
  width: 18.125rem;
  background-color: #f5f5f5;
  color: #242424;
  padding: 0.15rem 0.5rem;
  min-height: 2.5rem;
  font-size: 1.125rem;
  border-radius: 4px;
  outline: none;
  border: none;
  line-height: 1.15;
  box-shadow: 0px 0.625rem 1.25rem -1.125rem;

  &:focus {
    border-bottom: 2px solid #5b5fc7;
    border-radius: 4px 4px 2px 2px;
  }
  &:hover {
    outline: 1px solid lightgrey;
  }
}
</style>
