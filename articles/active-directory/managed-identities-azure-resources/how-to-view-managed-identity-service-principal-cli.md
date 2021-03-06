---
title: 'Visualización de la entidad de servicio de una identidad administrada: CLI de Azure: Azure AD'
description: Instrucciones detalladas para ver la entidad de servicio de una identidad administrada mediante la CLI de Azure.
services: active-directory
documentationcenter: ''
author: barclayn
manager: daveba
editor: ''
ms.service: active-directory
ms.subservice: msi
ms.devlang: na
ms.topic: how-to
ms.tgt_pltfrm: na
ms.workload: identity
ms.date: 09/30/2020
ms.author: barclayn
ms.collection: M365-identity-device-management
ms.custom: devx-track-azurecli
ms.openlocfilehash: 1c0f167a36ceff6a9b62e2a3ccf24ca6e13e6294
ms.sourcegitcommit: 829d951d5c90442a38012daaf77e86046018e5b9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2020
ms.locfileid: "91611918"
---
# <a name="view-the-service-principal-of-a-managed-identity-using-azure-cli"></a>Visualización de la entidad de servicio de una identidad administrada mediante la CLI de Azure

Las identidades administradas para los recursos de Azure proporcionan a los servicios de Azure una identidad administrada automáticamente en Azure Active Directory. Puede usar esta identidad para autenticar a cualquier servicio que admita la autenticación de Azure AD, sin necesidad de tener credenciales en el código. 

En este artículo, obtendrá información sobre cómo visualizar la entidad de servicio de una identidad administrada mediante la CLI de Azure.

## <a name="prerequisites"></a>Prerequisites

- Si no está familiarizado con las identidades administradas de los recursos de Azure, consulte la [sección de introducción](overview.md).
- Si aún no tiene una cuenta de Azure, [regístrese para obtener una cuenta gratuita](https://azure.microsoft.com/free/).
- Habilite la [identidad asignada por el sistema en una máquina virtual](./qs-configure-portal-windows-vm.md#system-assigned-managed-identity) o [aplicación](../../app-service/overview-managed-identity.md#add-a-system-assigned-identity).
- Para ejecutar los scripts de ejemplo, tiene dos opciones:
    - Use [Azure Cloud Shell](../../cloud-shell/overview.md), que puede abrir mediante el botón **Probar** en la esquina superior derecha de los bloques de código.
    - Ejecute scripts localmente instalando la versión más reciente de la [CLI de Azure](/cli/azure/install-azure-cli) y, a continuación, inicie sesión en Azure con [az login](/cli/azure/reference-index#az-login). Use una cuenta asociada a la suscripción de Azure en la que desea crear recursos.   

## <a name="view-the-service-principal"></a>Visualización de la entidad de servicio

El comando siguiente muestra cómo ver la entidad de servicio de una aplicación o máquina virtual con la identidad administrada habilitada. Reemplazar `<Azure resource name>` por sus propios valores.

```azurecli-interactive
az ad sp list --display-name <Azure resource name>
```

## <a name="next-steps"></a>Pasos siguientes

Para obtener más información sobre cómo administrar las entidades de servicio de Azure AD con la CLI de Azure, vea [az ad sp](/cli/azure/ad/sp).
