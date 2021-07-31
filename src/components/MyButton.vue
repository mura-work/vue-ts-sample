<template>
  <button @click="onClick">MyButton</button>
</template>

<script lang="ts">
import {Component, Emit, Prop, Vue} from "vue-property-decorator";
import { component } from "vue/types/umd";

@Component
export default class MyButton extends Vue{
  @Prop()
  public greet?: string; // ?は値が設定されないケースもあるということ
                         // 値が必ず設定されるのであれば!をつける

  public onClick() {
    alert(this.greet);
    this.click();
  }

  @Emit()
  public click(){}
}
</script>