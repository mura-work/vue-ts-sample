<template>
  <div class="home">
    <p>{{greetText}}</p>
    <my-button @click="onMyButtonClicked" :greet="greetText" /><br>
    <reset-button initialValue="Hello" v-model="greetText" />
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
  public greetText: string = "Hello";

  public onMyButtonClicked() {
    this.greetText = "こんにちわ"
  }
}
</script>
