---
title: Inicio rápido de la biblioteca cliente para JavaScript de Bing Web Search
titleSuffix: Azure Cognitive Services
services: cognitive-services
author: aahill
manager: nitinme
ms.service: cognitive-services
ms.topic: include
ms.date: 03/05/2020
ms.author: aahi
ms.custom: devx-track-js
ms.openlocfilehash: 20eaf6e6a9f0eee15e6ad6a5bd8f23bf8531545c
ms.sourcegitcommit: 5dbea4631b46d9dde345f14a9b601d980df84897
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/25/2020
ms.locfileid: "91376377"
---
La biblioteca cliente de Bing Web Search facilita la integración de Bing Web Search en la aplicación de Node.js. En esta guía de inicio rápido, aprenderá a crear una instancia de un cliente, enviar una solicitud e imprimir la respuesta.

¿Desea ver el código ahora mismo? En GitHub se encuentran disponibles ejemplos de [bibliotecas cliente de Bing Search para JavaScript](https://github.com/Azure-Samples/cognitive-services-node-sdk-samples/tree/master/Samples).

## <a name="prerequisites"></a>Prerequisites
Estas son algunas cosas que necesitará antes de ejecutar esta guía de inicio rápido:

* [Node.js 6](https://nodejs.org/en/download/) o posterior
* Una clave de suscripción  

[!INCLUDE [bing-web-search-quickstart-signup](~/includes/bing-web-search-quickstart-signup.md)]


## <a name="set-up-your-development-environment"></a>Configurado su entorno de desarrollo

Empecemos por la configuración del entorno de desarrollo para nuestro proyecto de Node.js.

1. Cree un directorio para su proyecto:

    ```console
    mkdir YOUR_PROJECT
    ```

1. Cree un archivo de paquete:

    ```console
    cd YOUR_PROJECT
    npm init
    ```

1. Ahora, vamos a instalar algunos módulos de Azure y agregarlos a `package.json`:

    ```console
    npm install --save @azure/cognitiveservices-websearch
    npm install --save @azure/ms-rest-azure-js
    ```

## <a name="create-a-project-and-declare-required-modules"></a>Creación de un proyecto y declaración de los módulos necesarios

En el mismo directorio que su `package.json`, cree un nuevo proyecto de Node.js con su editor o IDE favorito. Por ejemplo: `sample.js`.

A continuación, copie este código en el proyecto. Se cargan los módulos instalados en la sección anterior.

```javascript
const CognitiveServicesCredentials = require('@azure/ms-rest-azure-js').CognitiveServicesCredentials;
const WebSearchAPIClient = require('@azure/cognitiveservices-websearch');
```

## <a name="instantiate-the-client"></a>Creación de una instancia del cliente

Este código crea una instancia de un cliente mediante el módulo `@azure/cognitiveservices-websearch`. Asegúrese de escribir una clave de suscripción válida para la cuenta de Azure antes de continuar.

```javascript
let credentials = new CognitiveServicesCredentials('YOUR-ACCESS-KEY');
let webSearchApiClient = new WebSearchAPIClient(credentials);
```

## <a name="make-a-request-and-print-the-results"></a>Presentación de solicitud e impresión de resultados

Utilice el cliente para enviar una consulta de búsqueda a Bing Web Search. Si la respuesta incluye resultados para cualquiera de los elementos de la matriz `properties`, se imprime `result.value` en la consola.

```javascript
webSearchApiClient.web.search('seahawks').then((result) => {
    let properties = ["images", "webPages", "news", "videos"];
    for (let i = 0; i < properties.length; i++) {
        if (result[properties[i]]) {
            console.log(result[properties[i]].value);
        } else {
            console.log(`No ${properties[i]} data`);
        }
    }
}).catch((err) => {
    throw err;
})
```

## <a name="run-the-program"></a>Ejecución del programa

¡El último paso es ejecutar el programa!

## <a name="clean-up-resources"></a>Limpieza de recursos

Cuando haya terminado con este proyecto, asegúrese de quitar la clave de suscripción desde el código del programa.

## <a name="next-steps"></a>Pasos siguientes

> [!div class="nextstepaction"]
> [Ejemplos del SDK de Cognitive Services para Node.js](https://github.com/Azure-Samples/cognitive-services-node-sdk-samples)

## <a name="see-also"></a>Consulte también

* [Referencia del SDK de Nodo de Azure](https://docs.microsoft.com/javascript/api/@azure/cognitiveservices-websearch/)
