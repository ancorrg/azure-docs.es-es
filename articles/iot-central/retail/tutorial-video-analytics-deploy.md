---
title: Implementación de la plantilla de la aplicación Video analytics - object and motion detection de Azure IoT Central
description: En esta guía se resumen los pasos necesarios para implementar una aplicación de Azure IoT Central mediante la plantilla de la aplicación Video analytics - object and motion detection.
services: iot-central
ms.service: iot-central
ms.subservice: iot-central-retail
ms.topic: how-to
ms.author: nandab
author: KishorIoT
ms.date: 07/31/2020
ms.openlocfilehash: decfa7020be7778e8ca64a9fb0cb4aac1657da27
ms.sourcegitcommit: fbb620e0c47f49a8cf0a568ba704edefd0e30f81
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2020
ms.locfileid: "91873343"
---
# <a name="how-to-deploy-an-iot-central-application-using-the-video-analytics---object-and-motion-detection-application-template"></a>Implementación de una aplicación de IoT Central mediante la plantilla de la aplicación Video analytics - object and motion detection

Para información general sobre los componentes de la aplicación clave *Video analytics - object and motion detection*, consulte [Arquitectura de la aplicación Video analytics - object and motion detection](architecture-video-analytics.md).

En el siguiente vídeo se ofrece un tutorial sobre cómo usar la _plantilla de aplicación de análisis de vídeo y detección de movimiento y objetos_ para implementar una solución IoT Central:

> [!VIDEO https://www.youtube.com/embed/Bo3FziU9bSA]

## <a name="deploy-the-application"></a>Implementación de la aplicación

Para implementar una aplicación de IoT Central mediante la plantilla de análisis de vídeo, complete los pasos siguientes:

1. Complete el tutorial [Creación de una aplicación de análisis de vídeo en Azure IoT Central (YOLO v3)](tutorial-video-analytics-create-app-yolo-v3.md) o [Creación de un análisis de vídeo en Azure IoT Central (OpenVINO&trade;)](tutorial-video-analytics-create-app-openvino.md) para:
    - Creación de una cuenta de Azure Media Services.
    - Crear la aplicación de IoT Central a partir de la plantilla de la aplicación Video analytics - object and motion detection.
    - Configurar un dispositivo de puerta de enlace a la aplicación de IoT Central. La puerta de enlace permite que los dispositivos de cámara se conecten a la aplicación.

1. Complete el tutorial [Creación de una instancia de IoT Edge para análisis de vídeo (máquina virtual Linux)](tutorial-video-analytics-iot-edge-vm.md) o [: Creación de una instancia de IoT Edge para análisis de vídeo (Intel NUC)](tutorial-video-analytics-iot-edge-nuc.md) para:
    - Crear una máquina virtual de Azure con el entorno de ejecución de Azure IoT Edge instalado. Prepare la instalación de IoT Edge para hospedar el módulo de análisis de vídeo.
    - Conecte el dispositivo de IoT Edge a la aplicación de IoT Central.

1. Complete el tutorial [Supervisión y administración de una aplicación de análisis de vídeo](tutorial-video-analytics-manage.md) para:
    - Agregar cámaras de detección de objetos y movimiento a la puerta de enlace de la aplicación de IoT Central.
    - Iniciar el procesamiento de la cámara.
    - Instalar un reproductor multimedia local para ver el vídeo capturado en AMS.
    - Ver el vídeo capturado que muestra los objetos detectados.
    - Ordenar.

## <a name="next-steps"></a>Pasos siguientes

Ahora tiene una visión general de los pasos necesarios para implementar y usar la plantilla para aplicaciones de análisis de vídeo, consulte [Creación de una aplicación de análisis de vídeo en Azure IoT Central (YOLO v3)](tutorial-video-analytics-create-app-yolo-v3.md) o [Creación de un análisis de vídeo en Azure IoT Central (OpenVINO&trade;)](tutorial-video-analytics-create-app-openvino.md) para comenzar.
