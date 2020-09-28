---
title: Aprendizaje de Machine Learning acelerado por GPU en el subsistema de Windows para Linux
description: Obtenga más información sobre la compatibilidad con WSL 2 para NVIDIA CUDA, DirectML, Tensorflow y PyTorch.
keywords: WSL, Windows, subsistema de Windows, proceso de GPU, aceleración de GPU, NVIDIA, CUDA, DirectML, Tensorflow, PyTorch, NVIDIA CUDA Preview, controlador de GPU, NVIDIA Container Toolkit, Docker
ms.date: 06/17/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: bc20f2d3f1da646ba01dcdc00de8eca6c3825ec8
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413316"
---
# <a name="gpu-accelerated-machine-learning-training-in-the-windows-subsystem-for-linux"></a>Entrenamiento de aprendizaje automático acelerado por GPU en el subsistema de Windows para Linux

La compatibilidad con el proceso de GPU, la #1 la característica de WSL más solicitada, ahora está disponible para la versión preliminar a través del programa Windows Insider. [Leer la entrada de blog](https://blogs.windows.com/windowsdeveloper/?p=55781).

## <a name="what-is-gpu-compute"></a>¿Qué es el proceso de GPU?

En general, el uso de la aceleración de GPU para las tareas de proceso intensivo se conoce como "proceso de GPU". La informática de GPU aprovecha la GPU (unidad de procesamiento de gráficos) para acelerar las cargas de trabajo pesadas matemáticas y utiliza su procesamiento en paralelo para completar los cálculos necesarios más rápido, en muchos casos, que usar solo una CPU. Esta paralelización permite mejorar significativamente la velocidad de procesamiento de estas cargas de trabajo pesadas matemáticas cuando se ejecuta en una CPU. El entrenamiento de los modelos de aprendizaje automático es un buen ejemplo en el que el proceso de GPU puede acelerar considerablemente el tiempo para completar esta tarea costosa.

## <a name="install-and-set-up"></a>Instalación y configuración

Obtenga más información sobre la compatibilidad con WSL 2 y cómo empezar a entrenar modelos de aprendizaje automático en la [Guía de aprendizaje acelerado de GPU](/windows/win32/direct3d12/gpu-accelerated-training) dentro de los documentos de DirectML. En esta guía se trata:

* Instrucciones para principiantes o estudiantes para configurar TensorFlow con DirectML
* Instrucciones para que los profesionales empiecen a ejecutar sus flujos de trabajo de CUDA ML existentes