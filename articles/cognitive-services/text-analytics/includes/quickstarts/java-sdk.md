---
title: 'Inicio rápido: Biblioteca cliente v3 de Text Analytics para Java | Microsoft Docs'
description: Introducción a la biblioteca cliente v3 de Text Analytics para Java.
author: aahill
manager: nitinme
ms.service: cognitive-services
ms.subservice: text-analytics
ms.topic: include
ms.date: 10/07/2020
ms.custom: devx-track-java
ms.author: aahi
ms.reviewer: tasharm, assafi, sumeh
ms.openlocfilehash: 7adfafbb0b0b11057a21dfbbe6dffcf6d2564606
ms.sourcegitcommit: d103a93e7ef2dde1298f04e307920378a87e982a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/13/2020
ms.locfileid: "91977840"
---
<a name="HOLTop"></a>

# <a name="version-31-preview"></a>[Versión 3.1 (versión preliminar)](#tab/version-3-1)

[Documentación de referencia](https://docs.microsoft.com/java/api/overview/azure/ai-textanalytics-readme?view=azure-java-stable) | [Código fuente de la biblioteca](https://github.com/Azure/azure-sdk-for-java/blob/azure-ai-textanalytics_5.1.0-beta.1/sdk/textanalytics/azure-ai-textanalytics) | [Paquete](https://mvnrepository.com/artifact/com.azure/azure-ai-textanalytics/5.1.0-beta.1) | [Ejemplos](https://github.com/Azure/azure-sdk-for-java/tree/azure-ai-textanalytics_5.1.0-beta.1/sdk/textanalytics/azure-ai-textanalytics/src/samples/java/com/azure/ai/textanalytics)

# <a name="version-30"></a>[Versión 3.0](#tab/version-3)

[Documentación de referencia](https://docs.microsoft.com/java/api/overview/azure/ai-textanalytics-readme?view=azure-java-stable) | [Código fuente de la biblioteca](https://github.com/Azure/azure-sdk-for-java/blob/azure-ai-textanalytics_5.0.0/sdk/textanalytics/azure-ai-textanalytics) | [Paquete](https://mvnrepository.com/artifact/com.azure/azure-ai-textanalytics/5.0.0) | [Ejemplos](https://github.com/Azure/azure-sdk-for-java/tree/azure-ai-textanalytics_5.0.0/sdk/textanalytics/azure-ai-textanalytics/src/samples/java/com/azure/ai/textanalytics)

# <a name="version-21"></a>[Versión 2.1](#tab/version-2)

En este artículo solo se describe la versión 3.x de la API.

---

## <a name="prerequisites"></a>Prerrequisitos

* Una suscripción a Azure: [cree una cuenta gratuita](https://azure.microsoft.com/free/cognitive-services)
* [Kit de desarrollo de Java](https://www.oracle.com/technetwork/java/javase/downloads/index.html) (JDK), versión 8 o posterior
* Una vez que tenga la suscripción de Azure, <a href="https://ms.portal.azure.com/#create/Microsoft.CognitiveServicesTextAnalytics"  title="cree un recurso de Text Analytics"  target="_blank">cree un recurso de Text Analytics <span class="docon docon-navigate-external x-hidden-focus"></span></a> en Azure Portal para obtener la clave y el punto de conexión.  Una vez que se implemente, haga clic en **Ir al recurso**.
    * Necesitará la clave y el punto de conexión del recurso que cree para conectar la aplicación a API Text Analytics. En una sección posterior de este mismo inicio rápido pegará la clave y el punto de conexión en el código siguiente.
    * Puede usar el plan de tarifa gratis (`F0`) para probar el servicio y actualizarlo más adelante a un plan de pago para producción.

## <a name="setting-up"></a>Instalación

### <a name="add-the-client-library"></a>Incorporación de la biblioteca cliente

# <a name="version-31-preview"></a>[Versión 3.1 (versión preliminar)](#tab/version-3-1)

Cree un proyecto de Maven en el entorno de desarrollo o IDE que prefiera. Luego, agregue la siguiente dependencia al archivo *pom.xml* del proyecto. La sintaxis de implementación [de otras herramientas de compilación](https://mvnrepository.com/artifact/com.azure/azure-ai-textanalytics/5.1.0-beta.1) se puede encontrar en línea.

```xml
<dependencies>
     <dependency>
        <groupId>com.azure</groupId>
        <artifactId>azure-ai-textanalytics</artifactId>
        <version>5.1.0-beta.1</version>
    </dependency>
</dependencies>
```

# <a name="version-30"></a>[Versión 3.0](#tab/version-3)

Cree un proyecto de Maven en el entorno de desarrollo o IDE que prefiera. Luego, agregue la siguiente dependencia al archivo *pom.xml* del proyecto. La sintaxis de implementación [de otras herramientas de compilación](https://mvnrepository.com/artifact/com.azure/azure-ai-textanalytics/5.0.0) se puede encontrar en línea.

```xml
<dependencies>
     <dependency>
        <groupId>com.azure</groupId>
        <artifactId>azure-ai-textanalytics</artifactId>
        <version>5.0.0</version>
    </dependency>
</dependencies>
```

> [!TIP]
> ¿Desea ver todo el archivo de código de inicio rápido de una vez? Puede encontrarlo [en GitHub](https://github.com/Azure-Samples/cognitive-services-quickstart-code/blob/master/java/TextAnalytics/TextAnalyticsSamples.java), que contiene los ejemplos de código de este inicio rápido. 

# <a name="version-21"></a>[Versión 2.1](#tab/version-2)

En este artículo solo se describe la versión 3.x de la API.

---

Cree un archivo de Java llamado `TextAnalyticsSamples.java`. Abra el archivo y agregue las siguientes instrucciones `import`:

```java
import com.azure.core.credential.AzureKeyCredential;
import com.azure.ai.textanalytics.models.*;
import com.azure.ai.textanalytics.TextAnalyticsClientBuilder;
import com.azure.ai.textanalytics.TextAnalyticsClient;
```

En el archivo de Java, agregue una nueva clase y agregue el punto de conexión y la clave del recurso de Azure, como se muestra a continuación.

[!INCLUDE [text-analytics-find-resource-information](../find-azure-resource-info.md)]

```java
public class TextAnalyticsSamples {
    private static String KEY = "<replace-with-your-text-analytics-key-here>";
    private static String ENDPOINT = "<replace-with-your-text-analytics-endpoint-here>";
}
```

Agregue el siguiente método principal a la clase. Más adelante definirá los métodos a los que llama aquí.

# <a name="version-31-preview"></a>[Versión 3.1 (versión preliminar)](#tab/version-3-1)

```java
public static void main(String[] args) {
    //You will create these methods later in the quickstart.
    TextAnalyticsClient client = authenticateClient(KEY, ENDPOINT);

    sentimentAnalysisWithOpinionMiningExample(client)
    detectLanguageExample(client);
    recognizeEntitiesExample(client);
    recognizeLinkedEntitiesExample(client);
    recognizePiiEntitiesExample(client);
    extractKeyPhrasesExample(client);
}
```

# <a name="version-30"></a>[Versión 3.0](#tab/version-3)

```java
public static void main(String[] args) {
    //You will create these methods later in the quickstart.
    TextAnalyticsClient client = authenticateClient(KEY, ENDPOINT);

    sentimentAnalysisExample(client);
    detectLanguageExample(client);
    recognizeEntitiesExample(client);
    recognizeLinkedEntitiesExample(client);
    extractKeyPhrasesExample(client);
}
```

# <a name="version-21"></a>[Versión 2.1](#tab/version-2)

En este artículo solo se describe la versión 3.x de la API.

---


## <a name="object-model"></a>Modelo de objetos

El cliente de Text Analytics es un objeto `TextAnalyticsClient` que se autentica en Azure mediante su clave y que proporciona funciones para aceptar texto como cadenas individuales o como un lote. Puede enviar texto a la API de forma sincrónica o asincrónica. El objeto de respuesta contendrá la información del análisis de todos los documentos que envíe. 

## <a name="code-examples"></a>Ejemplos de código

* [Autenticar el cliente](#authenticate-the-client)
* [Análisis de sentimiento](#sentiment-analysis) 
* [Minería de opiniones](#opinion-mining)
* [Detección de idioma](#language-detection)
* [Reconocimiento de entidades con nombre](#named-entity-recognition-ner)
* [Vinculación de entidad](#entity-linking)
* [Extracción de frases clave](#key-phrase-extraction)

## <a name="authenticate-the-client"></a>Autenticar el cliente

Cree un método para crear una instancia del objeto `TextAnalyticsClient` con la clave y el punto de conexión del recurso Text Analytics. Este ejemplo es el mismo para las versiones 3.0 y 3.1 de la API.

```java
static TextAnalyticsClient authenticateClient(String key, String endpoint) {
    return new TextAnalyticsClientBuilder()
        .credential(new AzureKeyCredential(key))
        .endpoint(endpoint)
        .buildClient();
}
```


En el método de `main()` del programa, llame al método de autenticación para crear una instancia del cliente.

## <a name="sentiment-analysis"></a>análisis de opiniones

# <a name="version-31-preview"></a>[Versión 3.1 (versión preliminar)](#tab/version-3-1)

> [!NOTE]
> En la versión `3.1`:
> * Análisis de sentimiento incluye el análisis de minería de opiniones, que es una marca opcional. 
> * La minería de opiniones contiene el aspecto y el sentimiento de nivel de opinión. 

Cree una función denominada `sentimentAnalysisExample()` que tome el cliente que creó anteriormente y llame a su función `analyzeSentiment()`. El objeto `AnalyzeSentimentResult` devuelto contendrá `documentSentiment` y `sentenceSentiments` si la operación se realiza correctamente, o `errorMessage` si no. 

```java
static void sentimentAnalysisExample(TextAnalyticsClient client)
{
    // The text that need be analyzed.
    String text = "I had the best day of my life. I wish you were there with me.";

    DocumentSentiment documentSentiment = client.analyzeSentiment(text);
    System.out.printf(
        "Recognized document sentiment: %s, positive score: %s, neutral score: %s, negative score: %s.%n",
        documentSentiment.getSentiment(),
        documentSentiment.getConfidenceScores().getPositive(),
        documentSentiment.getConfidenceScores().getNeutral(),
        documentSentiment.getConfidenceScores().getNegative());

    for (SentenceSentiment sentenceSentiment : documentSentiment.getSentences()) {
        System.out.printf(
            "Recognized sentence sentiment: %s, positive score: %s, neutral score: %s, negative score: %s.%n",
            sentenceSentiment.getSentiment(),
            sentenceSentiment.getConfidenceScores().getPositive(),
            sentenceSentiment.getConfidenceScores().getNeutral(),
            sentenceSentiment.getConfidenceScores().getNegative());
        }
    }
}
```

### <a name="output"></a>Output

```console
Recognized document sentiment: positive, positive score: 1.0, neutral score: 0.0, negative score: 0.0.
Recognized sentence sentiment: positive, positive score: 1.0, neutral score: 0.0, negative score: 0.0.
Recognized sentence sentiment: neutral, positive score: 0.21, neutral score: 0.77, negative score: 0.02.
```

### <a name="opinion-mining"></a>Minería de opiniones

Para realizar análisis de sentimiento con la minería de opiniones, cree una nueva función llamada `sentimentAnalysisWithOpinionMiningExample()` que tome el cliente que creó anteriormente y llame a su función `analyzeSentiment()` con el objeto de opción de configuración `AnalyzeSentimentOptions`. El objeto `AnalyzeSentimentResult` devuelto contendrá `documentSentiment` y `sentenceSentiments` si la operación se realiza correctamente, o `errorMessage` si no. 


```java
static void sentimentAnalysisWithOpinionMiningExample(TextAnalyticsClient client)
{
    // The Document that needs be analyzed.
    String document = "Bad atmosphere. Not close to plenty of restaurants, hotels, and transit! Staff are not friendly and helpful.";

    System.out.printf("Document = %s%n", document);

    AnalyzeSentimentOptions options = new AnalyzeSentimentOptions().setIncludeOpinionMining(true);
    final DocumentSentiment documentSentiment = client.analyzeSentiment(document, "en", options);
    SentimentConfidenceScores scores = documentSentiment.getConfidenceScores();
    System.out.printf(
            "\tRecognized document sentiment: %s, positive score: %f, neutral score: %f, negative score: %f.%n",
            documentSentiment.getSentiment(), scores.getPositive(), scores.getNeutral(), scores.getNegative());

    documentSentiment.getSentences().forEach(sentenceSentiment -> {
        SentimentConfidenceScores sentenceScores = sentenceSentiment.getConfidenceScores();
        System.out.printf("\t\tSentence sentiment: %s, positive score: %f, neutral score: %f, negative score: %f.%n",
                sentenceSentiment.getSentiment(), sentenceScores.getPositive(), sentenceScores.getNeutral(), sentenceScores.getNegative());
        sentenceSentiment.getMinedOpinions().forEach(minedOpinions -> {
            AspectSentiment aspectSentiment = minedOpinions.getAspect();
            System.out.printf("\t\t\tAspect sentiment: %s, aspect text: %s%n", aspectSentiment.getSentiment(),
                    aspectSentiment.getText());
            for (OpinionSentiment opinionSentiment : minedOpinions.getOpinions()) {
                System.out.printf("\t\t\t\t'%s' opinion sentiment because of \"%s\". Is the opinion negated: %s.%n",
                        opinionSentiment.getSentiment(), opinionSentiment.getText(), opinionSentiment.isNegated());
            }
        });
    });
}
```

### <a name="output"></a>Output

```console
Text = Bad atmosphere. Not close to plenty of restaurants, hotels, and transit! Staff are not friendly and helpful.
    Recognized document sentiment: negative, positive score: 0.010000, neutral score: 0.140000, negative score: 0.850000.
        Sentence sentiment: negative, positive score: 0.000000, neutral score: 0.000000, negative score: 1.000000.
            Aspect sentiment: negative, aspect text: atmosphere
                'negative' opinion sentiment because of "bad". Is the opinion negated: false.
        Sentence sentiment: negative, positive score: 0.020000, neutral score: 0.440000, negative score: 0.540000.
        Sentence sentiment: negative, positive score: 0.000000, neutral score: 0.000000, negative score: 1.000000.
            Aspect sentiment: negative, aspect text: Staff
                'negative' opinion sentiment because of "friendly". Is the opinion negated: true.
                'negative' opinion sentiment because of "helpful". Is the opinion negated: true.

Process finished with exit code 0
```

# <a name="version-30"></a>[Versión 3.0](#tab/version-3)

Cree una función denominada `sentimentAnalysisExample()` que tome el cliente que creó anteriormente y llame a su función `analyzeSentiment()`. El objeto `AnalyzeSentimentResult` devuelto contendrá `documentSentiment` y `sentenceSentiments` si la operación se realiza correctamente, o `errorMessage` si no. 

```java
static void sentimentAnalysisExample(TextAnalyticsClient client)
{
    // The text that need be analyzed.
    String text = "I had the best day of my life. I wish you were there with me.";

    DocumentSentiment documentSentiment = client.analyzeSentiment(text);
    System.out.printf(
        "Recognized document sentiment: %s, positive score: %s, neutral score: %s, negative score: %s.%n",
        documentSentiment.getSentiment(),
        documentSentiment.getConfidenceScores().getPositive(),
        documentSentiment.getConfidenceScores().getNeutral(),
        documentSentiment.getConfidenceScores().getNegative());

    for (SentenceSentiment sentenceSentiment : documentSentiment.getSentences()) {
        System.out.printf(
            "Recognized sentence sentiment: %s, positive score: %s, neutral score: %s, negative score: %s.%n",
            sentenceSentiment.getSentiment(),
            sentenceSentiment.getConfidenceScores().getPositive(),
            sentenceSentiment.getConfidenceScores().getNeutral(),
            sentenceSentiment.getConfidenceScores().getNegative());
        }
    }
}
```

### <a name="output"></a>Output

```console
Recognized document sentiment: positive, positive score: 1.0, neutral score: 0.0, negative score: 0.0.
Recognized sentence sentiment: positive, positive score: 1.0, neutral score: 0.0, negative score: 0.0.
Recognized sentence sentiment: neutral, positive score: 0.21, neutral score: 0.77, negative score: 0.02.
```

# <a name="version-21"></a>[Versión 2.1](#tab/version-2)

En este artículo solo se describe la versión 3.x de la API.

---

## <a name="language-detection"></a>Detección de idiomas

Cree una función denominada `detectLanguageExample()` que tome el cliente que creó anteriormente y llame a su función `detectLanguage()`. El objeto `DetectLanguageResult` devuelto contendrá un idioma principal detectado, una lista de otros idiomas detectados si la operación se realiza correctamente o `errorMessage` si no. Este ejemplo es el mismo para las versiones 3.0 y 3.1 de la API.

> [!Tip]
> En algunos casos, puede ser difícil eliminar la ambigüedad de los idiomas en función de la entrada. Puede usar el parámetro `countryHint` para especificar un código de país de dos letras. De forma predeterminada, la API usa "US" como valor predeterminado de countryHint; para eliminar este comportamiento, puede restablecer este parámetro y configurarlo como una cadena `countryHint = ""` vacía. Para establecer un valor predeterminado diferente, establezca la propiedad `TextAnalyticsClientOptions.DefaultCountryHint` y pásela durante la inicialización del cliente.

```java
static void detectLanguageExample(TextAnalyticsClient client)
{
    // The text that need be analyzed.
    String text = "Ce document est rédigé en Français.";

    DetectedLanguage detectedLanguage = client.detectLanguage(text);
    System.out.printf("Detected primary language: %s, ISO 6391 name: %s, score: %.2f.%n",
        detectedLanguage.getName(),
        detectedLanguage.getIso6391Name(),
        detectedLanguage.getConfidenceScore());
}
```

### <a name="output"></a>Output

```console
Detected primary language: French, ISO 6391 name: fr, score: 1.00.
```

## <a name="named-entity-recognition-ner"></a>Reconocimiento de entidades con nombre (NER)

# <a name="version-31-preview"></a>[Versión 3.1 (versión preliminar)](#tab/version-3-1)

> [!NOTE]
> En la versión `3.1`:
> * NER incluye métodos independientes para detectar información personal. 
> * La vinculación de entidad es una solicitud independiente distinta a la de NER.

Cree una función denominada `recognizeEntitiesExample()` que tome el cliente que creó anteriormente y llame a su función `recognizeEntities()`. El objeto devuelto `CategorizedEntityCollection` contendrá una lista de `CategorizedEntity` si la operación se realiza correctamente o `errorMessage` si no.

```java
static void recognizeEntitiesExample(TextAnalyticsClient client)
{
    // The text that need be analyzed.
    String text = "I had a wonderful trip to Seattle last week.";

    for (CategorizedEntity entity : client.recognizeEntities(text)) {
        System.out.printf(
            "Recognized entity: %s, entity category: %s, entity sub-category: %s, score: %s, offset: %s, length: %s.%n",
            entity.getText(),
            entity.getCategory(),
            entity.getSubcategory(),
            entity.getConfidenceScore(),
            entity.getOffset(),
            entity.getLength());
    }
}
```

### <a name="output"></a>Output

```console
Recognized entity: trip, entity category: Event, entity sub-category: null, score: 0.61, offset: 8, length: 4.
Recognized entity: Seattle, entity category: Location, entity sub-category: GPE, score: 0.82, offset: 16, length: 7.
Recognized entity: last week, entity category: DateTime, entity sub-category: DateRange, score: 0.8, offset: 24, length: 9.
```

### <a name="entity-linking"></a>Vinculación de entidad

Cree una función denominada `recognizeLinkedEntitiesExample()` que tome el cliente que creó anteriormente y llame a su función `recognizeLinkedEntities()`. El objeto devuelto `LinkedEntityCollection` contendrá una lista de `LinkedEntity` si la operación se realiza correctamente o `errorMessage` si no. Puesto que las entidades vinculadas se identifican de forma única, las apariciones de la misma entidad se agrupan bajo un objeto `LinkedEntity` como una lista de objetos `LinkedEntityMatch`.


```java
static void recognizeLinkedEntitiesExample(TextAnalyticsClient client)
{
    // The text that need be analyzed.
    String text = "Microsoft was founded by Bill Gates and Paul Allen on April 4, 1975, " +
        "to develop and sell BASIC interpreters for the Altair 8800. " +
        "During his career at Microsoft, Gates held the positions of chairman, " +
        "chief executive officer, president and chief software architect, " +
        "while also being the largest individual shareholder until May 2014.";

    System.out.printf("Linked Entities:%n");
    for (LinkedEntity linkedEntity : client.recognizeLinkedEntities(text)) {
        System.out.printf("Name: %s, ID: %s, URL: %s, Data Source: %s.%n",
            linkedEntity.getName(),
            linkedEntity.getDataSourceEntityId(),
            linkedEntity.getUrl(),
            linkedEntity.getDataSource());
        System.out.printf("Matches:%n");
        for (LinkedEntityMatch linkedEntityMatch : linkedEntity.getMatches()) {
            System.out.printf("Text: %s, Score: %.2f, Offset: %s, Length: %s%n",
            linkedEntityMatch.getText(),
            linkedEntityMatch.getConfidenceScore(),
            linkedEntityMatch.getOffset(),
            linkedEntityMatch.getLength());
        }
    }
}
```

### <a name="output"></a>Output

```console
Linked Entities:
Name: Microsoft, ID: Microsoft, URL: https://en.wikipedia.org/wiki/Microsoft, Data Source: Wikipedia.
Matches:
Text: Microsoft, Score: 0.55, Offset: 9, Length: 0
Text: Microsoft, Score: 0.55, Offset: 9, Length: 150
Name: Bill Gates, ID: Bill Gates, URL: https://en.wikipedia.org/wiki/Bill_Gates, Data Source: Wikipedia.
Matches:
Text: Bill Gates, Score: 0.63, Offset: 10, Length: 25
Text: Gates, Score: 0.63, Offset: 5, Length: 161
Name: Paul Allen, ID: Paul Allen, URL: https://en.wikipedia.org/wiki/Paul_Allen, Data Source: Wikipedia.
Matches:
Text: Paul Allen, Score: 0.60, Offset: 10, Length: 40
Name: April 4, ID: April 4, URL: https://en.wikipedia.org/wiki/April_4, Data Source: Wikipedia.
Matches:
Text: April 4, Score: 0.32, Offset: 7, Length: 54
Name: BASIC, ID: BASIC, URL: https://en.wikipedia.org/wiki/BASIC, Data Source: Wikipedia.
Matches:
Text: BASIC, Score: 0.33, Offset: 5, Length: 89
Name: Altair 8800, ID: Altair 8800, URL: https://en.wikipedia.org/wiki/Altair_8800, Data Source: Wikipedia.
Matches:
Text: Altair 8800, Score: 0.88, Offset: 11, Length: 116
```


### <a name="personally-identifiable-information-recognition"></a>Reconocimiento de información de identificación personal

Cree una función denominada `recognizePiiEntitiesExample()` que tome el cliente que creó anteriormente y llame a su función `recognizePiiEntities()`. El objeto devuelto `PiiEntityCollection` contendrá una lista de `PiiEntity` si la operación se realiza correctamente o `errorMessage` si no. También contendrá el texto censurado, que consta del texto de entrada con todas las entidades identificables reemplazadas por `*****`.

```java
static void recognizePiiEntitiesExample(TextAnalyticsClient client)
{
    // The text that need be analyzed.
    String document = "My SSN is 859-98-0987";
    PiiEntityCollection piiEntityCollection = client.recognizePiiEntities(document);
    System.out.printf("Redacted Text: %s%n", piiEntityCollection.getRedactedText());
    piiEntityCollection.forEach(entity -> System.out.printf(
        "Recognized Personally Identifiable Information entity: %s, entity category: %s, entity subcategory: %s,"
            + " confidence score: %f.%n",
        entity.getText(), entity.getCategory(), entity.getSubcategory(), entity.getConfidenceScore()));
}
```

### <a name="output"></a>Output

```console
Redacted Text: My SSN is ***********
Recognized Personally Identifiable Information entity: 859-98-0987, entity category: U.S. Social Security Number (SSN), entity subcategory: null, confidence score: 0.650000.
```

# <a name="version-30"></a>[Versión 3.0](#tab/version-3)

> [!NOTE]
> En la versión `3.0`:
> * NER incluye métodos independientes para detectar información personal. 
> * La vinculación de entidad es una solicitud independiente distinta a la de NER.

Cree una función denominada `recognizeEntitiesExample()` que tome el cliente que creó anteriormente y llame a su función `recognizeEntities()`. El objeto devuelto `CategorizedEntityCollection` contendrá una lista de `CategorizedEntity` si la operación se realiza correctamente o `errorMessage` si no.

```java
static void recognizeEntitiesExample(TextAnalyticsClient client)
{
    // The text that need be analyzed.
    String text = "I had a wonderful trip to Seattle last week.";

    for (CategorizedEntity entity : client.recognizeEntities(text)) {
        System.out.printf(
            "Recognized entity: %s, entity category: %s, entity sub-category: %s, score: %s.%n",
            entity.getText(),
            entity.getCategory(),
            entity.getSubcategory(),
            entity.getConfidenceScore());
    }
}
```

### <a name="output"></a>Output

```console
Recognized entity: trip, entity category: Event, entity sub-category: null, score: 0.61.
Recognized entity: Seattle, entity category: Location, entity sub-category: GPE, score: 0.82.
Recognized entity: last week, entity category: DateTime, entity sub-category: DateRange, score: 0.8.
```

### <a name="entity-linking"></a>Vinculación de entidad

Cree una función denominada `recognizeLinkedEntitiesExample()` que tome el cliente que creó anteriormente y llame a su función `recognizeLinkedEntities()`. El objeto devuelto `LinkedEntityCollection` contendrá una lista de `LinkedEntity` si la operación se realiza correctamente o `errorMessage` si no. Puesto que las entidades vinculadas se identifican de forma única, las apariciones de la misma entidad se agrupan bajo un objeto `LinkedEntity` como una lista de objetos `LinkedEntityMatch`.

```java
static void recognizeLinkedEntitiesExample(TextAnalyticsClient client)
{
    // The text that need be analyzed.
    String text = "Microsoft was founded by Bill Gates and Paul Allen on April 4, 1975, " +
        "to develop and sell BASIC interpreters for the Altair 8800. " +
        "During his career at Microsoft, Gates held the positions of chairman, " +
        "chief executive officer, president and chief software architect, " +
        "while also being the largest individual shareholder until May 2014.";

    System.out.printf("Linked Entities:%n");
    for (LinkedEntity linkedEntity : client.recognizeLinkedEntities(text)) {
        System.out.printf("Name: %s, ID: %s, URL: %s, Data Source: %s.%n",
            linkedEntity.getName(),
            linkedEntity.getDataSourceEntityId(),
            linkedEntity.getUrl(),
            linkedEntity.getDataSource());
        System.out.printf("Matches:%n");
        for (LinkedEntityMatch linkedEntityMatch : linkedEntity.getMatches()) {
            System.out.printf("Text: %s, Score: %.2f%n",
            linkedEntityMatch.getText(),
            linkedEntityMatch.getConfidenceScore());
        }
    }
}
```

### <a name="output"></a>Output

```console
Linked Entities:
Name: Altair 8800, ID: Altair 8800, URL: https://en.wikipedia.org/wiki/Altair_8800, Data Source: Wikipedia.
Matches:
Text: Altair 8800, Score: 0.88
Name: Bill Gates, ID: Bill Gates, URL: https://en.wikipedia.org/wiki/Bill_Gates, Data Source: Wikipedia.
Matches:
Text: Bill Gates, Score: 0.63
Text: Gates, Score: 0.63
Name: Paul Allen, ID: Paul Allen, URL: https://en.wikipedia.org/wiki/Paul_Allen, Data Source: Wikipedia.
Matches:
Text: Paul Allen, Score: 0.60
Name: Microsoft, ID: Microsoft, URL: https://en.wikipedia.org/wiki/Microsoft, Data Source: Wikipedia.
Matches:
Text: Microsoft, Score: 0.55
Text: Microsoft, Score: 0.55
Name: April 4, ID: April 4, URL: https://en.wikipedia.org/wiki/April_4, Data Source: Wikipedia.
Matches:
Text: April 4, Score: 0.32
Name: BASIC, ID: BASIC, URL: https://en.wikipedia.org/wiki/BASIC, Data Source: Wikipedia.
Matches:
Text: BASIC, Score: 0.33
```

# <a name="version-21"></a>[Versión 2.1](#tab/version-2)

En este artículo solo se describe la versión 3.x de la API.

---

## <a name="key-phrase-extraction"></a>Extracción de la frase clave

Cree una función denominada `extractKeyPhrasesExample()` que tome el cliente que creó anteriormente y llame a su función `extractKeyPhrases()`. El objeto `ExtractKeyPhraseResult` devuelto contendrá una lista de frases clave si la operación se realiza correctamente o `errorMessage` si no. Este ejemplo es el mismo para las versiones 3.0 y 3.1 de la API.

```java
static void extractKeyPhrasesExample(TextAnalyticsClient client)
{
    // The text that need be analyzed.
    String text = "My cat might need to see a veterinarian.";

    System.out.printf("Recognized phrases: %n");
    for (String keyPhrase : client.extractKeyPhrases(text)) {
        System.out.printf("%s%n", keyPhrase);
    }
}
```

### <a name="output"></a>Output

```console
Recognized phrases: 
cat
veterinarian
```