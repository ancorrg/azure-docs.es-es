---
title: DNS personalizado
titleSuffix: Azure SQL Managed Instance
description: En este tema se describen las opciones de configuración de un DNS personalizado con Azure SQL Managed Instance.
services: sql-database
ms.service: sql-managed-instance
ms.subservice: operations
ms.custom: sqldbrb=1
ms.devlang: ''
ms.topic: conceptual
author: srdan-bozovic-msft
ms.author: srbozovi
ms.reviewer: sstein, bonova
ms.date: 07/17/2019
ms.openlocfilehash: 017698975706aa8501cd059351cf9a9d88594f77
ms.sourcegitcommit: 400f473e8aa6301539179d4b320ffbe7dfae42fe
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "92779907"
---
# <a name="configure-a-custom-dns-for-azure-sql-managed-instance"></a>Configuración de un DNS personalizado para Azure SQL Managed Instance
[!INCLUDE[appliesto-sqlmi](../includes/appliesto-sqlmi.md)]

Instancia administrada de Azure SQL tiene que implementarse dentro de una [red virtual (VNet)](../../virtual-network/virtual-networks-overview.md) de Azure. Hay algunos escenarios (por ejemplo, correo electrónico de base de datos o servidores vinculados a otras instancias de SQL Server en la nube o el entorno híbrido) que requieren que los nombres de host privados se resuelvan en SQL Managed Instance. En este caso, debe configurar un DNS personalizado dentro de Azure. 

Como Instancia administrada de SQL usa el mismo DNS para su funcionamiento interno, configure el servidor DNS personalizado para que pueda resolver los nombres de dominio públicos.

> [!IMPORTANT]
> Utilice siempre nombres de dominio completos (FQDN) para el servidor de correo electrónico, la instancia de SQL Server y otros servicios, aunque se encuentren en la zona DNS privada. Por ejemplo, `smtp.contoso.com` para el servidor de correo, ya que `smtp` no se resolverá correctamente. La creación de un servidor vinculado o una replicación que haga referencia a las máquinas virtuales de SQL Server de la misma red virtual también requiere un nombre de dominio completo y un sufijo DNS predeterminado. Por ejemplo, `SQLVM.internal.cloudapp.net`. Para más información, consulte [Resolución de nombres con su propio servidor DNS](../../virtual-network/virtual-networks-name-resolution-for-vms-and-role-instances.md#name-resolution-that-uses-your-own-dns-server).

> [!IMPORTANT]
> La actualización de los servidores DNS de una red virtual no afectará de inmediato a Instancia administrada de SQL. La configuración de DNS de SQL Managed Instance se actualiza una vez que expira la concesión de DHCP o se actualiza la plataforma, lo que ocurra primero. **Se recomienda que los usuarios establezcan la configuración de DNS de la red virtual antes de crear su primera instancia administrada.**

## <a name="next-steps"></a>Pasos siguientes

- Para obtener información general, consulte [¿Qué es Azure SQL Managed Instance?](sql-managed-instance-paas-overview.md).
- Se puede encontrar un tutorial que muestra cómo crear una instancia administrada en [Creación de instancias administradas](instance-create-quickstart.md).
- Para información sobre cómo configurar una red virtual para una instancia administrada, consulte [Configuración de la red virtual para las instancias administradas](connectivity-architecture-overview.md).