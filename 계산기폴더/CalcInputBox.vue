<template>
<div>
        <h2>{{title}}</h2>
        <span>
            <input v-model.number = "num1"> 
            {{operator}}
            <input v-model.number = "num2">
        </span>
        <button @click="calc">=</button>
        <div>결과 : {{result}}</div>
</div>    
</template>

<script>
export default {
    props:{
       title : {
            type: String
        },
        operator: {
            type: String,
            required: true
        }
    },
    data() {
        return {
            num1 : '',
            num2 : '',
            result : ''
        }
    },
    methods : {
        calc(){
            if(this.operator == "+"){
                this.addCal();
            }else if(this.operator == "-"){
                this.subCal();
            }else if(this.operator == "*"){
                this.mulCal();
            }else if(this.operator == "/"){
                this.divCal();
            }
            return;
        },
        addCal(){
            this.result = this.num1 + this.num2
        },
        subCal(){
            this.result = this.num1 - this.num2
        },
        mulCal(){
            this.result = this.num1 * this.num2
        },
        divCal(){
            this.result = this.num1 / this.num2
        }
    }  
};
</script>

<style/>