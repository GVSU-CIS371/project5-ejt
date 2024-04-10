<template>
  <v-card>
    <v-card-title>
      {{ product.data.name }}
    </v-card-title>
    <v-card-subtitle>
      {{ product.data.category }}
    </v-card-subtitle>
    <v-spacer>
      <v-img max-height="128":src="product.data.image"></v-img>
    </v-spacer>
    <v-card-text>
      {{ product.data.description }}
    </v-card-text>
    <v-rating
    :model-value="product.data.rating"
    color="blue-darken-4"
    readonly></v-rating>
  </v-card>
</template>

<script lang="ts" setup>
import { ProductDoc } from '../types/product';
import { defineProps } from "vue"
defineProps<{
  product: ProductDoc
}>();
</script>
