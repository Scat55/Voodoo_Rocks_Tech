<script setup lang="ts">
import { Container } from '@/shared/container';

interface Props {
  title: string;
  description: string;
}
const props = defineProps<Props>();

const { title, description } = props;
</script>

<template>
  <Container>
    <div class="card">
      <span class="card__title">{{ title }}</span>
      <p class="card__description">{{ description }}</p>
    </div>
  </Container>
</template>

<style scoped lang="scss">
.card {
  max-width: 320px;
  padding: 1rem;
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 20px 20px 30px rgba(0, 0, 0, 0.05);

  &__title {
    font-weight: 600;
    color: rgb(31 41 55);
  }
  &__description {
    margin-top: 1rem;
    font-size: 0.875rem;
    line-height: 1.25rem;
  }
}
</style>
