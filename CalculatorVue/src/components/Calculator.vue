<template> 
    <div class="calculator-interface">
      <div class="textbox">
        <p>{{result}}</p>
      </div>
      <div class="line"></div>
      <div class="buttons">
        <ButtonsContainer
          @mcClick="mcClick"
          @mrClick="mrClick"
          @mplusClick="mplusClick"
          @mminusClick="mminusClick"
          @percentClick="percentClick"
          @ceClick="ceClick"
          @cClick="cClick"
          @symbolClick="symbolClick"
          @sinClick="sinClick"
          @cosClick="cosClick"
          @tgClick="tgClick"
          @arcTgClick="arcTgClick"
          @logClick="logClick"
          @lnClick="lnClick"
          @factorialClick="factorialClick"
          @powClick="powClick"
          @reverseClick="reverseClick"
          @sqrClick="sqrClick"
          @sqrtClick="sqrtClick"
          @divideClick="divideClick" 
          @sevenClick="sevenClick"
          @eightClick="eightClick"
          @nineClick="nineClick"
          @multiplyClick="multiplyClick"
          @fourClick="fourClick"
          @fiveClick="fiveClick"
          @sixClick="sixClick"
          @subtractClick="subtractClick"
          @oneClick="oneClick"
          @twoClick="twoClick"
          @threeClick="threeClick"
          @plusClick="plusClick"
          @expClick="expClick"
          @zeroClick="zeroClick"
          @dotClick="dotClick"
          @equalClick="equalClick"
        />
      </div> 
    </div>
  </template>
  
<script>
    import { VueElement } from 'vue'
    import ButtonsContainer from './ButtonsContainer.vue'
    export default {
      components: {
        ButtonsContainer
      },
      data(){
          return {
          result:' ',
          memoryValue: 0.0,
          number1: 0.0,
          number2: 0.0,
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