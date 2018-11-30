---
title: tipo de enumeración diagnosticDataSubmissionMode
description: Permitir que el dispositivo enviar datos de telemetría de diagnóstico y uso, como Watson.
ms.openlocfilehash: 9cdc76691df0a7a9492524d02c338ee2a42106e3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083972"
---
# <a name="diagnosticdatasubmissionmode-enum-type"></a><span data-ttu-id="dfbea-103">tipo de enumeración diagnosticDataSubmissionMode</span><span class="sxs-lookup"><span data-stu-id="dfbea-103">diagnosticDataSubmissionMode enum type</span></span>

> <span data-ttu-id="dfbea-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dfbea-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dfbea-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dfbea-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="dfbea-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="dfbea-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="dfbea-107">Permitir que el dispositivo enviar datos de telemetría de diagnóstico y uso, como Watson.</span><span class="sxs-lookup"><span data-stu-id="dfbea-107">Allow the device to send diagnostic and usage telemetry data, such as Watson.</span></span>
## <a name="members"></a><span data-ttu-id="dfbea-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="dfbea-108">Members</span></span>
|<span data-ttu-id="dfbea-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="dfbea-109">Member</span></span>|<span data-ttu-id="dfbea-110">Valor</span><span class="sxs-lookup"><span data-stu-id="dfbea-110">Value</span></span>|<span data-ttu-id="dfbea-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfbea-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="dfbea-112">userDefined</span><span class="sxs-lookup"><span data-stu-id="dfbea-112">userDefined</span></span>|<span data-ttu-id="dfbea-113">0</span><span class="sxs-lookup"><span data-stu-id="dfbea-113">0</span></span>|<span data-ttu-id="dfbea-114">Permitir al usuario que establezca.</span><span class="sxs-lookup"><span data-stu-id="dfbea-114">Allow the user to set.</span></span>|
|<span data-ttu-id="dfbea-115">ninguno</span><span class="sxs-lookup"><span data-stu-id="dfbea-115">none</span></span>|<span data-ttu-id="dfbea-116">1</span><span class="sxs-lookup"><span data-stu-id="dfbea-116">1</span></span>|<span data-ttu-id="dfbea-117">No hay datos de telemetría se envían desde los componentes del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dfbea-117">No telemetry data is sent from OS components.</span></span> <span data-ttu-id="dfbea-118">Nota: Este valor solo es aplicable a dispositivos de servidor y de la empresa.</span><span class="sxs-lookup"><span data-stu-id="dfbea-118">Note: This value is only applicable to enterprise and server devices.</span></span> <span data-ttu-id="dfbea-119">El uso de esta configuración en otros dispositivos equivale a establecer el valor de 1.</span><span class="sxs-lookup"><span data-stu-id="dfbea-119">Using this setting on other devices is equivalent to setting the value of 1.</span></span>|
|<span data-ttu-id="dfbea-120">básica</span><span class="sxs-lookup"><span data-stu-id="dfbea-120">basic</span></span>|<span data-ttu-id="dfbea-121">2</span><span class="sxs-lookup"><span data-stu-id="dfbea-121">2</span></span>|<span data-ttu-id="dfbea-122">Envía los datos de telemetría básica.</span><span class="sxs-lookup"><span data-stu-id="dfbea-122">Sends basic telemetry data.</span></span>|
|<span data-ttu-id="dfbea-123">mejorado</span><span class="sxs-lookup"><span data-stu-id="dfbea-123">enhanced</span></span>|<span data-ttu-id="dfbea-124">3</span><span class="sxs-lookup"><span data-stu-id="dfbea-124">3</span></span>|<span data-ttu-id="dfbea-125">Envía mejoradas, incluidos los datos de uso y entendimiento de los datos de telemetría.</span><span class="sxs-lookup"><span data-stu-id="dfbea-125">Sends enhanced telemetry data including usage and insights data.</span></span>|
|<span data-ttu-id="dfbea-126">completa</span><span class="sxs-lookup"><span data-stu-id="dfbea-126">full</span></span>|<span data-ttu-id="dfbea-127">4</span><span class="sxs-lookup"><span data-stu-id="dfbea-127">4</span></span>|<span data-ttu-id="dfbea-128">Envía datos de telemetría completa, incluidos los datos de diagnósticos, como estado del sistema.</span><span class="sxs-lookup"><span data-stu-id="dfbea-128">Sends full telemetry data including diagnostic data, such as system state.</span></span>|





