<template>
  <div class="home">
    <p>{{greetText}}</p>
    <p>挨拶した回数: {{count}}回</p>
    <my-button @click="onMyButtonClicked" :greet="greetText" /><br>
    <reset-button v-model="greetText" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import MyButton from '../components/MyButton.vue';
import ResetButton from '../components/ResetButton.vue';

@Component({
  components: {
    MyButton,
    ResetButton,
  },
})
export default class Home extends Vue {
  private count: number = 0;

  public greetText: string = "Hello";

  public onMyButtonClicked(count: number) {
    this.count = count;
    this.greetText = "こんにちわ"
  }
}
</script>
