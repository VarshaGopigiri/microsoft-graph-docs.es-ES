---
title: tipo de enumeración diagnosticDataSubmissionMode
description: Permitir que el dispositivo enviar datos de telemetría de diagnóstico y uso, como Watson.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: a293288c3891f8ecd77d422986e419d2e3d53767
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912949"
---
# <a name="diagnosticdatasubmissionmode-enum-type"></a><span data-ttu-id="ab52f-103">tipo de enumeración diagnosticDataSubmissionMode</span><span class="sxs-lookup"><span data-stu-id="ab52f-103">diagnosticDataSubmissionMode enum type</span></span>

> <span data-ttu-id="ab52f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ab52f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ab52f-105">Permitir que el dispositivo enviar datos de telemetría de diagnóstico y uso, como Watson.</span><span class="sxs-lookup"><span data-stu-id="ab52f-105">Allow the device to send diagnostic and usage telemetry data, such as Watson.</span></span>
## <a name="members"></a><span data-ttu-id="ab52f-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ab52f-106">Members</span></span>
|<span data-ttu-id="ab52f-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="ab52f-107">Member</span></span>|<span data-ttu-id="ab52f-108">Valor</span><span class="sxs-lookup"><span data-stu-id="ab52f-108">Value</span></span>|<span data-ttu-id="ab52f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab52f-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ab52f-110">userDefined</span><span class="sxs-lookup"><span data-stu-id="ab52f-110">userDefined</span></span>|<span data-ttu-id="ab52f-111">0</span><span class="sxs-lookup"><span data-stu-id="ab52f-111">0</span></span>|<span data-ttu-id="ab52f-112">Permitir al usuario que establezca.</span><span class="sxs-lookup"><span data-stu-id="ab52f-112">Allow the user to set.</span></span>|
|<span data-ttu-id="ab52f-113">none</span><span class="sxs-lookup"><span data-stu-id="ab52f-113">none</span></span>|<span data-ttu-id="ab52f-114">1</span><span class="sxs-lookup"><span data-stu-id="ab52f-114">1</span></span>|<span data-ttu-id="ab52f-115">No hay datos de telemetría se envían desde los componentes del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ab52f-115">No telemetry data is sent from OS components.</span></span> <span data-ttu-id="ab52f-116">Nota: Este valor solo es aplicable a dispositivos de servidor y de la empresa.</span><span class="sxs-lookup"><span data-stu-id="ab52f-116">Note: This value is only applicable to enterprise and server devices.</span></span> <span data-ttu-id="ab52f-117">El uso de esta configuración en otros dispositivos equivale a establecer el valor de 1.</span><span class="sxs-lookup"><span data-stu-id="ab52f-117">Using this setting on other devices is equivalent to setting the value of 1.</span></span>|
|<span data-ttu-id="ab52f-118">básica</span><span class="sxs-lookup"><span data-stu-id="ab52f-118">basic</span></span>|<span data-ttu-id="ab52f-119">2</span><span class="sxs-lookup"><span data-stu-id="ab52f-119">2</span></span>|<span data-ttu-id="ab52f-120">Envía los datos de telemetría básica.</span><span class="sxs-lookup"><span data-stu-id="ab52f-120">Sends basic telemetry data.</span></span>|
|<span data-ttu-id="ab52f-121">mejorado</span><span class="sxs-lookup"><span data-stu-id="ab52f-121">enhanced</span></span>|<span data-ttu-id="ab52f-122">3</span><span class="sxs-lookup"><span data-stu-id="ab52f-122">3</span></span>|<span data-ttu-id="ab52f-123">Envía mejoradas, incluidos los datos de uso y entendimiento de los datos de telemetría.</span><span class="sxs-lookup"><span data-stu-id="ab52f-123">Sends enhanced telemetry data including usage and insights data.</span></span>|
|<span data-ttu-id="ab52f-124">completa</span><span class="sxs-lookup"><span data-stu-id="ab52f-124">full</span></span>|<span data-ttu-id="ab52f-125">4</span><span class="sxs-lookup"><span data-stu-id="ab52f-125">4</span></span>|<span data-ttu-id="ab52f-126">Envía datos de telemetría completa, incluidos los datos de diagnósticos, como estado del sistema.</span><span class="sxs-lookup"><span data-stu-id="ab52f-126">Sends full telemetry data including diagnostic data, such as system state.</span></span>|



