<template>
  <div class="home">
    <my-button />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import MyButton from '../components/MyButton.vue';

@Component({
  components: {
    MyButton,
  },
})
export default class Home extends Vue {}
</script>
