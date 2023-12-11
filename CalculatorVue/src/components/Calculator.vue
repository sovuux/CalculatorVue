<template> 
    <div class="calculator-interface">
      <div class="textbox">
        <p>{{result}}</p>
      </div>
      <div class="line"></div>
      <div class="buttons">
        <!-- <button @click="mcClick" class="button-memory">MC</button>
        <button @click="mrClick" class="button-memory">MR</button>
        <button @click="mplusClick" class="button-memory">M+</button>
        <button @click="mminusClick" class="button-memory">M-</button>
        <button @click="percentClick" class="button-basic">%</button>
        <button @click="ceClick" class="button-basic">CE</button>
        <button @click="cClick" class="button-basic">C</button>
        <button @click="symbolClick" class="button-basic button-symbol"><img class="symbol-image" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADIAAAAyCAYAAAAeP4ixAAAACXBIWXMAAAsTAAALEwEAmpwYAAABb0lEQVR4nO2YQUoDQRBFn6BrQXBIQBeC4A1c5QoeQG+gC28QD+HOpUs14M6VpzCL5AAhIIoYQXAhtgi1aM0w6Wl7YqWtBw2BqWr606k/NQWGYRiGYfxvuoBTsF6Aa2AnRsQB8KFAhPPWE7BZR0QHeJPkY/6eFnAl57kMTdoGHiTpFD205UyTkOA1YCgJN8AyunCyKlkBbiWwD6yiDzdLyBJwLkHjugWlSciJBLwCu+jFVQnZF5t9B/YiNj8EioC4QmIbEdL5pc0eeTVVJaaQGCc5sZQK2QLu5cFZ5MbrwJ3sMRCLnBXz9U6IZUpISputEpNSxJSQJmy2TExqEd+E+DY7AjZIh18H/R+/Q8yglpBuwzbr30LKm1AhpMwAYsnvrzWvYm8FWrNq+/VrIrUYN68XYllhpxTjsm5Rsmoas2rjs/qwyuZTN6vhw6KMg54XeUDXBnpynoscRqaPsf2hliH2RG4iZZNrGIZhGAYa+AQu6kng3Jtj4AAAAABJRU5ErkJggg==" alt=""></button>
        <button @click="sinClick" class="button-basic">sin</button>
        <button @click="cosClick" class="button-basic">cos</button>
        <button @click="tgClick" class="button-basic">tg</button>
        <button @click="arcTgClick" class="button-basic">arctg</button>
        <button @click="logClick" class="button-basic">log</button>
        <button @click="lnClick" class="button-basic">ln</button>
        <button @click="factorialClick" class="button-basic">!</button>
        <button @click="powClick" class="button-basic">xʸ</button>
        <button @click="reverseClick" class="button-basic">¹/x</button>
        <button @click="sqrClick" class="button-basic">x²</button>
        <button @click="sqrtClick" class="button-basic">²√x</button>
        <button @click="divideClick" class="button-basic button-operation">÷</button>
        <button @click="sevenClick" class="button-basic">7</button>
        <button @click="eightClick" class="button-basic">8</button>
        <button @click="nineClick" class="button-basic">9</button>
        <button @click="multiplyClick" class="button-basic button-operation">×</button>
        <button @click="fourClick" class="button-basic">4</button>
        <button @click="fiveClick" class="button-basic">5</button>
        <button @click="sixClick" class="button-basic">6</button>
        <button @click="subtractClick" class="button-basic button-operation">-</button>
        <button @click="oneClick" class="button-basic">1</button>
        <button @click="twoClick" class="button-basic">2</button>
        <button @click="threeClick" class="button-basic">3</button>
        <button @click="plusClick" class="button-basic button-operation">+</button>
        <button @click="expClick" class="button-basic">eˣ</button>
        <button @click="zeroClick" class="button-basic">0</button>
        <button @click="dotClick" class="button-basic">,</button>
        <button @click="equalClick" class="button-basic button-equal">=</button> -->
        <buttonImport  :content="'content'" :classButton="'button-basic'"/>
      </div> 
    </div>
  </template>
  
<script>
    import { VueElement } from 'vue'
    import buttonImport from './button.vue'
    export default {
      components: {
        buttonImport
      },
      data(){
          return {
          result:' ',
          memoryValue: 0.0,
          number1: 0.0,
          number2: 0.0,
          buttonMassive: [
                {click:"mcClick", class:"button-memory", content:"MC"},
                {click:"mrClick", class:"button-memory", content:"MR"},
                {click:"mplusClick", class:"button-memory", content:"M+"},
                {click:"mminusClick", class:"button-memory", content:"M-"},
                {click:"percentClick", class:"button-basic", content:"%"},
                {click:"ceClick", class:"button-basic", content:"CE"},
                {click:"cClick", class:"button-basic", content:"C"},
                {click:"symbolClick", class:"button-basic button-symbol", content:"!@!"},
                {click:"sinClick", class:"button-basic", content:"sin"},
                {click:"cosClick", class:"button-basic", content:"cos"},
                {click:"tgClick", class:"button-basic", content:"tg"},
                {click:"arcTgClick", class:"button-basic", content:"arctg"},
                {click:"logClick", class:"button-basic", content:"log"},
                {click:"lnClick", class:"button-basic", content:"ln"},
                {click:"factorialClick", class:"button-basic", content:"!"},
                {click:"powClick", class:"button-basic", content:"xʸ"},
                {click:"reverseClick", class:"button-basic", content:"¹/x"},
                {click:"sqrClick", class:"button-basic", content:"x²"},
                {click:"sqrtClick", class:"button-basic", content:"²√x"},
                {click:"divideClick", class:"button-basic button-operation", content:"÷"},
                {click:"sevenClick", class:"button-basic", content:"7"},
                {click:"eightClick", class:"button-basic", content:"8"},
                {click:"nineClick", class:"button-basic", content:"9"},
                {click:"multiplyClick", class:"button-basic button-operation", content:"×"},
                {click:"fourClick", class:"button-basic", content:"4"},
                {click:"fiveClick", class:"button-basic", content:"5"},
                {click:"sixCLick", class:"button-basic", content:"6"},
                {click:"subtractClick", class:"button-basic button-operation", content:"-"},
                {click:"oneClick", class:"button-basic", content:"1"},
                {click:"twoClick", class:"button-basic", content:"2"},
                {click:"threeClick", class:"button-basic", content:"3"},
                {click:"plusClick", class:"button-basic button-operation", content:"+"},
                {click:"expClick", class:"button-basic", content:"eˣ"},
                {click:"zeroClick", class:"button-basic", content:"0"},
                {click:"dotClick", class:"button-basic", content:","},
                {click:"equalClick", class:"button-basic button-equal", content:"="},
            ]
          }
      },

      mounted() {
        this.result = '0'
      },

      methods: {
        zeroClick() {
            if(!this.result.startsWith('0')) {
              this.result += '0'
            }
            else {
              this.result = this.result.slice(1)
              this.result += '0'
            }
        },
  
        oneClick() {
          if(!this.result.startsWith('0')) {
            this.result += '1'
          }
          else {
            this.result = this.result.slice(1)
            this.result += '1'
          }
        },
  
        twoClick() {
          if(!this.result.startsWith('0')) {
            this.result += '2'
          }
          else {
            this.result = this.result.slice(1)
            this.result += '2'
          }
        },
  
        threeClick() {
          if(!this.result.startsWith('0')) {
            this.result += '3'
          }
          else {
            this.result = this.result.slice(1)
            this.result += '3'
          }
        },
  
        fourClick() {
          if(!this.result.startsWith('0')) {
            this.result += '4'
          }
          else {
            this.result = this.result.slice(1)
            this.result += '4'
          }
        },
  
        fiveClick() {
          if(!this.result.startsWith('0')) {
            this.result += '5'
          }
          else {
            this.result = this.result.slice(1)
            this.result += '5'
          }
        },
  
        sixClick() {
          if(!this.result.startsWith('0')) {
            this.result += '6'
          }
          else {
            this.result = this.result.slice(1)
            this.result += '6'
          }
        },
  
        sevenClick() {
          if(!this.result.startsWith('0')) {
            this.result += '7'
          }
          else {
            this.result = this.result.slice(1)
            this.result += '7'
          }
        },
  
        eightClick() {
          if(!this.result.startsWith('0')) {
            this.result += '8'
          }
          else {
            this.result = this.result.slice(1)
            this.result += '8'
          }
        },
  
        nineClick() {
          if(!this.result.startsWith('0')) {
            this.result += '9'
          }
          else {
            this.result = this.result.slice(1)
            this.result += '9'
          }
        },
  
        mcClick() {
          this.memoryValue = 0.0
        },
  
        mrClick() {
          if(!this.result.startsWith('0')) {
            this.result += parseFloat(this.memoryValue)
          }
          else {
            this.result = parseFloat(this.memoryValue)
          }
        },
  
        mplusClick() {
          this.memoryValue += parseFloat(this.result)
        },
  
        mminusClick() {
          this.memoryValue -= parseFloat(this.result)
        },
  
        percentClick() {
          const basicArray = this.result.split(/(\+|\-|\*|\/|\^)/);
          if (this.result.includes('+') || this.result.includes('-') || this.result.includes('*') || this.result.includes('/') || this.result.includes('^')) {
            const number1 = Number(basicArray[0]);
            const number2 = Number(basicArray[2]);
            const operator = basicArray[1];
            const percentNum = number1 * number2 / 100;
            this.result = number1.toString() + operator + percentNum.toString();
          } 
          else {
            this.result = '0';
          }
        },
  
        ceClick() {
          const operators = ['+', '-', '*', '/', '^'];
          let operatorIndex = this.result.length;
          if (this.result.includes('+') || this.result.includes('-') || this.result.includes('*') || this.result.includes('/') || this.result.includes('^')) {
            for (let i = this.result.length - 1; i >= 0; i--) {
              if (operators.includes(this.result[i])) {
                operatorIndex = i;
                break;
              }
            }
            this.result = this.result.substr(0, operatorIndex);
          }
          else {
          this.result = '0'
          }
        },
  
        symbolClick() {
          this.result = this.result.slice(0, -1)
          if (this.result.length < 1) {
            this.result += '0'
          }
        },
  
        cClick() {
          this.result = '0';
        },
  
        sinClick() {
          this.result = (Math.sin(this.result)).toString()
        },
  
        cosClick() {
          this.result = (Math.cos(this.result)).toString()
        },
  
        tgClick() {
          this.result = (Math.tan(this.result)).toString()
        },
  
        arcTgClick() {
          this.result =( Math.atan(this.result)).toString()
        },
              
        logClick() {
          this.result = (Math.log(this.result)).toString()
        },
  
        lnClick() {
          this.result = (Math.log10(this.result)).toString()
        },
  
        factorialClick() {
          const num = Number(this.result)
          let factorial = 1
          if (Number.isInteger(num) && num > 0) {
            for (let i = 1; i <= num; i++) {
              factorial *= i;
            }
            this.result = factorial.toString()
          } 
        },
  
        powClick() {
          this.result += '^'
        },
  
        reverseClick() {
          this.result = (1 / this.result).toString()
        },
  
        sqrClick() {
          this.result = Math.pow(this.result, 2)
        },
  
        sqrtClick() {
          this.result = Math.sqrt(this.result)
        },
  
        divideClick() {
          this.result += '/'
        },
  
        multiplyClick() {
          this.result += '*'
        },
  
        subtractClick() {
          if (!this.result.startsWith('0')) {
            this.result += '-'
          }
          else {
            this.result = ''
            this.result += '-0.'
          }
        },
  
        plusClick() {
          this.result += '+'
        },
  
        expClick() {
          this.result = Math.exp(this.result)
        },
  
        dotClick() {
          this.result += '.'
        },
  
        equalClick() {
          const basicArray = this.result.split(/(\+|\-|\*|\/|\^)/)
          const number1 = Number(basicArray[0]) //число 1
          const number2 = Number(basicArray[2]) //число 2
          const operation = basicArray[1] //оператор
          switch(operation) {
            case '+': {
              this.result = number1 + number2;
            }
            break;
                          
            case '-': {
              this.result = number1 - number2;
            }
            break;
  
            case '*': {
              this.result = number1 * number2;
            }
            break;
  
            case '/': {
              this.result = number1 / number2;
            }
            break;
  
            case '^': {
              this.result = Math.pow(number1, number2);
            }
            break;
  
            default: {
              return this.result;
            }
          }
        }
      }
    }
</script>
  
<style>
    
    .line {
      border: 1px solid black;
      margin-top: 5px;
    }
    .textbox p {
      margin-top: 10px;
      width: 268px;
      height: 50px;
      text-align: right;
      padding-right: 5px;
      font-size: 26px;
    }
  
    .calculator-interface {
      border: 2px solid black;
      border-radius: 10px;
      align-items: center;
      position: relative;
      left: 50%;
    }
  
    ::selection {
      background-color: rgb(255, 187, 60);
      color: rgb(58, 57, 57);
    }
  
    .buttons {
      margin-top: 5px;
      display: grid; 
      grid-template-columns: repeat(4, 1fr);
      justify-items: center;
      user-select: none;
      align-items: center;
    }
</style>