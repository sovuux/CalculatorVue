<template> 
    <div class="calcInterface">
      <div class="textbox">
        <p>{{result}}</p>
      </div>
      <div class="line"></div>
      <div class="buttons">
        <button @click="mcClick"  class="butMemory">MC</button>
        <button @click="mrClick" class="butMemory">MR</button>
        <button @click="mplusClick" class="butMemory">M+</button>
        <button @click="mminusClick" class="butMemory">M-</button>
        <button @click="percentClick" class="but">%</button>
        <button @click="ceClick" class="but">CE</button>
        <button @click="cClick" class="but">C</button>
        <button @click="symbolClick" class="but symbol"><img class="imgClear" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADIAAAAyCAYAAAAeP4ixAAAACXBIWXMAAAsTAAALEwEAmpwYAAABb0lEQVR4nO2YQUoDQRBFn6BrQXBIQBeC4A1c5QoeQG+gC28QD+HOpUs14M6VpzCL5AAhIIoYQXAhtgi1aM0w6Wl7YqWtBw2BqWr606k/NQWGYRiGYfxvuoBTsF6Aa2AnRsQB8KFAhPPWE7BZR0QHeJPkY/6eFnAl57kMTdoGHiTpFD205UyTkOA1YCgJN8AyunCyKlkBbiWwD6yiDzdLyBJwLkHjugWlSciJBLwCu+jFVQnZF5t9B/YiNj8EioC4QmIbEdL5pc0eeTVVJaaQGCc5sZQK2QLu5cFZ5MbrwJ3sMRCLnBXz9U6IZUpISputEpNSxJSQJmy2TExqEd+E+DY7AjZIh18H/R+/Q8yglpBuwzbr30LKm1AhpMwAYsnvrzWvYm8FWrNq+/VrIrUYN68XYllhpxTjsm5Rsmoas2rjs/qwyuZTN6vhw6KMg54XeUDXBnpynoscRqaPsf2hliH2RG4iZZNrGIZhGAYa+AQu6kng3Jtj4AAAAABJRU5ErkJggg==" alt=""></button>
        <button @click="sinClick" class="but">sin</button>
        <button @click="cosClick" class="but">cos</button>
        <button @click="tgClick" class="but">tg</button>
        <button @click="acrTgClick" class="but">arctg</button>
        <button @click="logClick" class="but">log</button>
        <button @click="lnClick" class="but">ln</button>
        <button @click="factorialClick" class="but">!</button>
        <button @click="powClick" class="but">xʸ</button>
        <button @click="reverseClick" class="but">¹/x</button>
        <button @click="sqrClick" class="but">x²</button>
        <button @click="sqrtClick" class="but">²√x</button>
        <button @click="divideClick" class="operation">÷</button>
        <button @click="sevenClick" class="but">7</button>
        <button @click="eightClick" class="but">8</button>
        <button @click="nineClick" class="but">9</button>
        <button @click="multiplyClick" class="operation">×</button>
        <button @click="fourClick" class="but">4</button>
        <button @click="fiveClick" class="but">5</button>
        <button @click="sixClick" class="but">6</button>
        <button @click="subtractClick" class="operation">-</button>
        <button @click="oneClick" @keyup.enter="keyOne" class="but">1</button>
        <button @click="twoClick" class="but">2</button>
        <button @click="threeClick" class="but">3</button>
        <button @click="plusClick" class="operation">+</button>
        <button @click="expClick" class="but">eˣ</button>
        <button @click="zeroClick" class="but">0</button>
        <button @click="dotClick" class="but">,</button>
        <button @click="equalClick" class="but equal">=</button>
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
              numbers: ['1', '2', '3', '4', '5', '6', '7', '8', '9', '0'],
              
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
          this.result = Number(this.memoryValue)
        },
  
        mplusClick() {
          this.memoryValue += this.result
        },
  
        mminusClick() {
          this.memoryValue -= this.result
        },
  
        percentClick() {
          const numbersArray = this.result.split(/(\+|\-|\*|\/|\^)/);
          if (this.result.includes('+') || this.result.includes('-') || this.result.includes('*') || this.result.includes('/') || this.result.includes('^')) {
            const number1 = Number(numbersArray[0]);
            const number2 = Number(numbersArray[2]);
            const operator = numbersArray[1];
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
          this.result += '-'
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
          const numbersArray = this.result.split(/(\+|\-|\*|\/|\^)/)
          const number1 = Number(numbersArray[0]) //число 1
          const number2 = Number(numbersArray[2]) //число 2
          const operation = numbersArray[1] //оператор
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
  
    .calcInterface {
      border: 2px solid black;
      border-radius: 10px;
      align-items: center;
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
  
    .butMemory {
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
  
    .butMemory:hover {
      background-color:  rgb(187, 187, 187);
      color: black;
      cursor: pointer;
    }
  
    .but {
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
  
    .but:hover {
        background-color:   rgb(224, 224, 224);
        color: black;
        cursor: pointer;
    }
  
    .operation {
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
  
    .operation:hover {
        background-color: rgb(255, 187, 60);
        color: black;
        cursor: pointer;
    }
  
    .imgClear {
        width: 30px;
        height: 30px;
    }
  
    .symbol {
        align-items: center;
    }
  
    .equal {
        background-color: rgb(50, 50, 253);
        color: white;
    }
  
    .equal:hover {
        background-color: rgb(64, 64, 252);
        color: white;
    }
  </style>