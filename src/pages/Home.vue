<script setup lang="ts">
import { Container } from '@/shared/container';
import { Input } from '@/shared/input';
</script>

<template>
  <header class="header">
    <Container>
      <div class="header__input">
        <svg class="header__input-icon" aria-hidden="true" viewBox="0 0 24 24">
          <g>
            <path
              d="M21.53 20.47l-3.66-3.66C19.195 15.24 20 13.214 20 11c0-4.97-4.03-9-9-9s-9 4.03-9 9 4.03 9 9 9c2.215 0 4.24-.804 5.808-2.13l3.66 3.66c.147.146.34.22.53.22s.385-.073.53-.22c.295-.293.295-.767.002-1.06zM3.5 11c0-4.135 3.365-7.5 7.5-7.5s7.5 3.365 7.5 7.5-3.365 7.5-7.5 7.5-7.5-3.365-7.5-7.5z"
            ></path>
          </g>
        </svg>
        <Input placeholder="Автор..." />
      </div>
    </Container>
  </header>
</template>

<style scoped lang="scss">
.header {
  display: flex;
  align-items: center;
  justify-content: center;
  &__input {
    line-height: 28px;
    position: relative;
    max-width: 350px;

    &-icon {
      position: absolute;
      top: 0.7rem;
      left: 0.8rem;
      fill: #9e9ea7;
      width: 1rem;
      height: 1rem;
    }
  }
}
</style>
