# Formulario de Registro con Vue y Vite M6AE1 - ABPRO1
Este proyecto consiste en un formulario de registro simple desarrollado con Vue 3 y Vite, utilizando Bootstrap para los estilos. La aplicación permite al usuario ingresar su nombre, correo electrónico y edad. Una vez completado el formulario, se muestra un resumen de la información ingresada.

---
# Integrantes:
- María Teresa de la Fuente
- Daniela Garrido
- Gonzalo Román 
---
### Repositorio: https://github.com/GRomanD3v/M6AE1-ABPRO1.git

---
### Aprendizaje Esperado
Describir los aspectos fundamentales de un framework orientado a
componentes para el desarrollo de una aplicación Front-End

---

### Requerimientos de la actividad
El proyecto se construyó siguiendo los siguientes requerimientos:

- Tecnologías: Se utilizó Vue.js (instalado vía Vite) y Bootstrap 5 para el diseño y la interfaz de usuario.

- Binding de datos (v-model): La directiva v-model se usó para crear un enlace bidireccional entre los campos del formulario (```<input>```) y las propiedades de datos en el componente (nombre, correo y edad). Esto asegura que cualquier cambio en el formulario se refleje instantáneamente en la lógica de la aplicación.

- Renderizado condicional (v-if): La directiva v-if se implementó para controlar la visibilidad de dos secciones:

  1. El formulario de registro (```<form>```) se muestra solo si la variable de estado mostrarResumen es false.

  2. El resumen de datos (```<div class="card">```) se muestra solo si la variable mostrarResumen es true.

Esta lógica garantiza que el resumen solo sea visible después de que el usuario haya completado y enviado los datos del formulario.

- Botón de "Limpiar": Se añadió un botón que, al ser presionado, ejecuta un método que restablece las propiedades de datos (nombre, correo, edad) a cadenas de texto vacías y vuelve a establecer mostrarResumen en false, ocultando así el resumen y mostrando el formulario nuevamente.

---

## Cómo ejecutar el proyecto
Para ejecutar este proyecto en tu entorno local, sigue estos sencillos pasos:

1. Asegúrate de tener Node.js y npm instalados.

2. Navega a la carpeta principal del proyecto en tu terminal.

3. Ejecuta el siguiente comando para instalar las dependencias:
npm install

4. Una vez finalizada la instalación, inicia el servidor de desarrollo con:
npm run dev

5. Abre la URL proporcionada por la terminal (generalmente http://localhost:5173) en tu navegador para ver la aplicación en funcionamiento.