<script>
export default {
    name: 'RegisterForm',
    data() {
        return {
            nombre: '',
            correo: '',
            edad: '',
            mostrarResumen: false
        }
    },
    methods: {
        enviarFormulario() {
            if (this.nombre && this.correo && this.edad) {
                this.mostrarResumen = true;
            } else {
                alert('Por favor, completa todos los campos.');
            }
        },
        limpiarFormulario() {
            this.nombre = '';
            this.correo = '';
            this.edad = '';
            this.mostrarResumen = false;
        }
    }
}
</script>

<template>
<div class="container mt-5">
    <form @submit.prevent="enviarFormulario" v-if="!mostrarResumen">
        <div class="mb-3">
            <label for="nombreImput" class="form-label">Nombre:</label>
            <input type="text" class="form-control" id="
            nombreImput" v-model="nombre">
        </div>
        <div class="mb-3">
           <label for="correoImput" class="form-label">Correo:</label>
           <input type="email" class="form-control" id="
            correoImput" v-model="correo"> 
        </div>
        <div class="mb-3">
           <label for="edadImput" class="form-label">Edad:</label>
           <input type="number" class="form-control" id="
            edadImput" v-model="edad">
        </div>
        <button type="submit" class="btn btn-danger mt-3 p-3">Enviar</button>
    </form>

    <div class="card mt-4" v-if="mostrarResumen">
        <div class="card-header">
            Resumen de Registro
        </div>
        <ul class="list-group list-group-flush">
            <li class="list-group-item"><strong>Nombre:</strong> {{ nombre }}</li>
            <li class="list-group-item"><strong>Correo:</strong> {{ correo }}</li>
            <li class="list-group-item"><strong>Edad:</strong> {{ edad }}</li>
        </ul>
        <div class="card-footer">
            <button class="btn btn-danger" @click="limpiarFormulario">Limpiar Formulario</button>
        </div>
    </div>

</div>
</template>