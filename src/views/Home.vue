<template>
  <div class="home">
    <p>{{greetText}}</p>
    <my-button @click="onMyButtonClicked" :greet="greetText" />
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
export default class Home extends Vue {
  public greetText: string = "Hello";

  public onMyButtonClicked() {
    this.greetText = "こんにちわ"
  }
}
</script>
