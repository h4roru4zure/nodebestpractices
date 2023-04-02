[✔]: assets/images/checkbox-small-blue.png

# Node.js Mejores Practicas

<h1 align="center">
  <img src="assets/images/banner-2.jpg" alt="Node.js Mejores Practicas"/>
</h1>

<br/>

<div align="center">
  <img src="https://img.shields.io/badge/⚙%20Item%20count%20-%20102%20Best%20Practices-blue.svg" alt="102 items"/> <img id="last-update-badge" src="https://img.shields.io/badge/%F0%9F%93%85%20Last%20update%20-%20March%2021%2C%202023-green.svg" alt="Last update: March 21, 2023" /> <img src="https://img.shields.io/badge/ %E2%9C%94%20Updated%20For%20Version%20-%20Node%2014.0.0-brightgreen.svg" alt="Updated for Node 14.0.0"/>
</div>

<br/>

[<img src="assets/images/twitter.svg" width="16" height="16" alt="" />](https://twitter.com/nodepractices/) **Follow us on Twitter!** [**@nodepractices**](https://twitter.com/nodepractices/)

<br/>

Leer en un idioma diferente: [![CN](./assets/flags/CN.png)**CN**](./README.chinese.md), [![FR](./assets/flags/FR.png)**FR**](./README.french.md), [![BR](./assets/flags/BR.png)**BR**](./README.brazilian-portuguese.md), [![RU](./assets/flags/RU.png)**RU**](./README.russian.md), [![PL](./assets/flags/PL.png)**PL**](./README.polish.md), [![JA](./assets/flags/JA.png)**JA**](./README.japanese.md), [![EU](./assets/flags/EU.png)**EU**](./README.basque.md) [(![ES](./assets/flags/ES.png)**ES**, ![HE](./assets/flags/HE.png)**HE**, ![KR](./assets/flags/KR.png)**KR** and ![TR](./assets/flags/TR.png)**TR** in progress! )](#translations)

<br/>

## 🚀 Tenemos una version [official Node.js starter - Practica.js](https://github.com/practicajs/practica). Úsalo para generar una nueva estructura de solución con todas las prácticas hechas en su interior. O simplemente para aprender por ejemplos de código

<br/>

# Últimas mejores prácticas y noticias

- **✨ 80,000 stars**: Sonrojado, sorprendido y orgulloso!

- **🔖 Nuevo menú y etiquetas**: Nuestro menú ahora es plegable e incluye `#etiquetas`. Los nuevos visitantes pueden leer primero los artículos `#strategic`. Los visitantes que regresan pueden concentrarse en el contenido `#nuevo`. Las personas mayores pueden filtrar por elementos `#avanzados`. Cortesía del único e inigualable [Rubek Joshi](https://github.com/rubek-joshi)

- **👨‍👩‍👧‍👦 ¡Nuevo miembro de la familia!**: Un nuevo repositorio se une a nuestra familia - [Prácticas recomendadas de las pruebas de integración de Node.js ✨](https://github.com/testjavascript/nodejs-integration-tests -mejores prácticas). Incluye más de 40 prácticas recomendadas para escribir pruebas de componentes de Node.js asombrosas y eficaces

- **![FR](./assets/flags/FR.png) ¡Traducción al francés!1! :** La última traducción que se une a nuestra guía internacional es al francés. bienvenue

<br/><br/>

# ¡Bienvenido! 3 cosas que debes saber primero

**1. Estás leyendo docenas de los mejores artículos de Node.js: ** este repositorio es un resumen y una selección del contenido mejor clasificado sobre las mejores prácticas de Node.js, así como el contenido escrito aquí por colaboradores.

**2. Es la compilación más grande y crece cada semana. ** Actualmente, se presentan más de 80 mejores prácticas, guías de estilo y consejos arquitectónicos. Todos los días se crean nuevas ediciones y solicitudes de incorporación de cambios para mantener actualizado este libro en vivo. Nos encantaría verlo contribuir aquí, ya sea corrigiendo errores de código, ayudando con las traducciones o sugiriendo nuevas ideas brillantes. Consulte nuestras [directrices de escritura aquí] (./.operations/writing-guidelines.md)

**3. Las mejores prácticas tienen información adicional -** la mayoría de las viñetas incluyen un enlace **🔗Leer más** que amplía la práctica con ejemplos de código, citas de blogs seleccionados y más información

<br/><br/>


## Table of Contents

<details>
  <summary>
    <a href="#1-project-structure-practices">1. Practicas de Estructura del proyecto (5)</a>
  </summary>

&emsp;&emsp;[1.1 Estructura tu solucion por componentes`#strategic`](#-11-structure-your-solution-by-components)</br>
&emsp;&emsp;[1.2 Coloque los componentes en capas, mantenga la capa web dentro de sus límites `#strategic`](#-12-layer-your-components-keep-the-web-layer-within-its-boundaries)</br>
&emsp;&emsp;[1.3 Envurelve las utilidades comunes como paquetes npm](#-13-wrap-common-utilities-as-npm-packages)</br>
&emsp;&emsp;[1.4 Separar la 'aplicación' y el 'servidor' de Express](#-14-separate-express-app-and-server)</br>
&emsp;&emsp;[1.5 Usar configuración jerárquica, segura y en un entorno consciente `#modified-recently`](#-15-use-environment-aware-secure-and-hierarchical-config)</br>

</details>

<details>
  <summary>
    <a href="#2-error-handling-practices">2. rácticas de manejo de errores (12)</a>
  </summary>

&emsp;&emsp;[2.1 Usar Async-Await o promesas para el manejo de errores asíncronos ](#-21-use-async-await-or-promises-for-async-error-handling)</br>
&emsp;&emsp;[2.2 sar solo el objeto de error incorporado `#strategic`](#-22-use-only-the-built-in-error-object)</br>
&emsp;&emsp;[2.3 Distinguir entre errores operativos y de programador `#strategic`](#-23-distinguish-operational-vs-programmer-errors)</br>
&emsp;&emsp;[2.4 Manejar errores de forma centralizada, no dentro de un middleware `#strategic`](#-24-handle-errors-centrally-not-within-a-middleware)</br>
&emsp;&emsp;[2.5 Documentar errores de API usando Swagger o GraphQL `#modified-recently`](#-25-document-api-errors-using-swagger-or-graphql)</br>
&emsp;&emsp;[2.6 Salir del proceso con gracia cuando un extraño llega a la ciudad `#strategic`](#-26-exit-the-process-gracefully-when-a-stranger-comes-to-town)</br>
&emsp;&emsp;[2.7 Usar un registrador maduro para aumentar la visibilidad de errores ](#-27-use-a-mature-logger-to-increase-error-visibility)</br>
&emsp;&emsp;[2.8 Pruebe los flujos de error usando su marco de prueba favorito ](#-28-test-error-flows-using-your-favorite-test-framework)</br>
&emsp;&emsp;[2.9 Descubrir errores y tiempo de inactividad con productos de APM](#-29-discover-errors-and-downtime-using-apm-products)</br>
&emsp;&emsp;[2.10 Detectar rechazos de promesas no gestionados `#modified-recently`](#-210-catch-unhandled-promise-rejections)</br>
&emsp;&emsp;[2.11 Fallo-rapido, validar argumentos usando una biblioteca dedicada](#-211-fail-fast-validate-arguments-using-a-dedicated-library)</br>
&emsp;&emsp;[2.12 Siempre espere las promesas antes de regresar para evitar un seguimiento de pila parcial `#new`](#-212-always-await-promises-before-returning-to-avoid-a-partial-stacktrace)</br>

</details>
