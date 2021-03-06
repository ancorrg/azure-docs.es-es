---
title: ¿Qué es Form Recognizer?
titleSuffix: Azure Cognitive Services
description: El servicio Azure Form Recognizer le permite identificar y extraer pares clave-valor y datos de tabla de los documentos de formulario, así como información importante de los recibos de ventas y las tarjetas de presentación.
author: PatrickFarley
manager: nitinme
ms.service: cognitive-services
ms.subservice: forms-recognizer
ms.topic: overview
ms.date: 09/21/2020
ms.author: pafarley
ms.custom: cog-serv-seo-aug-2020
keywords: automated data processing, document processing, automated data entry, forms processing
ms.openlocfilehash: 5243c170e1f6b5f647057b8cfafbcac9b2fb4db3
ms.sourcegitcommit: eb6bef1274b9e6390c7a77ff69bf6a3b94e827fc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/05/2020
ms.locfileid: "91318966"
---
# <a name="what-is-form-recognizer"></a>¿Qué es Form Recognizer?

[!INCLUDE [TLS 1.2 enforcement](../../../includes/cognitive-services-tls-announcement.md)]

Azure Form Recognizer es un servicio cognitivo que le permite crear software de procesamiento de datos automatizado mediante tecnología de aprendizaje automático. Identifique y extraiga texto, pares clave-valor y datos de tabla de los documentos de formulario; el servicio genera datos estructurados que incluyen las relaciones en el archivo original. Obtendrá rápidamente resultados precisos a la medida de su contenido específico sin necesidad de una intervención manual pesada o una amplia experiencia en ciencia de datos. Use Form Recognizer para automatizar la entrada de datos en las aplicaciones.

Form Recognizer consta de modelos de procesamiento de documentos personalizados, los modelos precompilados de recibos y tarjetas de presentación y la API de diseño. Puede llamar a los modelos de Form Recognizer mediante una API REST o los SDK de la biblioteca cliente, e integrarlos en su flujo de trabajo o aplicación.

Form Recognizer se compone de los siguientes servicios:
* **[Modelos personalizados](#custom-models)** : extraiga pares clave-valor y datos de tabla de los formularios. Puede entrenar estos modelos con sus propios datos para que se adapten a sus formularios.
* **[Modelos precompilados](#prebuilt-models)** : extraiga datos de tipos de formularios únicos mediante modelos precompilados. Actualmente, hay modelos pregenerados para las confirmaciones de ventas y las tarjetas de presentación en inglés.
* **[API de diseño](#layout-api)** : extraiga estructuras de texto y tabla, junto con sus coordenadas de rectángulos de selección, de los documentos.

## <a name="custom-models"></a>Modelos personalizados

Puede entrenar los modelos personalizados de Form Recognizer con sus propios datos y solo necesita cinco formularios de entrada de ejemplo para empezar. Un modelo de procesamiento de documentos entrenado puede generar datos estructurados que incluyen las relaciones en el documento de formulario original. Después de entrenar el modelo, puede probarlo, volver a entrenarlo y finalmente usarlo para extraer datos de forma confiable de más formularios en función de las propias necesidades.

Tiene las siguientes opciones al entrenar modelos personalizados: entrenamiento con datos etiquetados y sin ellos.

### <a name="train-without-labels"></a>Entrenamiento sin etiquetas

De forma predeterminada, Form Recognizer usa el aprendizaje sin supervisión para comprender el diseño y las relaciones entre los campos y las entradas de los formularios. Cuando se envían los formularios de entrada, el algoritmo agrupa los formularios por tipos, descubre qué claves y tablas están presentes y asocia los valores a las claves y entradas a las tablas. Esto no requiere el etiquetado de datos manual ni una codificación intensiva, ni mantenimiento y se recomienda probar este método primero.

Consulte [Creación de un conjunto de datos de entrenamiento](./build-training-data-set.md) para ver sugerencias sobre cómo recopilar los documentos de entrenamiento.

### <a name="train-with-labels"></a>Entrenamiento con etiquetas

Al entrenar con datos etiquetados, el modelo realiza un aprendizaje supervisado para extraer valores de interés mediante los formularios etiquetados que se proporcionan. Esto da como resultado modelos con un mejor rendimiento y puede generar modelos que funcionen con formularios complejos o formularios que contengan valores sin claves.

Form Recognizer usa la [API de diseño](#layout-api) para aprender los tamaños y posiciones esperados de los elementos de texto impresos y manuscritos. A continuación, usa etiquetas especificadas por el usuario para aprender las asociaciones clave-valor de los documentos. Se recomienda usar cinco formularios etiquetados manualmente del mismo tipo para empezar a entrenar un nuevo modelo y agregar más datos etiquetados según sea necesario para mejorar la precisión del modelo.

## <a name="prebuilt-models"></a>Modelos creados previamente

Form Recognizer también incluye modelos precompilados para el procesamiento automático de datos de tipos de formularios únicos.

### <a name="prebuilt-receipt-model"></a>Modelo de recibo pregenerado

El modelo de recibo pregenerado se usa para leer los recibos de ventas en Inglés de Australia, Canadá, Gran Bretaña, India y Estados Unidos (el tipo que usan los restaurantes, las estaciones de gas, minoristas, etc). Este modelo extrae información clave como la hora y la fecha de la transacción, información del comerciante, importe de los impuestos, totales y mucho más. Además, el modelo de recibo pregenerado se entrena para reconocer y devolver todo el texto en un recibo. Consulte la guía conceptual sobre [recibos](./concept-receipts.md) para más información.

![recibo de ejemplo](./media/contoso-receipt-small.png)

### <a name="prebuilt-business-cards-model"></a>Modelo de tarjetas de presentación pregenerado

El modelo de tarjetas de presentación le permite extraer información como el nombre de la persona, el puesto de trabajo, la dirección, el correo electrónico, la empresa y los números de teléfono de las tarjetas de presentación en inglés. Consulte la guía conceptual sobre [tarjetas de presentación](./concept-business-cards.md) para más información.

![tarjeta de presentación de ejemplo](./media/business-card-english.jpg)

## <a name="layout-api"></a>API de diseño

Form Recognizer también puede extraer texto y estructuras de tablas (los números de fila y columna asociados al texto) mediante el reconocimiento óptico de caracteres (OCR) de alta definición.

## <a name="get-started"></a>Introducción

Siga un inicio rápido para comenzar a extraer datos de los formularios. Se recomienda usar el servicio gratuito cuando se está aprendiendo la tecnología. Recuerde que el número de páginas gratuitas se limita a 500 al mes.

* [Inicios rápidos de la biblioteca cliente](./quickstarts/client-library.md) (todos los lenguajes, varios escenarios)
* Inicios rápidos de la interfaz de usuario web
  * [Entrenamiento con etiquetas: herramienta de etiquetado de ejemplo](quickstarts/label-tool.md)
* Inicios rápidos de REST
  * Entrenamiento de modelos personalizados y extracción de datos de formularios
    * [Entrenamiento sin etiquetas: cURL](quickstarts/curl-train-extract.md)
    * [Entrenamiento sin etiquetas: Python](quickstarts/python-train-extract.md)
    * [ Entrenamiento con etiquetas: Python](quickstarts/python-labeled-data.md)
  * Extracción de datos de recibos de ventas
    * [Extracción de datos de recibos: cURL](quickstarts/curl-receipts.md)
    * [Extracción de datos de recibos: Python](quickstarts/python-receipts.md)
  * Extracción de datos de tarjetas de presentación
    * [Extracción de datos de tarjetas de presentación: Python](quickstarts/python-business-cards.md)
  * Extracción de texto y estructura de tablas de formularios
    * [Extracción de datos de diseño: Python](quickstarts/python-layout.md)


### <a name="review-the-rest-apis"></a>Revisión de las API REST

Va a utilizar las siguientes API para entrenar modelos y extraer datos estructurados de formularios.

|Nombre |Descripción |
|---|---|
| **Entrenamiento de modelos personalizados**| Entrene un nuevo modelo para analizar los formularios con cinco formularios del mismo tipo. Establezca el parámetro _useLabelFile_ en `true` para entrenar con datos etiquetados manualmente. |
| **Análisis de formularios** |Analice un documento único pasado como una secuencia para extraer texto, pares clave-valor y tablas del formulario con su modelo personalizado.  |
| **Análisis de recibos** |Analice un documento de entrada individual para extraer la información clave y cualquier otro texto del recibo.|
| **Análisis de una tarjeta de presentación** |Analice una tarjeta de presentación para extraer el texto y la información más importante.|
| **Análisis de diseño** |Analice el diseño de un formulario para extraer texto y estructuras de tablas.|

Explore la [documentación de referencia de API REST](https://westus2.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-v2/operations/AnalyzeWithCustomForm) para más información. Si está familiarizado con una versión anterior de la API, consulte el artículo sobre [novedades](./whats-new.md) para más información sobre los cambios recientes.

## <a name="input-requirements"></a>Requisitos de entrada

[!INCLUDE [input requirements](./includes/input-requirements.md)]

## <a name="data-privacy-and-security"></a>Seguridad y privacidad de datos

Al igual que sucede con todas las instancias de Cognitive Services, los desarrolladores que usan el servicio Form Recognizer deben estar al tanto de las directivas de Microsoft sobre los datos de los clientes. Para más información, consulte la [página de Cognitive Services](https://www.microsoft.com/trustcenter/cloudservices/cognitiveservices) en Microsoft Trust Center.

## <a name="next-steps"></a>Pasos siguientes

Realice un [inicio rápido de biblioteca cliente](quickstarts/client-library.md) para empezar a escribir una aplicación de procesamiento de formularios con Form Recognizer en el lenguaje de su elección.