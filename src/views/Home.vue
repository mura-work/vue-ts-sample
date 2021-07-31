<template>
  <div class="home">
    <my-button greet="Hello" />
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
