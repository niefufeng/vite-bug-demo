<template>
  <div>
    <br />

    <div>
      <span>current value: </span>
      <span>{{ data.int }}</span>
    </div>

    <br />

    <div>
      <span>current value type: </span>
      <strong>{{ dataType }}</strong>
    </div>

    <br />

    <!-- <label>
      <input type="radio" :value="1" v-model="data.int" />
      <span>1</span>
    </label>
    <label>
      <input type="radio" :value="2" v-model="data.int" />
      <span>2</span>
    </label>
    <label>
      <input type="radio" :value="3" v-model="data.int" />
      <span>2</span>
    </label> -->

    <select v-model="data.int">
      <option :value="1">1</option>
      <option :value="2">2</option>
      <option :value="3">3</option>
    </select>
  </div>
</template>

<script setup>
import { computed, reactive } from 'vue'

const data = reactive({
  int: 1
});

const dataType = computed(() => typeof data.int);
</script>

<style scoped>
select {
  padding: 0.5em 2em;
}
</style>