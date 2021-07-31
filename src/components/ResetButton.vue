<template>
  <button @click="onClick">Reset</button>
</template>

<script lang="ts">
import {Component, Emit, Prop, Vue} from "vue-property-decorator";

@Component
export default class ResetButton extends Vue {
  @Prop({required: true}) // required: trueによって値を必須にする
    public initialValue!: string; // 変数名: 型名;

  // モデルのバインドの為に必要
  @Prop()
  public value!: string;

  // モデルのバインドの為に必要
  @Emit()
  public input(value: string){

  }

  public onClick(){
    this.input(this.initialValue);
  }
}
</script>