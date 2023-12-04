<template>
    <button @click="emit(mcClick)"  class="button-memory">MC</button>
    <button @click="emit(mrClick)" class="button-memory">MR</button>
    <button @click="emit(mplusClick)" class="button-memory">M+</button>
    <button @click="emit(mminusClick)" class="button-memory">M-</button>
    <button @click="emit(percentClick)" class="button-basic">%</button>
    <button @click="emit(ceClick)" class="button-basic">CE</button>
    <button @click="emit(cClick)" class="button-basic">C</button>
    <button @click="emit(symbolClick)" class="button-basic button-symbol"><img class="symbol-image" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADIAAAAyCAYAAAAeP4ixAAAACXBIWXMAAAsTAAALEwEAmpwYAAABb0lEQVR4nO2YQUoDQRBFn6BrQXBIQBeC4A1c5QoeQG+gC28QD+HOpUs14M6VpzCL5AAhIIoYQXAhtgi1aM0w6Wl7YqWtBw2BqWr606k/NQWGYRiGYfxvuoBTsF6Aa2AnRsQB8KFAhPPWE7BZR0QHeJPkY/6eFnAl57kMTdoGHiTpFD205UyTkOA1YCgJN8AyunCyKlkBbiWwD6yiDzdLyBJwLkHjugWlSciJBLwCu+jFVQnZF5t9B/YiNj8EioC4QmIbEdL5pc0eeTVVJaaQGCc5sZQK2QLu5cFZ5MbrwJ3sMRCLnBXz9U6IZUpISputEpNSxJSQJmy2TExqEd+E+DY7AjZIh18H/R+/Q8yglpBuwzbr30LKm1AhpMwAYsnvrzWvYm8FWrNq+/VrIrUYN68XYllhpxTjsm5Rsmoas2rjs/qwyuZTN6vhw6KMg54XeUDXBnpynoscRqaPsf2hliH2RG4iZZNrGIZhGAYa+AQu6kng3Jtj4AAAAABJRU5ErkJggg==" alt=""></button>
    <button @click="emit(sinClick)" class="button-basic">sin</button>
    <button @click="emit(cosClick)" class="button-basic">cos</button>
    <button @click="emit(tgClick)" class="button-basic">tg</button>
    <button @click="emit(arcTgClick)" class="button-basic">arctg</button>
    <button @click="emit(logClick)" class="button-basic">log</button>
    <button @click="emit(lnClick)" class="button-basic">ln</button>
    <button @click="emit(factorialClick)" class="button-basic">!</button>
    <button @click="emit(powClick)" class="button-basic">xʸ</button>
    <button @click="emit(reverseClick)" class="button-basic">¹/x</button>
    <button @click="emit(sqrClick)" class="button-basic">x²</button>
    <button @click="emit(sqrtClick)" class="button-basic">²√x</button>
    <button @click="emit(divideClick)" class="button-basic button-operation">÷</button>
    <button @click="emit(sevenClick)" class="button-basic">7</button>
    <button @click="emit(eightClick)" class="button-basic">8</button>
    <button @click="emit(nineClick)" class="button-basic">9</button>
    <button @click="emit(multiplyClick)" class="button-basic button-operation">×</button>
    <button @click="emit(fourClick)" class="button-basic">4</button>
    <button @click="emit(fiveClick)" class="button-basic">5</button>
    <button @click="emit(sixClick)" class="button-basic">6</button>
    <button @click="emit(subtractClick)" class="button-basic button-operation">-</button>
    <button @click="emit(oneClick)" class="button-basic">1</button>
    <button @click="emit(twoClick)" class="button-basic">2</button>
    <button @click="emit(threeClick)" class="button-basic">3</button>
    <button @click="emit(plusClick)" class="button-basic button-operation">+</button>
    <button @click="emit(expClick)" class="button-basic">eˣ</button>
    <button @click="emit(zeroClick)" class="button-basic">0</button>
    <button @click="emit(dotClick)" class="button-basic">,</button>
    <button @click="emit(equalClick)" class="button-basic button-equal">=</button>
</template>

<script>
    export default {
        methods: {
            emit(eventName) {
                this.$emit(eventName)
            }
        },
        computed: {
            mcClick() {
                return 'mcClick'
            },
            mrClick() {
                return 'mrClick'
            },
            mplusClick() {
                return 'mplusClick'
            },
            mminusClick() {
                return 'mminusClick'
            },
            percentClick() {
                return 'percentClick'
            },
            ceClick() {
                return 'ceClick'
            },
            cClick() {
                return 'cClick'
            },
            symbolClick() {
                return 'symbolClick'
            },
            sinClick() {
                return 'sinClick'
            },
            cosClick() {
                return 'cosClick'
            },
            tgClick() {
                return 'tgClick'
            },
            arcTgClick() {
                return 'arcTgClick'
            },
            logClick() {
                return 'logClick'
            },
            lnClick() {
                return 'lnClick'
            },
            factorialClick() {
                return 'factorialClick'
            },
            powClick() {
                return 'powClick'
            },
            reverseClick() {
                return 'reverseClick'
            },
            sqrClick() {
                return 'sqrClick'
            },
            sqrtClick() {
                return 'sqrtClick'
            },
            divideClick() {
                return 'divideClick'
            },
            sevenClick() {
                return 'sevenClick'
            },
            eightClick() {
                return 'eightClick'
            },
            nineClick() {
                return 'nineClick'
            },
            multiplyClick() {
                return 'multiplyClick'
            },
            fourClick() {
                return 'fourClick'
            },
            fiveClick() {
                return 'fiveClick'
            },
            sixClick() {
                return 'sixClick'
            },
            subtractClick() {
                return 'subtractClick'
            },
            oneClick() {
                return 'oneClick'
            },
            twoClick() {
                return 'twoClick'
            },
            threeClick() {
                return 'threeClick'
            },
            plusClick() {
                return 'plusClick'
            },
            expClick() {
                return 'expClick'
            },
            zeroClick() {
                return 'zeroClick'
            },
            dotClick() {
                return 'dotClick'
            },
            equalClick() {
                return 'equalClick'
            }
        }
    }
</script>

<style>
.button-memory {
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
  
    .button-memory:hover {
      background-color:  rgb(187, 187, 187);
      color: black;
      cursor: pointer;
    }
  
    .button-basic {
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
  
    .button-basic:hover {
        background-color:   rgb(224, 224, 224);
        color: black;
        cursor: pointer;
    }
  
    .button-operation {
        background-color: orange;
        border: 0.5px solid rgb(158, 157, 157);
        
    }
  
    .button-operation:hover {
        background-color: rgb(255, 187, 60);
    }
  
    .symbol-image {
        width: 30px;
        height: 30px;
    }
  
    .button-symbol {
        margin-bottom: 0;
        align-items: center;
    }
  
    .button-equal {
        background-color: rgb(11, 11, 172);
        color: white;
    }
  
    .button-equal:hover {
        background-color: rgb(27, 27, 219);
        color: white;
    }
</style>