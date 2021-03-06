---
title: Características compatibles disponibles en Azure Security Center | Microsoft Docs
description: En este documento se proporciona una lista de servicios compatibles con Azure Security Center.
services: security-center
documentationcenter: na
author: memildin
manager: rkarlin
ms.assetid: 870ebc8d-1fad-435b-9bf9-c477f472ab17
ms.service: security-center
ms.devlang: na
ms.topic: overview
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/12/2020
ms.author: memildin
ms.openlocfilehash: 59a87e7c91266dd1ec2d7263df7149d07f6e7ce8
ms.sourcegitcommit: f88074c00f13bcb52eaa5416c61adc1259826ce7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "92342304"
---
# <a name="feature-coverage-for-machines"></a>Cobertura de características para las máquinas

En las dos tablas siguientes se muestran las características de Azure Security Center disponibles para las máquinas virtuales y los servidores Windows y Linux.

## <a name="supported-features-for-virtual-machines-and-servers"></a>Características admitidas para máquinas virtuales y servidores <a name="vm-server-features"></a>

### <a name="windows-machines"></a>[**Máquinas Windows**](#tab/features-windows)

|**Característica**|**Azure Virtual Machines**|**Azure Virtual Machine Scale Sets**|**Máquinas habilitadas para Azure Arc**|**Azure Defender necesario**
|----|:----:|:----:|:----:|:----:|
|[Integración de ATP de Microsoft Defender](security-center-wdatp.md)|✔</br>✔ (en versiones admitidas)|✔</br>✔ (en versiones admitidas)|✔|Sí|
|[Análisis del comportamiento de máquinas virtuales (y alertas de seguridad)](alerts-reference.md)|✔|✔|✔|Sí|
|[Alertas de seguridad sin archivos](alerts-reference.md#alerts-windows)|✔|✔|✔|Sí|
|[Alertas de seguridad basadas en la red](other-threat-protections.md#network-layer)|✔|✔|-|Sí|
|[Acceso de máquina virtual Just-In-Time](security-center-just-in-time.md)|✔|-|-|Sí|
|[Evaluación de vulnerabilidades nativa](deploy-vulnerability-assessment-vm.md#overview-of-the-integrated-vulnerability-scanner)|✔|-|-|Sí|
|[Supervisión de la integridad de los archivos](security-center-file-integrity-monitoring.md)|✔|✔|✔|Sí|
|[Controles de aplicación adaptables](security-center-adaptive-application.md)|✔|-|✔|Sí|
|[Mapa de red](security-center-network-recommendations.md#network-map)|✔|✔|-|Sí|
|[Protección de red adaptable](security-center-adaptive-network-hardening.md)|✔|-|-|Sí|
|[Panel e informes de cumplimiento normativo](security-center-compliance-dashboard.md)|✔|✔|✔|Sí|
|Recomendaciones y protección frente a amenazas en contenedores IaaS hospedados en Docker|-|-|-|Sí|
|Evaluación de revisiones de SO que faltan|✔|✔|✔|Azure: No<br><br>Habilitada para Arc: Sí|
|Evaluación de configuraciones de seguridad incorrectas|✔|✔|✔|Azure: No<br><br>Habilitada para Arc: Sí|
|[Evaluación de EndPoint Protection](security-center-services.md#supported-endpoint-protection-solutions-)|✔|✔|✔|Azure: No<br><br>Habilitada para Arc: Sí|
|Evaluación de Disk Encryption|✔</br>(para [escenarios admitidos](../virtual-machines/windows/disk-encryption-windows.md#unsupported-scenarios))|✔|-|No|
|Evaluación de vulnerabilidades de terceros|✔|-|-|No|
|[Evaluación de la seguridad de red](security-center-network-recommendations.md)|✔|✔|-|No|


### <a name="linux-machines"></a>[**Máquinas Linux**](#tab/features-linux)

|**Característica**|**Azure Virtual Machines**|**Azure Virtual Machine Scale Sets**|**Máquinas habilitadas para Azure Arc**|**Azure Defender necesario**
|----|:----:|:----:|:----:|:----:|
|[Integración de ATP de Microsoft Defender](security-center-wdatp.md)|-|-|-|Sí|
|[Análisis del comportamiento de máquinas virtuales (y alertas de seguridad)](./azure-defender.md)|✔</br>✔ (en versiones admitidas)|✔</br>✔ (en versiones admitidas)|✔|Sí|
|[Alertas de seguridad sin archivos](alerts-reference.md#alerts-windows)|-|-|-|Sí|
|[Alertas de seguridad basadas en la red](other-threat-protections.md#network-layer)|✔|✔|-|Sí|
|[Acceso de máquina virtual Just-In-Time](security-center-just-in-time.md)|✔|-|-|Sí|
|[Evaluación de vulnerabilidades nativa](deploy-vulnerability-assessment-vm.md#overview-of-the-integrated-vulnerability-scanner)|✔|-|-|Sí|
|[Supervisión de la integridad de los archivos](security-center-file-integrity-monitoring.md)|✔|✔|✔|Sí|
|[Controles de aplicación adaptables](security-center-adaptive-application.md)|✔|-|✔|Sí|
|[Mapa de red](security-center-network-recommendations.md#network-map)|✔|✔|-|Sí|
|[Protección de red adaptable](security-center-adaptive-network-hardening.md)|✔|-|-|Sí|
|[Panel e informes de cumplimiento normativo](security-center-compliance-dashboard.md)|✔|✔|✔|Sí|
|Recomendaciones y protección frente a amenazas en contenedores IaaS hospedados en Docker|✔|✔|✔|Sí|
|Evaluación de revisiones de SO que faltan|✔|✔|✔|Azure: No<br><br>Habilitada para Arc: Sí|
|Evaluación de configuraciones de seguridad incorrectas|✔|✔|✔|Azure: No<br><br>Habilitada para Arc: Sí|
|[Evaluación de EndPoint Protection](security-center-services.md#supported-endpoint-protection-solutions-)|-|-|-|No|
|Evaluación de Disk Encryption|✔</br>(para [escenarios admitidos](../virtual-machines/windows/disk-encryption-windows.md#unsupported-scenarios))|✔|-|No|
|Evaluación de vulnerabilidades de terceros|✔|-|-|No|
|[Evaluación de la seguridad de red](security-center-network-recommendations.md)|✔|✔|-|No|

--- 


> [!TIP]
>Para experimentar con características que solo están disponibles con Azure Defender, puede inscribirse en una evaluación de treinta días. Consulte la [página de precios](https://azure.microsoft.com/pricing/details/security-center/)para obtener más información.


## <a name="supported-endpoint-protection-solutions"></a>Soluciones de protección de punto de conexión compatibles <a name="endpoint-supported"></a>

En la tabla siguiente se proporciona una matriz de:

 - Si puede usar Azure Security Center para instalar cada solución para usted.
 - Qué soluciones de protección de punto de conexión puede detectar Security Center. Si se detecta una de las soluciones de protección de punto de conexión de esta lista, Security Center no recomendará instalar ninguna.

Para más información sobre cuándo se generan recomendaciones para cada una de estas protecciones, vea [Evaluación y recomendaciones de Endpoint Protection](security-center-endpoint-protection.md).

| Endpoint Protection| Plataformas | Instalación de Security Center | Detección de Security Center |
|------|------|-----|-----|
| Antivirus de Microsoft Defender| Windows Server 2016 o posterior| No, se integra en el sistema operativo.| Sí |
| System Center Endpoint Protection (Microsoft Antimalware) | Windows Server 2012 R2, 2012, 2008 R2 (consulte la nota que hay a continuación) | Mediante extensión | Sí |
| Trend Micro: Deep Security | Familia de Windows Server  | No | Sí |
| Symantec v12.1.1100+| Familia de Windows Server  | No | Sí |
| McAfee v10 o posterior | Familia de Windows Server  | No | Sí |
| McAfee v10 o posterior | Familia de Linux Server  | No | Sí * *\** _ |
| Sophos V9+| Familia de Linux Server  | No | Sí  _*\**_  |

 _ *\** * El estado de cobertura y los datos auxiliares solo están disponibles en el área de trabajo de Log Analytics asociada con las suscripciones protegidas. No se refleja en el portal de Azure Security Center.

> [!NOTE]
> La detección de System Center Endpoint Protection (SCEP) en una máquina virtual de Windows Server 2008 R2 requiere que SCEP se instale después de PowerShell 0 (v3.0 o una versión superior).


## <a name="next-steps"></a>Pasos siguientes

- Obtenga información sobre cómo [Security Center recopila datos mediante el agente de Log Analytics](security-center-enable-data-collection.md).
- Obtenga información sobre cómo [Security Center administra y protege los datos](security-center-data-security.md).
- Revise las [plataformas compatibles con Security Center](security-center-os-coverage.md).