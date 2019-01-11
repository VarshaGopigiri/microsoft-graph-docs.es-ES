---
title: tipo de enumeración diagnosticDataSubmissionMode
description: Permitir que el dispositivo enviar datos de telemetría de diagnóstico y uso, como Watson.
localization_priority: Normal
ms.openlocfilehash: 3be69b4be25ece2ced611c028a855347e4dba66e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871536"
---
# <a name="diagnosticdatasubmissionmode-enum-type"></a><span data-ttu-id="09c95-103">tipo de enumeración diagnosticDataSubmissionMode</span><span class="sxs-lookup"><span data-stu-id="09c95-103">diagnosticDataSubmissionMode enum type</span></span>

> <span data-ttu-id="09c95-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="09c95-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="09c95-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="09c95-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="09c95-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="09c95-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="09c95-107">Permitir que el dispositivo enviar datos de telemetría de diagnóstico y uso, como Watson.</span><span class="sxs-lookup"><span data-stu-id="09c95-107">Allow the device to send diagnostic and usage telemetry data, such as Watson.</span></span>
## <a name="members"></a><span data-ttu-id="09c95-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="09c95-108">Members</span></span>
|<span data-ttu-id="09c95-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="09c95-109">Member</span></span>|<span data-ttu-id="09c95-110">Valor</span><span class="sxs-lookup"><span data-stu-id="09c95-110">Value</span></span>|<span data-ttu-id="09c95-111">Description</span><span class="sxs-lookup"><span data-stu-id="09c95-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="09c95-112">userDefined</span><span class="sxs-lookup"><span data-stu-id="09c95-112">userDefined</span></span>|<span data-ttu-id="09c95-113">0</span><span class="sxs-lookup"><span data-stu-id="09c95-113">0</span></span>|<span data-ttu-id="09c95-114">Permitir al usuario que establezca.</span><span class="sxs-lookup"><span data-stu-id="09c95-114">Allow the user to set.</span></span>|
|<span data-ttu-id="09c95-115">none</span><span class="sxs-lookup"><span data-stu-id="09c95-115">none</span></span>|<span data-ttu-id="09c95-116">1</span><span class="sxs-lookup"><span data-stu-id="09c95-116">1</span></span>|<span data-ttu-id="09c95-117">No hay datos de telemetría se envían desde los componentes del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="09c95-117">No telemetry data is sent from OS components.</span></span> <span data-ttu-id="09c95-118">Nota: Este valor solo es aplicable a dispositivos de servidor y de la empresa.</span><span class="sxs-lookup"><span data-stu-id="09c95-118">Note: This value is only applicable to enterprise and server devices.</span></span> <span data-ttu-id="09c95-119">El uso de esta configuración en otros dispositivos equivale a establecer el valor de 1.</span><span class="sxs-lookup"><span data-stu-id="09c95-119">Using this setting on other devices is equivalent to setting the value of 1.</span></span>|
|<span data-ttu-id="09c95-120">básica</span><span class="sxs-lookup"><span data-stu-id="09c95-120">basic</span></span>|<span data-ttu-id="09c95-121">2</span><span class="sxs-lookup"><span data-stu-id="09c95-121">2</span></span>|<span data-ttu-id="09c95-122">Envía los datos de telemetría básica.</span><span class="sxs-lookup"><span data-stu-id="09c95-122">Sends basic telemetry data.</span></span>|
|<span data-ttu-id="09c95-123">mejorado</span><span class="sxs-lookup"><span data-stu-id="09c95-123">enhanced</span></span>|<span data-ttu-id="09c95-124">3</span><span class="sxs-lookup"><span data-stu-id="09c95-124">3</span></span>|<span data-ttu-id="09c95-125">Envía mejoradas, incluidos los datos de uso y entendimiento de los datos de telemetría.</span><span class="sxs-lookup"><span data-stu-id="09c95-125">Sends enhanced telemetry data including usage and insights data.</span></span>|
|<span data-ttu-id="09c95-126">completa</span><span class="sxs-lookup"><span data-stu-id="09c95-126">full</span></span>|<span data-ttu-id="09c95-127">4</span><span class="sxs-lookup"><span data-stu-id="09c95-127">4</span></span>|<span data-ttu-id="09c95-128">Envía datos de telemetría completa, incluidos los datos de diagnósticos, como estado del sistema.</span><span class="sxs-lookup"><span data-stu-id="09c95-128">Sends full telemetry data including diagnostic data, such as system state.</span></span>|





