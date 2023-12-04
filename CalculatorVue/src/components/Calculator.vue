<template> 
    <div class="calculator_interface">
      <div class="textbox">
        <p>{{result}}</p>
      </div>
      <div class="line"></div>
      <div class="buttons">
        <button @click="mcClick"  class="button_memory">MC</button>
        <button @click="mrClick" class="button_memory">MR</button>
        <button @click="mplusClick" class="button_memory">M+</button>
        <button @click="mminusClick" class="button_memory">M-</button>
        <button @click="percentClick" class="button_basic">%</button>
        <button @click="ceClick" class="button_basic">CE</button>
        <button @click="cClick" class="button_basic">C</button>
        <button @click="symbolClick" class="button_basic button_symbol"><img class="symbol_image" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADIAAAAyCAYAAAAeP4ixAAAACXBIWXMAAAsTAAALEwEAmpwYAAABb0lEQVR4nO2YQUoDQRBFn6BrQXBIQBeC4A1c5QoeQG+gC28QD+HOpUs14M6VpzCL5AAhIIoYQXAhtgi1aM0w6Wl7YqWtBw2BqWr606k/NQWGYRiGYfxvuoBTsF6Aa2AnRsQB8KFAhPPWE7BZR0QHeJPkY/6eFnAl57kMTdoGHiTpFD205UyTkOA1YCgJN8AyunCyKlkBbiWwD6yiDzdLyBJwLkHjugWlSciJBLwCu+jFVQnZF5t9B/YiNj8EioC4QmIbEdL5pc0eeTVVJaaQGCc5sZQK2QLu5cFZ5MbrwJ3sMRCLnBXz9U6IZUpISputEpNSxJSQJmy2TExqEd+E+DY7AjZIh18H/R+/Q8yglpBuwzbr30LKm1AhpMwAYsnvrzWvYm8FWrNq+/VrIrUYN68XYllhpxTjsm5Rsmoas2rjs/qwyuZTN6vhw6KMg54XeUDXBnpynoscRqaPsf2hliH2RG4iZZNrGIZhGAYa+AQu6kng3Jtj4AAAAABJRU5ErkJggg==" alt=""></button>
        <button @click="sinClick" class="button_basic">sin</button>
        <button @click="cosClick" class="button_basic">cos</button>
        <button @click="tgClick" class="button_basic">tg</button>
        <button @click="acrTgClick" class="button_basic">arctg</button>
        <button @click="logClick" class="button_basic">log</button>
        <button @click="lnClick" class="button_basic">ln</button>
        <button @click="factorialClick" class="button_basic">!</button>
        <button @click="powClick" class="button_basic">xʸ</button>
        <button @click="reverseClick" class="button_basic">¹/x</button>
        <button @click="sqrClick" class="button_basic">x²</button>
        <button @click="sqrtClick" class="button_basic">²√x</button>
        <button @click="divideClick" class="button_operation">÷</button>
        <button @click="sevenClick" class="button_basic">7</button>
        <button @click="eightClick" class="button_basic">8</button>
        <button @click="nineClick" class="button_basic">9</button>
        <button @click="multiplyClick" class="button_operation">×</button>
        <button @click="fourClick" class="button_basic">4</button>
        <button @click="fiveClick" class="button_basic">5</button>
        <button @click="sixClick" class="button_basic">6</button>
        <button @click="subtractClick" class="button_operation">-</button>
        <button @click="oneClick" class="button_basic">1</button>
        <button @click="twoClick" class="button_basic">2</button>
        <button @click="threeClick" class="button_basic">3</button>
        <button @click="plusClick" class="button_operation">+</button>
        <button @click="expClick" class="button_basic">eˣ</button>
        <button @click="zeroClick" class="button_basic">0</button>
        <button @click="dotClick" class="button_basic">,</button>
        <button @click="equalClick" class="button_basic button_equal">=</button>
      </div> 
    </div>
  </template>
  
  <script lang="ts">
    import { VueElement } from 'vue'

    export default {
      data() {
          return {
              result:' ',
              memoryValue: 0.0,
              numLock: false,
              number1: 0.0,
              number2: 0.0,
              basic: ['1', '2', '3', '4', '5', '6', '7', '8', '9', '0'],
              
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
          this.memoryValue = 0
        },
  
        mrClick() {
          this.result += Number(this.memoryValue)
        },
  
        mplusClick() {
          this.memoryValue += this.result
        },
  
        mminusClick() {
          this.memoryValue -= this.result
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
          this.result = Math.sin(this.result)
        },
  
        cosClick() {
          this.result = Math.cos(this.result)
        },
  
        tgClick() {
          this.result = Math.tan(this.result)
        },
  
        acrTgClick() {
          this.result = Math.atan(this.result)
        },
              
        logClick() {
          this.result = Math.log(this.result)
        },
  
        lnClick() {
          this.result = Math.log10(this.result)
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
          this.result = 1 / this.result
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
        },

        keyOne: function() {
          this.result += '1'
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
      font-size: 40px;
      padding-right: 5px;
      font-size: 26px;
    }
  
    .calculator_interface {
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
  
    .button_memory {
      background-color: rgb(134, 134, 134);
      border: 0.5px solid rgb(158, 157, 157);
      border-radius: 10px;
      padding: 10px;
      margin: 1px;
      font-size: 16px;
      width: 65px;
      height: 50px;
      -webkit-box-shadow: 0px -5px 5px -5px rgba(34, 60, 80, 0.45) inset;
      -moz-box-shadow: 0px -5px 5px -5px rgba(34, 60, 80, 0.45) inset;
      box-shadow: 0px -5px 5px -5px rgba(34, 60, 80, 0.45) inset;
    }
  
    .button_memory:hover {
      background-color:  rgb(187, 187, 187);
      color: black;
      cursor: pointer;
    }
  
    .button_basic {
        background-color: white;
        border: 0.5px solid rgb(158, 157, 157);
        border-radius: 10px;
        padding: 10px;
        margin: 1px;
        font-size: 16px;
        width: 65px;
        height: 50px;
        -webkit-box-shadow: 0px -5px 5px -5px rgba(34, 60, 80, 0.45) inset;
        -moz-box-shadow: 0px -5px 5px -5px rgba(34, 60, 80, 0.45) inset;
        box-shadow: 0px -5px 5px -5px rgba(34, 60, 80, 0.45) inset;
    }
  
    .button_basic:hover {
        background-color:   rgb(224, 224, 224);
        color: black;
        cursor: pointer;
    }
  
    .button_operation {
        background-color: orange;
        border: 0.5px solid rgb(158, 157, 157);
        border-radius: 10px;
        padding: 10px;
        margin: 1px;
        font-size: 16px;
        width: 65px;
        height: 50px;
        -webkit-box-shadow: 0px -5px 5px -5px rgba(34, 60, 80, 0.45) inset;
        -moz-box-shadow: 0px -5px 5px -5px rgba(34, 60, 80, 0.45) inset;
        box-shadow: 0px -5px 5px -5px rgba(34, 60, 80, 0.45) inset;
    }
  
    .button_operation:hover {
        background-color: rgb(255, 187, 60);
        color: black;
        cursor: pointer;
    }
  
    .symbol_image {
        width: 30px;
        height: 30px;
    }
  
    .button_symbol {
        margin-bottom: 0;
        align-items: center;
    }
  
    .button_equal {
        background-color: rgb(50, 50, 253);
        color: white;
    }
  
    .button_equal:hover {
        background-color: rgb(64, 64, 252);
        color: white;
    }
  </style>