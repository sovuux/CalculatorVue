<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
</script>

<template> 
    <div class="calcInterface">
        <div class="textbox">
            <input type="number" placeholder="0">
        </div>
        <div class="buttons">
            <button class="but">MC</button>
            <button class="but">MR</button>
            <button class="but">M+</button>
            <button class="but">M-</button>
            <button class="but">%</button>
            <button class="but">CE</button>
            <button class="but">C</button>
            <button class="but" id="symbol"><img id="imgClear" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADIAAAAyCAYAAAAeP4ixAAAACXBIWXMAAAsTAAALEwEAmpwYAAABb0lEQVR4nO2YQUoDQRBFn6BrQXBIQBeC4A1c5QoeQG+gC28QD+HOpUs14M6VpzCL5AAhIIoYQXAhtgi1aM0w6Wl7YqWtBw2BqWr606k/NQWGYRiGYfxvuoBTsF6Aa2AnRsQB8KFAhPPWE7BZR0QHeJPkY/6eFnAl57kMTdoGHiTpFD205UyTkOA1YCgJN8AyunCyKlkBbiWwD6yiDzdLyBJwLkHjugWlSciJBLwCu+jFVQnZF5t9B/YiNj8EioC4QmIbEdL5pc0eeTVVJaaQGCc5sZQK2QLu5cFZ5MbrwJ3sMRCLnBXz9U6IZUpISputEpNSxJSQJmy2TExqEd+E+DY7AjZIh18H/R+/Q8yglpBuwzbr30LKm1AhpMwAYsnvrzWvYm8FWrNq+/VrIrUYN68XYllhpxTjsm5Rsmoas2rjs/qwyuZTN6vhw6KMg54XeUDXBnpynoscRqaPsf2hliH2RG4iZZNrGIZhGAYa+AQu6kng3Jtj4AAAAABJRU5ErkJggg==" alt=""></button>
            <button class="but">sin</button>
            <button class="but">cos</button>
            <button class="but">tg</button>
            <button class="but">arctg</button>
            <button class="but">log</button>
            <button class="but">ln</button>
            <button class="but">!</button>
            <button class="but">xʸ</button>
            <button class="but">¹/x</button>
            <button class="but">x²</button>
            <button class="but">²√x</button>
            <button class="operation">÷</button>
            <button class="but">7</button>
            <button class="but">8</button>
            <button class="but">9</button>
            <button class="operation">×</button>
            <button class="but">4</button>
            <button class="but">5</button>
            <button class="but">6</button>
            <button class="operation">-</button>
            <button class="but">1</button>
            <button class="but">2</button>
            <button class="but">3</button>
            <button class="operation">+</button>
            <button class="but">eˣ</button>
            <button class="but">0</button>
            <button class="but">,</button>
            <button class="but" id="equal">=</button>
            
        </div> 
    </div>
</template>

<style>
    input[type="number"]::-webkit-inner-spin-button,
    input[type="number"]::-webkit-outer-spin-button {
        -webkit-appearance: none;
        margin: 0;
    }

    .calcInterface {
        border: 2px solid black;
        border-radius: 10px;
        position: absolute;
        top: 10px;
        left: 10px;
    }

    ::selection {
        background-color: rgb(255, 187, 60);
        color: rgb(58, 57, 57);
    }
    input[type="number"]  {
        width: 268px;
        height: 50px;
        text-align: right;
        font-size: 40px;
        border-top: 0;
        border-radius: 10px;
        padding-right: 5px;
        
    }
    
    .buttons {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        margin-top: 1px;
        justify-items: center;
        user-select: none;
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

    .operation:hover{
        background-color: rgb(255, 187, 60);
        color: black;
        cursor: pointer;
    }

    #imgClear {
        width: 30px;
        height: 30px;
    }

    #symbol {
        align-items: center;
    }

    #equal {
        background-color: rgb(50, 50, 253);
        color: white;
    }

    #equal:hover {
        background-color: rgb(64, 64, 252);
        color: white;
    }
</style>


