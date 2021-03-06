---
title: 'Determinación de la opción de publicación: marketplace comercial de Microsoft'
description: En este artículo se describen los criterios de idoneidad y los requisitos para publicar ofertas en Microsoft AppSource y Azure Marketplace.
ms.service: marketplace
ms.subservice: partnercenter-marketplace-publisher
ms.topic: conceptual
author: keferna
ms.author: keferna
ms.date: 09/04/2020
ms.openlocfilehash: 4acdd8bfd567a317b954d58629468fa8cd929669
ms.sourcegitcommit: 829d951d5c90442a38012daaf77e86046018e5b9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2020
ms.locfileid: "90032391"
---
# <a name="determine-your-publishing-option"></a>Determinar la opción de publicación

La opción de publicación que elige para su oferta está relacionada directamente con los requisitos de idoneidad y las ventajas de GTM de Marketplace comercial. Y, aún más importante, la selección de la opción de publicación y el tipo de oferta definen cómo interactúan los usuarios con su oferta de Marketplace comercial.

Para configurar su oferta, debe comprender los siguientes conceptos clave del marketplace comercial: las opciones de publicación, la configuración y los tipos de oferta, y las opciones de descripción que rigen cómo y dónde se presenta la oferta en las tiendas en línea del marketplace comercial.

En este artículo, aprenderá lo siguiente:

- Cómo determinar la tienda en línea adecuada para su solución.
- Qué opciones de publicación y descripción están disponibles en cada tienda en línea.
- Qué tipos de ofertas están disponibles para cada opción de publicación.

## <a name="commercial-marketplace-publishing-options"></a>Opciones de publicación de Marketplace comercial

En la tabla siguiente se muestran las opciones de publicación de los tipos de oferta en Microsoft AppSource y Azure Marketplace.

|   | **Lista (contacto)**  | **Lista (evaluación)**  | **Gratis** | **BYOL** | **Transacción**|
| :--------- | :----------- | :------------ | :----------- | :---------- |:---------- |
| **Máquina virtual** |  |  |  | Azure Marketplace |  Azure Marketplace |
| **Aplicaciones de Azure (varias máquinas virtuales)** |  |  | Azure Marketplace | Azure Marketplace | Azure Marketplace  |
| **Imagen de contenedor** |  |  | Azure Marketplace | Azure Marketplace |   |
| **Módulo IoT Edge** |  |  | Azure Marketplace | Azure Marketplace |   |
| **Servicios administrados** |  |  |  | Azure Marketplace |   |
| **Servicios de consultoría** | Ambas tiendas en línea |  |  |  |   |
| **Aplicación SaaS** | Ambas tiendas en línea | Ambas tiendas en línea | Ambas tiendas en línea |  | Ambas tiendas en línea* |
| **Aplicación de Microsoft 365** | AppSource | AppSource |  |  | AppSource**  |
| **Complemento de Dynamics 365** |  AppSource | AppSource |  |  |   |
| **PowerApps** | AppSource |AppSource  |  |  |   |

&#42;Las ofertas de transacción de aplicación SaaS en Microsoft AppSource actualmente son con tarjeta de crédito.

&#42;&#42; Las ofertas de Microsoft 365 se instalan gratis y se pueden monetizar a través de una oferta de SaaS como servicio de licencia. Para más información, consulte el artículo sobre cómo [monetizar el complemento de Microsoft 365 a través del marketplace comercial de Microsoft](/office/dev/store/monetize-addins-through-microsoft-commercial-marketplace).

## <a name="choose-a-listing-option"></a>Selección de una opción de publicación

Las opciones de publicación disponibles ofrecen distintos compromisos para los clientes y proporcionan acceso al uso compartido de clientes potenciales y a las [ventajas del marketplace comercial](https://docs.microsoft.com/azure/marketplace/gtm-your-marketplace-benefits). Tenga en cuenta las opciones de oferta que se corresponden con la opción de publicación:

| **Opción de publicación**    | **Descripción**  |
| :------------------- | :-------------------|
| **Lista** | Descripción sencilla de la aplicación o servicio que permite a los usuarios del marketplace comercial solicitarle que se conecte con el cliente a través de las opciones de descripción para **Ponerse en contacto conmigo**. |
| **Versión de prueba** | Use Marketplace comercial para mejorar la detectabilidad y automatizar el aprovisionamiento de la experiencia de evaluación de la solución, permitiendo a los usuarios potenciales usar su experiencia dentro de la aplicación de Microsoft, SaaS o IaaS sin ningún costo extra durante un tiempo limitado antes de comprarla. Las opciones de descripción que se usan para la opción de publicación de prueba son: **Evaluación gratuita** o **Versión de prueba**. |
| **BYOL** | Use Marketplace comercial para mejorar la detectabilidad y automatizar el aprovisionamiento de su solución, así como para completar la transacción financiera por separado. Los tipos de ofertas BYOL son ideales para las migraciones desde el entorno local a la nube. La opción de descripción es **Obtenerlo ahora**.
| **Transacción** | Las ofertas de Transact se venden a través de Marketplace comercial. Microsoft es responsable de la facturación y el cobro. La opción de descripción es **Obtenerlo ahora**.|

> [!Note]
> Cuando se usa la opción de publicación de transacciones, es importante comprender las consideraciones sobre precios, facturación y pago antes de seleccionar un tipo de oferta y crear la oferta. Para más información, revise el artículo sobre las [funcionalidades de transacción de Marketplace comercial](./marketplace-commercial-transaction-capabilities-and-considerations.md).

## <a name="selecting-an-online-store"></a>Selección de una tienda en línea

Cada tienda en línea cumple diferentes requisitos del cliente para las soluciones empresariales y de TI. El tipo de oferta, las funcionalidades de transacción y la categoría determinarán dónde se publicará la oferta. Las categorías y subcategorías se asignan a cada tienda en línea en función del tipo de solución publicada:

**Microsoft AppSource** ofrece soluciones empresariales, como soluciones del sector y servicios de consultoría, para Dynamics 365, Microsoft 365 y Power Platform.

**Azure Marketplace** ofrece soluciones de TI creadas para Azure o en dicha plataforma, así como servicios de consultoría que agilizan cómo tus clientes usan Azure.

Seleccione la categoría y la subcategoría que mejor coincida con el tipo de solución. Por ejemplo, un firewall de aplicaciones web es una solución de TI que debe publicarse en Azure Marketplace, en la categoría de seguridad. Una aplicación de administración de contratos es una solución empresarial que debe publicarse en AppSource, en la categoría de ventas. La selección de una categoría o subcategoría incorrecta puede hacer que la oferta se publique en la tienda en línea equivocada.

### <a name="publishing-to-both-online-stores-saas-offers-only"></a>Publicación en ambas tiendas en línea (solo ofertas de SaaS)

Las ofertas de SaaS pueden publicarse en Azure Marketplace o AppSource. Si la oferta de SaaS se encuentra en *ambas* categorías; es decir, es una solución de TI (Azure Marketplace) y una solución empresarial (AppSource), seleccione una categoría o una subcategoría aplicable a cada tienda en línea. Las ofertas publicadas en ambas tiendas en línea deben tener una propuesta de valor como solución de TI *y* como solución empresarial.

> [!IMPORTANT]
> Las ofertas de SaaS con [facturación medida](partner-center-portal/saas-metered-billing.md) están disponibles a través de Azure Marketplace y Azure Portal. Las ofertas de SaaS con planes privados exclusivamente están disponibles en Azure Portal.

| Facturación de uso medido | Plan público | Plan privado | Disponible en: |
|---|---|---|---|
| Sí             | Sí         | No           | Azure Marketplace y Azure Portal |
| Sí             | Sí         | Sí          | Azure Marketplace y Azure Portal* |
| Sí             | No          | Sí          | Azure Portal solamente |
| No              | No          | Sí          | Azure Portal solamente |

&#42; El plan privado de la oferta solo estará disponible en Azure Portal.

Por ejemplo, una oferta con facturación de uso medido y un plan privado solo (ningún plan público) lo comprarán los clientes en Azure Portal. Obtenga más información sobre [Ofertas privadas en el marketplace comercial de Microsoft](private-offers.md).

### <a name="categories"></a>Categorías

Las categorías y subcategorías se asignan a cada tienda en línea en función del tipo de solución. Seleccione las categorías y subcategorías que mejor se adapten a su solución. Puede seleccionar:

- Al menos una categoría, hasta un máximo de dos. Puede elegir una categoría principal y una secundaria.
- Hasta dos subcategorías para cada categoría principal o secundaria. Si no selecciona ninguna subcategoría, la oferta se podrá detectar en la categoría seleccionada.

[!INCLUDE [categories and subcategories](./includes/categories.md)]

## <a name="next-steps"></a>Pasos siguientes

- Una vez que elija una opción de publicación, revise la [guía de publicación por tipo de oferta](./publisher-guide-by-offer-type.md).
