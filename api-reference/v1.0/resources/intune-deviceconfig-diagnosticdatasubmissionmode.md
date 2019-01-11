---
title: tipo de enumeración diagnosticDataSubmissionMode
description: Permitir que el dispositivo enviar datos de telemetría de diagnóstico y uso, como Watson.
localization_priority: Normal
ms.openlocfilehash: 1654e9c5c94fd79bbda0d77ef84101fb9fb92d5c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27812785"
---
# <a name="diagnosticdatasubmissionmode-enum-type"></a><span data-ttu-id="0cb52-103">tipo de enumeración diagnosticDataSubmissionMode</span><span class="sxs-lookup"><span data-stu-id="0cb52-103">diagnosticDataSubmissionMode enum type</span></span>

> <span data-ttu-id="0cb52-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0cb52-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0cb52-105">Permitir que el dispositivo enviar datos de telemetría de diagnóstico y uso, como Watson.</span><span class="sxs-lookup"><span data-stu-id="0cb52-105">Allow the device to send diagnostic and usage telemetry data, such as Watson.</span></span>
## <a name="members"></a><span data-ttu-id="0cb52-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="0cb52-106">Members</span></span>
|<span data-ttu-id="0cb52-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="0cb52-107">Member</span></span>|<span data-ttu-id="0cb52-108">Valor</span><span class="sxs-lookup"><span data-stu-id="0cb52-108">Value</span></span>|<span data-ttu-id="0cb52-109">Description</span><span class="sxs-lookup"><span data-stu-id="0cb52-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0cb52-110">userDefined</span><span class="sxs-lookup"><span data-stu-id="0cb52-110">userDefined</span></span>|<span data-ttu-id="0cb52-111">0</span><span class="sxs-lookup"><span data-stu-id="0cb52-111">0</span></span>|<span data-ttu-id="0cb52-112">Permitir al usuario que establezca.</span><span class="sxs-lookup"><span data-stu-id="0cb52-112">Allow the user to set.</span></span>|
|<span data-ttu-id="0cb52-113">none</span><span class="sxs-lookup"><span data-stu-id="0cb52-113">none</span></span>|<span data-ttu-id="0cb52-114">1</span><span class="sxs-lookup"><span data-stu-id="0cb52-114">1</span></span>|<span data-ttu-id="0cb52-115">No hay datos de telemetría se envían desde los componentes del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0cb52-115">No telemetry data is sent from OS components.</span></span> <span data-ttu-id="0cb52-116">Nota: Este valor solo es aplicable a dispositivos de servidor y de la empresa.</span><span class="sxs-lookup"><span data-stu-id="0cb52-116">Note: This value is only applicable to enterprise and server devices.</span></span> <span data-ttu-id="0cb52-117">El uso de esta configuración en otros dispositivos equivale a establecer el valor de 1.</span><span class="sxs-lookup"><span data-stu-id="0cb52-117">Using this setting on other devices is equivalent to setting the value of 1.</span></span>|
|<span data-ttu-id="0cb52-118">básica</span><span class="sxs-lookup"><span data-stu-id="0cb52-118">basic</span></span>|<span data-ttu-id="0cb52-119">2</span><span class="sxs-lookup"><span data-stu-id="0cb52-119">2</span></span>|<span data-ttu-id="0cb52-120">Envía los datos de telemetría básica.</span><span class="sxs-lookup"><span data-stu-id="0cb52-120">Sends basic telemetry data.</span></span>|
|<span data-ttu-id="0cb52-121">mejorado</span><span class="sxs-lookup"><span data-stu-id="0cb52-121">enhanced</span></span>|<span data-ttu-id="0cb52-122">3</span><span class="sxs-lookup"><span data-stu-id="0cb52-122">3</span></span>|<span data-ttu-id="0cb52-123">Envía mejoradas, incluidos los datos de uso y entendimiento de los datos de telemetría.</span><span class="sxs-lookup"><span data-stu-id="0cb52-123">Sends enhanced telemetry data including usage and insights data.</span></span>|
|<span data-ttu-id="0cb52-124">completa</span><span class="sxs-lookup"><span data-stu-id="0cb52-124">full</span></span>|<span data-ttu-id="0cb52-125">4</span><span class="sxs-lookup"><span data-stu-id="0cb52-125">4</span></span>|<span data-ttu-id="0cb52-126">Envía datos de telemetría completa, incluidos los datos de diagnósticos, como estado del sistema.</span><span class="sxs-lookup"><span data-stu-id="0cb52-126">Sends full telemetry data including diagnostic data, such as system state.</span></span>|



