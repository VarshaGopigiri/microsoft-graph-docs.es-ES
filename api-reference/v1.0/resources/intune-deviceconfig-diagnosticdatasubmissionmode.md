---
title: tipo de enumeración diagnosticDataSubmissionMode
description: Permitir que el dispositivo enviar datos de telemetría de diagnóstico y uso, como Watson.
ms.openlocfilehash: b09a4bf334af5981c3ce6dabbab0ac64e2b24887
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031658"
---
# <a name="diagnosticdatasubmissionmode-enum-type"></a><span data-ttu-id="cd930-103">tipo de enumeración diagnosticDataSubmissionMode</span><span class="sxs-lookup"><span data-stu-id="cd930-103">diagnosticDataSubmissionMode enum type</span></span>

> <span data-ttu-id="cd930-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cd930-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cd930-105">Permitir que el dispositivo enviar datos de telemetría de diagnóstico y uso, como Watson.</span><span class="sxs-lookup"><span data-stu-id="cd930-105">Allow the device to send diagnostic and usage telemetry data, such as Watson.</span></span>
## <a name="members"></a><span data-ttu-id="cd930-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="cd930-106">Members</span></span>
|<span data-ttu-id="cd930-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="cd930-107">Member</span></span>|<span data-ttu-id="cd930-108">Valor</span><span class="sxs-lookup"><span data-stu-id="cd930-108">Value</span></span>|<span data-ttu-id="cd930-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd930-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cd930-110">userDefined</span><span class="sxs-lookup"><span data-stu-id="cd930-110">userDefined</span></span>|<span data-ttu-id="cd930-111">0</span><span class="sxs-lookup"><span data-stu-id="cd930-111">0</span></span>|<span data-ttu-id="cd930-112">Permitir al usuario que establezca.</span><span class="sxs-lookup"><span data-stu-id="cd930-112">Allow the user to set.</span></span>|
|<span data-ttu-id="cd930-113">ninguno</span><span class="sxs-lookup"><span data-stu-id="cd930-113">none</span></span>|<span data-ttu-id="cd930-114">1</span><span class="sxs-lookup"><span data-stu-id="cd930-114">1</span></span>|<span data-ttu-id="cd930-115">No hay datos de telemetría se envían desde los componentes del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cd930-115">No telemetry data is sent from OS components.</span></span> <span data-ttu-id="cd930-116">Nota: Este valor solo es aplicable a dispositivos de servidor y de la empresa.</span><span class="sxs-lookup"><span data-stu-id="cd930-116">Note: This value is only applicable to enterprise and server devices.</span></span> <span data-ttu-id="cd930-117">El uso de esta configuración en otros dispositivos equivale a establecer el valor de 1.</span><span class="sxs-lookup"><span data-stu-id="cd930-117">Using this setting on other devices is equivalent to setting the value of 1.</span></span>|
|<span data-ttu-id="cd930-118">básica</span><span class="sxs-lookup"><span data-stu-id="cd930-118">basic</span></span>|<span data-ttu-id="cd930-119">2</span><span class="sxs-lookup"><span data-stu-id="cd930-119">2</span></span>|<span data-ttu-id="cd930-120">Envía los datos de telemetría básica.</span><span class="sxs-lookup"><span data-stu-id="cd930-120">Sends basic telemetry data.</span></span>|
|<span data-ttu-id="cd930-121">mejorado</span><span class="sxs-lookup"><span data-stu-id="cd930-121">enhanced</span></span>|<span data-ttu-id="cd930-122">3</span><span class="sxs-lookup"><span data-stu-id="cd930-122">3</span></span>|<span data-ttu-id="cd930-123">Envía mejoradas, incluidos los datos de uso y entendimiento de los datos de telemetría.</span><span class="sxs-lookup"><span data-stu-id="cd930-123">Sends enhanced telemetry data including usage and insights data.</span></span>|
|<span data-ttu-id="cd930-124">completa</span><span class="sxs-lookup"><span data-stu-id="cd930-124">full</span></span>|<span data-ttu-id="cd930-125">4</span><span class="sxs-lookup"><span data-stu-id="cd930-125">4</span></span>|<span data-ttu-id="cd930-126">Envía datos de telemetría completa, incluidos los datos de diagnósticos, como estado del sistema.</span><span class="sxs-lookup"><span data-stu-id="cd930-126">Sends full telemetry data including diagnostic data, such as system state.</span></span>|



