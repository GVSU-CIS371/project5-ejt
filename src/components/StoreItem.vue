<template>
  <v-card class="flex-column">
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
    <v-container>
      <v-row>
        <v-spacer/>
        <b>Stock:</b>{{ product.data.stock }} items
        <v-spacer/>
        <b>Price:</b> ${{ product.data.price }}
        <v-spacer/>
      </v-row>
    </v-container>
    <v-row>
      <v-spacer/>
      <v-rating
      :model-value="product.data.rating"
      color="blue-darken-4"
      readonly>
      </v-rating>
      <v-spacer/>
    </v-row>
  </v-card>
</template>

<script lang="ts" setup>
import { ProductDoc } from '../types/product';
import { defineProps } from "vue"
defineProps<{
  product: ProductDoc
}>();
</script>
