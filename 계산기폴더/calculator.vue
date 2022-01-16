<template>
<div>
    <h1>사칙연산 계산기</h1>
    <h2>더하기</h2>
    <input v-model.number = "num1"> +
    <input v-model.number = "num2">
    <button v-on:click="addCal">=</button>
    <div>결과 : {{result}}</div>
    <h2>빼기</h2>
    <input v-model.number = "num3"> -
    <input v-model.number = "num4">
    <button v-on:click="subCal">=</button>
    <div>결과 : {{result1}}</div>
    <h2>곱하기</h2>
    <input v-model.number = "num5"> *
    <input v-model.number = "num6">
    <button v-on:click="mulCal">=</button>
    <div>결과 : {{result2}}</div>
    <h2>나누기</h2>
    <input v-model.number = "num7"> /
    <input v-model.number = "num8">
    <button v-on:click="divCal">=</button>
    <div>결과 : {{result3}}</div>  
</div>    
</template>

<script>
export default {
  data() {
            num1 : ''
            num2 : ''
            result : ''
            result1 : ''
            result2 : ''
            result3 : ''
         
        },
        methods : {
            addCal:function(){
                this.result = this.num1 + this.num2
            },
            subCal:function(){
                this.result1 = this.num3 - this.num4
            },
            mulCal:function(){
                this.result2 = this.num5 * this.num6
            },
            divCal:function(){
                this.result3 = this.num7 / this.num8
            }
        }  
};
</script>

<style>

</style>