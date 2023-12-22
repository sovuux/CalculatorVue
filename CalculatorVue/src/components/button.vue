<template>
  <button :class="classButton">
    {{ content }}
  </button>
</template>

<script>
export default {
  props: {
    classButton: {
      type: String,
      required: true
    },
    content: {
      type: String,
      required: true
    },
    click: {
      type: Function,
      required: true
    }
  }
};
</script>

<style scoped>
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

    .button-memory {
        background-color: rgb(134, 134, 134);
        border: 0.5px solid rgb(158, 157, 157);
    }

    .button-memory:hover {
        background-color:  rgb(187, 187, 187);
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