---
title: Aprendizaje de Machine Learning acelerado por GPU en el subsistema de Windows para Linux
description: Obtenga más información sobre la compatibilidad con WSL 2 para NVIDIA CUDA, DirectML, Tensorflow y PyTorch.
keywords: WSL, Windows, subsistema de Windows, proceso de GPU, aceleración de GPU, NVIDIA, CUDA, DirectML, Tensorflow, PyTorch, NVIDIA CUDA Preview, controlador de GPU, NVIDIA Container Toolkit, Docker
ms.date: 06/17/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: f101022dec534055905b25619a6c4fcee36f3f7d
ms.sourcegitcommit: 031a74801e03a90aed4b34c4fd5bfe964fc30994
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "84947419"
---
# <a name="gpu-accelerated-machine-learning-training-in-the-windows-subsystem-for-linux"></a>Entrenamiento de aprendizaje automático acelerado por GPU en el subsistema de Windows para Linux

La compatibilidad con el proceso de GPU, la #1 la característica de WSL más solicitada, ahora está disponible para la versión preliminar a través del programa Windows Insider. [Leer la entrada de blog](https://blogs.windows.com/windowsdeveloper/?p=55781).

## <a name="what-is-gpu-compute"></a>¿Qué es el proceso de GPU?

En general, el uso de la aceleración de GPU para las tareas de proceso intensivo se conoce como "proceso de GPU". La informática de GPU aprovecha la GPU (unidad de procesamiento de gráficos) para acelerar las cargas de trabajo pesadas matemáticas y utiliza su procesamiento en paralelo para completar los cálculos necesarios más rápido, en muchos casos, que usar solo una CPU. Esta paralelización permite mejorar significativamente la velocidad de procesamiento de estas cargas de trabajo pesadas matemáticas cuando se ejecuta en una CPU. El entrenamiento de los modelos de aprendizaje automático es un buen ejemplo en el que el proceso de GPU puede acelerar considerablemente el tiempo para completar esta tarea costosa.

## <a name="install-and-set-up"></a>Instalación y configuración

Obtenga más información sobre la compatibilidad con WSL 2 y cómo empezar a entrenar modelos de aprendizaje automático en la [Guía de aprendizaje acelerado de GPU](https://docs.microsoft.com/windows/win32/direct3d12/gpu-accelerated-training) dentro de los documentos de DirectML. En esta guía se trata:

* Instrucciones para principiantes o estudiantes para configurar TensorFlow con DirectML
* Instrucciones para que los profesionales empiecen a ejecutar sus flujos de trabajo de CUDA ML existentes
