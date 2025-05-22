<template>
    <div class="container">
        <img src="https://yesno.wtf/assets/no/19-2062f4c91189b1f88a9e809c10a5b0f0.gif" alt="No hubo ese placeholder"
            srcset="">
        <div class="container-2">

        </div>
        <div class="pregunta-container">
            <input v-model="pregunta" type="text" placeholder="Hazme una pregunta">
            <p>Recuerda terminar con el signo de pregunta '?'</p>
            <h2>{{ pregunta }}</h2>
            <h1>{{ respuesta }}</h1>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            pregunta: null,
            respuesta: null,

        }
    },
    watch: {
        pregunta(value, oldValue){
            // if(value.endsWith(, endPosition))
            console.log('Actual: '+value)
            console.log('Old: '+oldValue)
        }
    },
    mounted() {

    }

}
</script>

<style scoped>
.container-2,
img {
    /* todo el ancho y todo el alto*/
    height: 100vh;
    width: 100vw;
    max-height: 100%;
    max-width: 100%;
    /* como si fuera una marca de agua */
    position: fixed;
    left: 0px;
    top: 0px;
}

.container-2 {
    background-color: rgba(0, 0, 0, 0.829);

}

input {
    border: none;
    padding: 10px 15px;
    border-radius: 5px;
    width: 250px;
    margin-top: 50px;

}

input:focus {
    outline: none;
}

p {
    color: white;
    font-size: large;
}

h1,
h2 {
    color: #fff;
}

h2 {
    margin-top: 100px;
}

.pregunta-container {

    position: relative;
    /* color: #fff; */
}
</style>