
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
    <a href="#1-Practicas-de-Estructura-del-proyecto">1. Practicas de Estructura del proyecto (5)</a>
  </summary>

&emsp;&emsp;[1.1 Estructura tu solucion por componentes`#strategic`](#-11-Estructura-tu-solucion-por-componentes)</br>
&emsp;&emsp;[1.2 Coloque tus componentes en capas, mantenga la capa web dentro de sus límites `#strategic`](#-12-Coloca-tus-componentes-en-capas-mantén-la-capa-web-dentro-de-sus-límites)</br>
&emsp;&emsp;[1.3 Envurelve las utilidades comunes como paquetes npm](#-13-Envuelva-las-utilidades-comunes-como-paquetes-npm)</br>
&emsp;&emsp;[1.4 Separar la 'aplicación' y el 'servidor' de Express](#-14-Separar-la-aplicación-y-el-servidor-de-Express)</br>
&emsp;&emsp;[1.5 Usar configuración jerárquica, segura y en un entorno consciente `#modified-recently`](#-15-Usar-configuración-jerárquica-segura-y-en-un-entorno-consciente)</br>

</details>

<details>
  <summary>
    <a href="#2-error-handling-practices">2. Prácticas de manejo de errores (12)</a>
  </summary>

&emsp;&emsp;[2.1 Usar Async-Await o promesas para el manejo de errores asíncronos ](#-21-Usar-Async-Await-o-promesas-para-el-manejo-de-errores-asíncronos)</br>
&emsp;&emsp;[2.2 Usar solo el objeto de error incorporado `#strategic`](#-22-Usar-solo-el-objeto-de-error-incorporado)</br>
&emsp;&emsp;[2.3 Distinguir entre errores operativos y de programador `#strategic`](#-23-Distinguir-entre-errores-operativos-y-de-programador)</br>
&emsp;&emsp;[2.4 Manejar errores de forma centralizada, no dentro de un middleware `#strategic`](#-24-Manejar-errores-de-forma-centralizada-no-dentro-de-un-middleware)</br>
&emsp;&emsp;[2.5 Documentar errores de API usando Swagger o GraphQL `#modified-recently`](#-25-Documentar-errores-de-API-usando-Swagger-o-GraphQL)</br>
&emsp;&emsp;[2.6 Salir del proceso con gracia cuando un extraño llega a la ciudad `#strategic`](#-26-Salir-del-proceso-con-gracia-cuando-un-extraño-llega-a-la-ciudad)</br>
&emsp;&emsp;[2.7 Usar un registrador maduro para aumentar la visibilidad de errores ](#-27-Usar-un-registrador-maduro-para-aumentar-la-visibilidad-de-errores)</br>
&emsp;&emsp;[2.8 Pruebe los flujos de error usando su marco de prueba favorito ](#-28-Pruebe-los-flujos-de-error-usando-su-marco-de-prueba-favorito)</br>
&emsp;&emsp;[2.9 Descubrir errores y tiempo de inactividad con productos de APM](#-29-Descubrir-errores-y-tiempo-de-inactividad-con-productos-de-APM)</br>
&emsp;&emsp;[2.10 Detectar rechazos de promesas no gestionados `#modified-recently`](#-210-Detectar-rechazos-de-promesas-no-gestionados)</br>
&emsp;&emsp;[2.11 Fallo-rapido, validar argumentos usando una biblioteca dedicada](#-211-Fallo-rapido-validar-argumentos-usando-una-biblioteca-dedicada)</br>
&emsp;&emsp;[2.12 Siempre espere las promesas antes de regresar para evitar un seguimiento de pila parcial `#new`](#-212-Siempre-espere-las-promesas-antes-de-regresar-para-evitar-un-seguimiento-de-pila-parcial)</br>

</details>


<br/><br/>
<br/><br/>
<br/><br/>



<br/><br/>
# `1. Practicas de Estructura del Projecto`

## ![✔] 1.1 Estructura tu solucion por componentes

**TL;DR:** El peor escollo de las aplicaciones grandes es mantener una enorme base de código con cientos de dependencias: un monolito de este tipo ralentiza a los desarrolladores cuando intentan incorporar nuevas funciones. En su lugar, divida su código en componentes, cada uno tiene su carpeta o una base de código dedicada, y asegúrese de que cada unidad se mantenga pequeña y simple. Visite 'Leer más' a continuación para ver ejemplos de la estructura correcta del proyecto

**De lo contrario:** WCuando los desarrolladores que codifican nuevas funciones luchan por darse cuenta del impacto de su cambio y temen romper otros componentes dependientes, las implementaciones se vuelven más lentas y riesgosas. También se considera más difícil escalar horizontalmente cuando todas las unidades de negocio no están separadas.
🔗 [**Leer Más: estructura por componentes**](./sections/projectstructre/breakintcomponents.md)

<br/><br/>

## ![✔] 1.2 Coloca tus componentes en capas, mantén la capa web dentro de sus límites

**TL;DR:** Cada componente debe contener "capas", un objeto dedicado para la web, la lógica y el código de acceso a datos. Esto no solo genera una clara separación de preocupaciones, sino que también facilita significativamente la simulacion y la prueba del sistema. Aunque este es un patrón muy común, los desarrolladores de API tienden a mezclar capas al pasar los objetos de la capa web (por ejemplo, Express req, res) a la lógica comercial y las capas de datos; esto hace que su aplicación dependa y sea accesible solo por marcos web específicos.

**De lo contrario:** No se puede acceder a la aplicación que combina objetos web con otras capas mediante código de prueba, trabajos CRON, disparadores de colas de mensajes, etc.

🔗 [**Leer Más: Estructura en capas tu applicacion**](./sections/projectstructre/createlayers.md)

<br/><br/>

## ![✔] 1.3 Envuelva las utilidades comunes como paquetes npm

**TL;DR:** En una aplicación grande que constituye una gran base de código, las utilidades transversales, como un registrador, cifrado y similares, deben incluirse en su código y exponerse como paquetes npm privados. Esto permite compartirlos entre múltiples bases de código y proyectos.

**De lo contrario:** Tendrás que inventar tu implementación y la rueda de dependencia

🔗 [**Leer Más: Estructura por funcionalidad**](./sections/projectstructre/wraputilities.md)

<br/><br/>

## ![✔] 1.4 Separar la 'aplicación' y el 'servidor' de Express

**TL;DR:** Evite el desagradable hábito de definir toda la aplicación [Express](https://expressjs.com/) en un solo archivo enorme: separe su definición 'Express' en al menos dos archivos: la API declaración (app.js) y las preocupaciones de red (WWW). Para una estructura aún mejor, ubique su declaración de API dentro de los componentes

**De lo contrario:** Se podrá acceder a su API para realizar pruebas solo a través de llamadas HTTP (es más lento y mucho más difícil generar informes de cobertura). Probablemente no sea un gran placer mantener cientos de líneas de código en un solo archivo.

🔗 [**Leer Más: separar la 'aplicación' y el 'servidor' de Express**](./sections/projectstructre/separateexpress.md)

<br/><br/>

## ![✔] 1.5 Usar configuración jerárquica, segura y en un entorno consciente

**TL;DR:** Una configuración perfecta e impecable debe garantizar que (a) las claves se puedan leer desde el archivo Y desde la variable de entorno (b) los secretos se mantengan fuera del código confirmado (c) la configuración sea jerárquica para facilitar la búsqueda. Hay algunos paquetes que pueden ayudar a marcar la mayoría de esas casillas como [rc](https://www.npmjs.com/package/rc), [nconf](https://www.npmjs.com/package/nconf ), [config](https://www.npmjs.com/package/config) y [convict](https://www.npmjs.com/package/convict).

**De lo contrario:** Si no se cumple alguno de los requisitos de configuración, simplemente se atascará el equipo de desarrollo o DevOps. probablemente ambos

🔗 [**Leer Más: configuration best practices**](./sections/projectstructre/configguide.md)

<br/><br/><br/>
<p align="right"><a href="#table-of-contents">⬆ Regresar hacia arriba</a>
</p>

<br/><br/>

# `2. Prácticas de manejo de errores`

## ![✔] 2.1 Usar Async-Await o promesas para el manejo de errores asíncronos 

**TL;DR:** Manejar errores asincrónicos en el estilo de devolución de llamada es probablemente el camino más rápido al infierno (también conocido como la pirámide de la perdición). El mejor regalo que le puede dar a su código es usar una biblioteca de promesa de buena reputación o async-await en su lugar, lo que permite una sintaxis de código mucho más compacta y familiar como try-catch

**De lo contrario:** El estilo de devolución de llamada de Node.js, función (err, respuesta), es una forma prometedora de código que no se puede mantener debido a la combinación de manejo de errores con código casual, anidamiento excesivo y patrones de codificación incómodos

🔗 [**Leer Más: evitar callbacks**](./sections/errorhandling/asyncerrorhandling.md)

<br/><br/>

## ![✔] 2.2 Usar solo el objeto de error incorporado

**TL;DR:** Muchos arrojan errores como una cadena o como algún tipo personalizado; esto complica la lógica de manejo de errores y la interoperabilidad entre módulos. Ya sea que rechace una promesa, genere una excepción o emita un error, usar solo el objeto Error integrado (o un objeto que amplíe el objeto Error integrado) aumentará la uniformidad y evitará la pérdida de información. Hay una regla ESLint `no-throw-literal` que verifica estrictamente eso (aunque tiene algunas [limitaciones] (https://eslint.org/docs/rules/no-throw-literal) que se pueden resolver usando TypeScript y configurando la regla `@typescript-eslint/no-throw-literal`)

**De lo contrario:** Al invocar algún componente, no estar seguro de qué tipo de errores se obtienen, hace que el manejo adecuado de errores sea mucho más difícil. Peor aún, el uso de tipos personalizados para describir errores podría provocar la pérdida de información crítica sobre errores, como el seguimiento de la pila.

🔗 [**Leer Más: usando el objeto de error integrado**](./sections/errorhandling/useonlythebuiltinerror.md)

<br/><br/>

## ![✔] 2.3 Distinguir entre errores operativos y de programador

**TL;DR:** Los errores operativos (p. ej., la API recibió una entrada no válida) se refieren a casos conocidos en los que el impacto del error se comprende completamente y se puede manejar con cuidado. Por otro lado, el error del programador (por ejemplo, intentar leer una variable indefinida) se refiere a fallas de código desconocidas que dictan que se reinicie correctamente la aplicación.

**De lo contrario:** siempre puede reiniciar la aplicación cuando aparece un error, pero ¿por qué decepcionar a ~5000 usuarios en línea debido a un error operativo menor previsto? Lo contrario tampoco es lo ideal: mantener la aplicación activa cuando se produjo un problema desconocido (error del programador) podría provocar un comportamiento imprevisto. Diferenciar los dos permite actuar con tacto y aplicar un enfoque equilibrado basado en el contexto dado.

🔗 [**Leer Más: error operativo vs programador**](./sections/errorhandling/operationalvsprogrammererror.md)

<br/><br/>

## ![✔] 2.4 Manejar errores de forma centralizada, no dentro de un middleware

**TL;DR:** La lógica de manejo de errores, como el correo al administrador y el registro, debe encapsularse en un objeto dedicado y centralizado al que todos los puntos finales (por ejemplo, Express middleware, trabajos cron, pruebas unitarias) llamen cuando se produzca un error.

**De lo contrario:** No manejar errores dentro de un solo lugar conducirá a la duplicación de código y probablemente a errores manejados incorrectamente

🔗 [**Leer Más: manejo de errores en un lugar centralizado**](./sections/errorhandling/centralizedhandling.md)

<br/><br/>

## ![✔] 2.5 Documentar errores de API usando Swagger o GraphQL

**TL;DR:** Infórmeles a las personas que llaman a la API qué errores pueden surgir a cambio para que puedan manejarlos cuidadosamente sin fallar. Para las API RESTful, esto generalmente se hace con marcos de documentación como Swagger. Si está utilizando GraphQL, también puede utilizar su esquema y sus comentarios.

**De lo contrario:** un cliente API podría decidir fallar y reiniciar solo porque recibió un error que no pudo entender. Nota: la persona que llama a su API podría ser usted (muy típico en un entorno de microservicio)

🔗 [**Leer Más: documentando errores de API en Swagger o GraphQL**](./sections/errorhandling/documentingusingswagger.md)

<br/><br/>

## ![✔] 2.6 Salir del proceso con gracia cuando un extraño llega a la ciudad

**TL;DR:** Cuando ocurre un error desconocido (un error del desarrollador, consulte la práctica recomendada 2.3), existe incertidumbre sobre el estado de la aplicación. La práctica común sugiere reiniciar el proceso con cuidado utilizando una herramienta de gestión de procesos como [Forever](https://www.npmjs.com/package/forever) o [PM2](http://pm2.keymetrics.io/)

**De lo contrario:** cuando ocurre una excepción desconocida, algún objeto puede estar en un estado defectuoso (por ejemplo, un emisor de eventos que se usa globalmente y ya no activa eventos debido a alguna falla interna) y todas las solicitudes futuras pueden fallar o comportarse de manera descabellada.

🔗 [**Leer Más: cerrando el proceso**](./sections/errorhandling/shuttingtheprocess.md)

<br/><br/>

## ![✔] 2.7 Usar un registrador maduro para aumentar la visibilidad de errores

**TL;DR:** Un conjunto de herramientas de registro maduras como [Pino](https://github.com/pinojs/pino) o [Log4js](https://www.npmjs.com/package/log4js) , acelerará el descubrimiento y la comprensión de errores. Así que olvídate de console.log

**De lo contrario:** hojear console.logs o manualmente a través de un archivo de texto desordenado sin herramientas de consulta o un visor de registro decente puede mantenerlo ocupado en el trabajo hasta tarde

🔗 [**Leer Más: usando un registrador maduro**](./sections/errorhandling/usematurelogger.md)

<br/><br/>

## ![✔] 2.8 Pruebe los flujos de error usando su marco de prueba favorito

**TL;DR:** Ya sea control de calidad automatizado profesional o pruebas de desarrollador manuales simples: asegúrese de que su código no solo satisfaga los escenarios positivos, sino que también maneje y devuelva los errores correctos. Los marcos de prueba como Mocha & Chai pueden manejar esto fácilmente (ver ejemplos de código dentro de la "ventana emergente Gist")

**De lo contrario:** Sin pruebas, ya sea de forma automática o manual, no puede confiar en que su código devuelva los errores correctos. Sin errores significativos: no hay manejo de errores

🔗 [**Leer Más: pruebas de flujos de error**](./sections/errorhandling/testingerrorflows.md)

<br/><br/>

## ![✔] 2.9 Descubrir errores y tiempo de inactividad con productos de APM

**TL;DR:** Los productos de supervisión y rendimiento (también conocidos como APM) miden de forma proactiva su base de código o API para que puedan resaltar automáticamente errores, bloqueos y partes lentas que le faltaban

**De lo contrario:** Es posible que dedique un gran esfuerzo a medir el rendimiento de la API y los tiempos de inactividad, probablemente nunca se dará cuenta de cuáles son sus partes de código más lentas en el escenario del mundo real y cómo afectan a la experiencia de usuario.

🔗 [**Leer Más: Usando APM productos**](./sections/errorhandling/apmproducts.md)

<br/><br/>

## ![✔] 2.10 Detectar rechazos de promesas no gestionados

**TL;DR:** Cualquier excepción lanzada dentro de una promesa será tragada y descartada a menos que un desarrollador no se olvide de manejarla explícitamente. ¡Incluso si su código está suscrito a`process.uncaughtException`! Supere esto registrándose en el evento `process.unhandledRejection`

**De lo contrario:** Sus errores serán absorbidos y no dejarán rastro. Nada de que preocuparse

🔗 [**Leer Más: detección de rechazos de promesas no controlados**](./sections/errorhandling/catchunhandledpromiserejection.md)

<br/><br/>

## ![✔] 2.11 Fallo-rapido, validar argumentos usando una biblioteca dedicada

**TL;DR:** Afirme la entrada de API para evitar errores desagradables que son mucho más difíciles de rastrear más adelante. El código de validación suele ser tedioso a menos que esté utilizando una biblioteca auxiliar muy interesante como [ajv](https://www.npmjs.com/package/ajv) y [Joi](https://www.npmjs.com/package /yo)

**De lo contrario:** Considere esto: su función espera un argumento numérico "Descuento" que la persona que llama se olvida de pasar, más tarde, su código verifica si ¡Descuento! = 0 (la cantidad de descuento permitido es mayor que cero), entonces lo hará permitir al usuario disfrutar de un descuento. Dios mío, qué bicho más desagradable. ¿Puedes verlo?

🔗 [**Leer Más: Falling fast**](./sections/errorhandling/failfast.md)

<br/><br/>

## ![✔] 2.12 Siempre espere las promesas antes de regresar para evitar un seguimiento de pila parcial `#new`

**TL;DR:** Siempre haga `return await` cuando devuelva una promesa para beneficiarse del seguimiento completo del error. si un la función devuelve una promesa, esa función debe declararse como función `async` y explícitamente
`await` (esperar) la promesa antes de devolverla

**De lo contrario:** La función que devuelve una promesa sin esperar no aparecerá en el seguimiento de la pila.
Tales marcos faltantes probablemente complicarían la comprensión del flujo que conduce al error,
especialmente si la causa del comportamiento anormal está dentro de la función que falta

🔗 [**Leer Más: retorno de promesas**](./sections/errorhandling/returningpromises.md)

<br/><br/><br/>

<p align="right"><a href="#table-of-contents">⬆ Return to top</a></p>
