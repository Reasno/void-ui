<template>
  <button class="vd-button">
    <slot></slot>
  </button>
</template>

<script lang="ts">
import {
  Component,
  Emit,
  Inject,
  Model,
  Prop,
  Provide,
  Vue,
  Watch,
} from 'vue-property-decorator';

@Component
export default class VdButton extends Vue {}
</script>

