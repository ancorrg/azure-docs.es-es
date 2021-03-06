---
title: Comparación del rendimiento de la aplicación en Azure Disk Storage
description: Obtenga información sobre el proceso de comparación de la aplicación en Azure.
author: roygara
ms.author: rogarana
ms.date: 01/11/2019
ms.topic: how-to
ms.service: virtual-machines-windows
ms.subservice: disks
ms.openlocfilehash: d8bf90f4ecea992b3212200905cd9204e4079b1b
ms.sourcegitcommit: 829d951d5c90442a38012daaf77e86046018e5b9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2020
ms.locfileid: "88683970"
---
# <a name="benchmarking-a-disk"></a>Pruebas comparativas de un disco

Las pruebas comparativas consisten en el proceso de simular cargas de trabajo diferentes en la aplicación y medir el rendimiento de las aplicaciones para cada carga de trabajo. Mediante los pasos descritos en el artículo sobre el [diseño con alto rendimiento](../premium-storage-performance.md), recopiló los requisitos de rendimiento de las aplicaciones. Al ejecutar las herramientas de pruebas comparativas en las máquinas virtuales en las que se hospeda la aplicación, puede determinar los niveles de rendimiento que la aplicación puede lograr con Premium Storage. En este artículo, se proporcionan ejemplos de pruebas comparativas realizadas con una máquina virtual estándar DS14 aprovisionada con discos de Azure Premium Storage.

Hemos usado las herramientas de pruebas comparativas comunes Iometer y FIO, para Windows y Linux respectivamente. Estas herramientas generan varios subprocesos que simulan una carga de trabajo de producción y miden el rendimiento del sistema. Con estas herramientas, también puede configurar parámetros como la profundidad de la cola y el tamaño de bloque, que normalmente no se puede cambiar de una aplicación. Esto proporciona más flexibilidad para controlar el rendimiento máximo en una máquina virtual a gran escala aprovisionada con discos premium para diferentes tipos de cargas de trabajo de la aplicación. Para más información sobre la herramienta de pruebas comparativas, visite [Iometer](http://www.iometer.org/) y [FIO](http://freecode.com/projects/fio).

Para seguir estos ejemplos, cree una máquina virtual estándar DS14 y conecte 11 discos de Premium Storage a la máquina virtual. De los once discos, configure diez con almacenamiento en caché de host como "None" y secciónelos en un volumen denominado NoCacheWrites. Configure el almacenamiento en caché de host como "ReadOnly" en el disco restante y cree un volumen denominado CacheReads con dicho disco. Con esta configuración, puede ver el rendimiento máximo de lectura y escritura de una máquina virtual estándar DS14. Para obtener instrucciones detalladas sobre cómo crear una máquina virtual DS14 con SSD Premium, consulte [Azure Premium Storage: Diseño de alto rendimiento](../premium-storage-performance.md).

[!INCLUDE [virtual-machines-disks-benchmarking](../../../includes/virtual-machines-managed-disks-benchmarking.md)]

## <a name="next-steps"></a>Pasos siguientes

Diríjase al artículo sobre el [diseño para lograr un alto rendimiento](../premium-storage-performance.md).

En dicho artículo, se crea una lista de comprobación similar a la aplicación existente para el prototipo. Con herramientas de pruebas comparativas puede simular las cargas de trabajo y medir el rendimiento de las aplicaciones de prototipo. De este modo, puede determinar qué oferta de disco puede alcanzar o superar los requisitos de rendimiento de las aplicaciones. A continuación, puede implementar las mismas directrices para la aplicación de producción.