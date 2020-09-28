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
# <a name="gpu-accelerated-machine-learning-training-in-the-windows-subsystem-for-linux"></a><span data-ttu-id="0a4ec-104">Entrenamiento de aprendizaje automático acelerado por GPU en el subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="0a4ec-104">GPU accelerated machine learning training in the Windows Subsystem for Linux</span></span>

<span data-ttu-id="0a4ec-105">La compatibilidad con el proceso de GPU, la #1 la característica de WSL más solicitada, ahora está disponible para la versión preliminar a través del programa Windows Insider.</span><span class="sxs-lookup"><span data-stu-id="0a4ec-105">Support for GPU compute, the #1 most requested WSL feature, is now available for preview via the Windows Insider program.</span></span> <span data-ttu-id="0a4ec-106">[Leer la entrada de blog](https://blogs.windows.com/windowsdeveloper/?p=55781).</span><span class="sxs-lookup"><span data-stu-id="0a4ec-106">[Read the blog post](https://blogs.windows.com/windowsdeveloper/?p=55781).</span></span>

## <a name="what-is-gpu-compute"></a><span data-ttu-id="0a4ec-107">¿Qué es el proceso de GPU?</span><span class="sxs-lookup"><span data-stu-id="0a4ec-107">What is GPU compute?</span></span>

<span data-ttu-id="0a4ec-108">En general, el uso de la aceleración de GPU para las tareas de proceso intensivo se conoce como "proceso de GPU".</span><span class="sxs-lookup"><span data-stu-id="0a4ec-108">Leveraging GPU acceleration for compute-intensive tasks is generally referred  to as "GPU compute".</span></span> <span data-ttu-id="0a4ec-109">La informática de GPU aprovecha la GPU (unidad de procesamiento de gráficos) para acelerar las cargas de trabajo pesadas matemáticas y utiliza su procesamiento en paralelo para completar los cálculos necesarios más rápido, en muchos casos, que usar solo una CPU.</span><span class="sxs-lookup"><span data-stu-id="0a4ec-109">GPU computing leverages the GPU (graphics processing unit) to accelerate math heavy workloads and uses its parallel processing to complete the required calculations faster, in many cases, than utilizing only a CPU.</span></span> <span data-ttu-id="0a4ec-110">Esta paralelización permite mejorar significativamente la velocidad de procesamiento de estas cargas de trabajo pesadas matemáticas cuando se ejecuta en una CPU.</span><span class="sxs-lookup"><span data-stu-id="0a4ec-110">This parallelization enables significant processing speed improvements for these math heavy workloads then when running on a CPU.</span></span> <span data-ttu-id="0a4ec-111">El entrenamiento de los modelos de aprendizaje automático es un buen ejemplo en el que el proceso de GPU puede acelerar considerablemente el tiempo para completar esta tarea costosa.</span><span class="sxs-lookup"><span data-stu-id="0a4ec-111">Training machine learning models is a great example in which GPU compute can significantly accelerate the time to complete this computationally expensive task.</span></span>

## <a name="install-and-set-up"></a><span data-ttu-id="0a4ec-112">Instalación y configuración</span><span class="sxs-lookup"><span data-stu-id="0a4ec-112">Install and set up</span></span>

<span data-ttu-id="0a4ec-113">Obtenga más información sobre la compatibilidad con WSL 2 y cómo empezar a entrenar modelos de aprendizaje automático en la [Guía de aprendizaje acelerado de GPU](/windows/win32/direct3d12/gpu-accelerated-training) dentro de los documentos de DirectML. En esta guía se trata:</span><span class="sxs-lookup"><span data-stu-id="0a4ec-113">Learn more about WSL 2 support and how to start training machine learning models in the [GPU Accelerated Training guide](/windows/win32/direct3d12/gpu-accelerated-training) inside the DirectML docs. This guide covers:</span></span>

* <span data-ttu-id="0a4ec-114">Instrucciones para principiantes o estudiantes para configurar TensorFlow con DirectML</span><span class="sxs-lookup"><span data-stu-id="0a4ec-114">Guidance for beginners or students to set up TensorFlow with DirectML</span></span>
* <span data-ttu-id="0a4ec-115">Instrucciones para que los profesionales empiecen a ejecutar sus flujos de trabajo de CUDA ML existentes</span><span class="sxs-lookup"><span data-stu-id="0a4ec-115">Guidance for professionals to start running their exisiting CUDA ML workflows</span></span>