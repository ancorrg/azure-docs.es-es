---
services: storage
author: normesta
ms.service: storage
ms.topic: include
ms.date: 09/29/2020
ms.author: normesta
ms.custom: include file
ms.openlocfilehash: 73a8f20122e21c4557289995c15b008401285011
ms.sourcegitcommit: 33368ca1684106cb0e215e3280b828b54f7e73e8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "92131656"
---
En las entradas de ACL, use siempre [grupos de seguridad de Azure AD](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-manage-groups) como entidad de seguridad asignada. Ofrece la oportunidad de asignar directamente usuarios individuales o entidades de servicio. Con esta estructura, podrá agregar y quitar usuarios o entidades de servicio sin necesidad de volver a aplicar las ACL en una estructura de directorios completa. En su lugar, puede agregar o quitar usuarios y entidades de servicio del grupo de seguridad de Azure AD adecuado. 

Hay muchas maneras diferentes de configurar grupos. Por ejemplo, Imagine que tiene un directorio denominado **/LogData** que contiene los datos de registro generados por su servidor. Azure Data Factory (ADF) ingiere los datos en esa carpeta. Usuarios concretos del equipo de ingeniería de servicios cargarán los registros y administrarán a otros usuarios de esta carpeta y varios clústeres de Databricks de archivos analizarán los registros de esa carpeta. 

Para habilitar estas actividades, puede crear un grupo `LogsWriter` y un grupo `LogsReader`. Luego, puede asignar permisos como se indica a continuación:

- Agregue el grupo `LogsWriter` a la lista de control de acceso del directorio **/LogData** con permisos de `rwx`.
- Agregue el grupo `LogsReader` a la lista de control de acceso del directorio **/LogData** con permisos de `r-x`.
- Agregue el objeto de entidad de servicio o Managed Service Identity (MSI) para ADF al grupo `LogsWriters`.
- Agregue los usuarios del equipo de ingeniería de servicios al grupo `LogsWriter`.
- Agregue el objeto de entidad de servicio o MSI para Databricks al grupo `LogsReader`.

Si un usuario del equipo de ingeniería de servicios deja la empresa, puede quitarle del grupo `LogsWriter`. Si no agregó dicho usuario a un grupo, sino que en su lugar agregó una entrada de ACL dedicada para ese usuario, tendrá que quitar esa entrada del directorio **/LogData** . También tendría que quitar la entrada de todos los subdirectorios y archivos de toda la jerarquía de directorios del directorio **/LogData** . 

Para más información, consulte [Creación de un grupo básico e incorporación de miembros con Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).