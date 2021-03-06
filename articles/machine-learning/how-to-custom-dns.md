---
title: Uso de un servidor DNS personalizado
titleSuffix: Azure Machine Learning
description: Cómo configurar un servidor DNS personalizado para trabajar con un área de trabajo de Azure Machine Learning y un punto de conexión privado.
services: machine-learning
ms.service: machine-learning
ms.subservice: core
ms.reviewer: larryfr
ms.author: jhirono
author: jhirono
ms.date: 10/05/2020
ms.topic: conceptual
ms.custom: how-to
ms.openlocfilehash: 1d215c9564d89e5bd410e68839807f5c2c752356
ms.sourcegitcommit: d2222681e14700bdd65baef97de223fa91c22c55
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/07/2020
ms.locfileid: "91828298"
---
# <a name="how-to-use-your-workspace-with-a-custom-dns-server"></a>Uso de un área de trabajo con un servidor DNS personalizado

Al usar Azure Machine Learning con una red virtual, hay [varias maneras de controlar la resolución de nombres DNS](/azure/virtual-network/virtual-networks-name-resolution-for-vms-and-role-instances). De manera predeterminada, Azure controla automáticamente la resolución de nombres para el área de trabajo y el punto de conexión privado. Sin embargo, __al usar su propio servidor DNS personalizado__, debe crear manualmente las entradas DNS para el área de trabajo.

> [!IMPORTANT]
> En este artículo solo se explica cómo buscar el nombre de dominio completo (FQDN) y las direcciones IP para estas entradas; NO se proporciona información sobre cómo configurar los registros DNS para estos elementos. Consulte la documentación del software de DNS para obtener información sobre cómo agregar registros.

## <a name="prerequisites"></a>Prerrequisitos

- Una instancia de Azure Virtual Network que use [su propio servidor DNS](/azure/virtual-network/virtual-networks-name-resolution-for-vms-and-role-instances#name-resolution-that-uses-your-own-dns-server).

- Un área de trabajo de Azure Machine Learning con un punto de conexión privado. Para más información, consulte [Creación de un área de trabajo de Azure Machine Learning](how-to-manage-workspace.md).

- Familiaridad con el uso del [aislamiento de red durante el entrenamiento e inferencia](how-to-enable-virtual-network.md).

- De manera opcional, la [CLI de Azure](https://docs.microsoft.com/cli/azure/install-azure-cli) o [Azure PowerShell](https://docs.microsoft.com/powershell/azure/install-az-ps).

## <a name="find-the-ip-addresses"></a>Búsqueda de direcciones IP

La lista siguiente contiene los nombres de dominio completos (FQDN) que usa el área de trabajo y el punto de conexión privado:

* `<workspace-GUID>.workspace.<region>.api.azureml.ms`
* `<workspace-GUID>.studio.workspace.<region>.api.azureml.ms`
* `cert-<workspace-GUID>.workspace.<region>.api.azureml.ms`
* `<workspace-GUID>.workspace.<region>.experiments.azureml.net`
* `<workspace-GUID>.workspace.<region>.modelmanagement.azureml.net`
* `<workspace-GUID>.workspace.<region>.aether.ms`
* `ml-<workspace-name>-<region>-<workspace-guid>.notebooks.azure.ml`
* Si crea una instancia de proceso, también debe agregar una entrada para `<instance-name>.<region>.instances.azureml.ms`.

Para buscar las direcciones IP internas de los FQDN en la red virtual, use uno de los métodos siguientes:

> [!NOTE]
> Los nombres de dominio completos y las direcciones IP serán diferentes en función de la configuración. Por ejemplo, el valor de GUID en el nombre de dominio será específico del área de trabajo.

# <a name="azure-cli"></a>[CLI de Azure](#tab/azure-cli)

```azurecli
az network private-endpoint show --endpoint-name <endpoint> --resource-group <resource-group> --query 'customDnsConfigs[*].{FQDN: fqdn, IPAddress: ipAddresses[0]}' --output table
```

# <a name="azure-powershell"></a>[Azure PowerShell](#tab/azure-powershell)

```azurepowershell
$workspaceDns=Get-AzPrivateEndpoint -Name <endpoint> -resourcegroupname <resource-group>
$workspaceDns.CustomDnsConfigs | format-table
```

# <a name="azure-portal"></a>[Azure Portal](#tab/azure-portal)

1. En [Azure Portal](https://portal.azure.com), seleccione el __área de trabajo__ de Azure Machine Learning.
1. En la sección __Configuración__, seleccione __Conexiones de punto de conexión privado__.
1. Seleccione el vínculo en la columna __Punto de conexión privado__ que se muestra.
1. Al final de la página se muestra una lista de los nombres de dominio completos (FQDN) y las direcciones IP del punto de conexión privado del área de trabajo.

:::image type="content" source="./media/how-to-custom-dns/private-endpoint-custom-dns.png" alt-text="Lista de los FQDN en el portal":::

---

La información devuelta por todos los métodos es la misma; una lista de los FQDN y las direcciones IP privadas para los recursos.

| FQDN | Dirección IP |
| ----- | ----- |
| `fb7e20a0-8891-458b-b969-55ddb3382f51.workspace.eastus.api.azureml.ms` | `10.1.0.5` |
| `fb7e20a0-8891-458b-b969-55ddb3382f51.studio.workspace.eastus.api.azureml.ms` | `10.1.0.5` |
| `cert-fb7e20a0-8891-458b-b969-55ddb3382f51.workspace.eastus.api.azureml.ms` | `10.1.0.5` |
| `ml-myworkspace-eastus-fb7e20a0-8891-458b-b969-55ddb3382f51.notebooks.azure.net` | `10.1.0.6` |

> [!IMPORTANT]
> El punto de conexión privado no enumera algunos FQDN, pero estos son necesarios en el área de trabajo. Estos FQDN se muestran en la tabla siguiente y también se deben agregar al servidor DNS:
>
> * `<workspace-GUID>.workspace.<region>.experiments.azureml.net`
> * `<workspace-GUID>.workspace.<region>.modelmanagement.azureml.net`
> * `<workspace-GUID>.workspace.<region>.aether.ms`
> * Si tiene una instancia de proceso, use `<instance-name>.<region>.instances.azureml.ms`, donde `<instance-name>` es el nombre de la instancia de proceso.
>
> Para todas estas direcciones IP, use la misma dirección que las entradas `*.api.azureml.ms` devueltas en los pasos anteriores.

## <a name="next-steps"></a>Pasos siguientes

Para obtener más información sobre el uso de Azure Machine Learning con una red virtual, consulte la [información general sobre la red virtual](how-to-network-security-overview.md).