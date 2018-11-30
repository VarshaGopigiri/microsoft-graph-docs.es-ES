---
title: tipo de enumeración folderProtectionType
description: Valores posibles de protección de carpeta
ms.openlocfilehash: a02f1602f8b9a962124fb7bf2a9731662a6f3057
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086022"
---
# <a name="folderprotectiontype-enum-type"></a><span data-ttu-id="46cc5-103">tipo de enumeración folderProtectionType</span><span class="sxs-lookup"><span data-stu-id="46cc5-103">folderProtectionType enum type</span></span>

> <span data-ttu-id="46cc5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="46cc5-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="46cc5-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="46cc5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="46cc5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="46cc5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="46cc5-107">Valores posibles de protección de carpeta</span><span class="sxs-lookup"><span data-stu-id="46cc5-107">Possible values of Folder Protection</span></span>
## <a name="members"></a><span data-ttu-id="46cc5-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="46cc5-108">Members</span></span>
|<span data-ttu-id="46cc5-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="46cc5-109">Member</span></span>|<span data-ttu-id="46cc5-110">Valor</span><span class="sxs-lookup"><span data-stu-id="46cc5-110">Value</span></span>|<span data-ttu-id="46cc5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="46cc5-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="46cc5-112">userDefined</span><span class="sxs-lookup"><span data-stu-id="46cc5-112">userDefined</span></span>|<span data-ttu-id="46cc5-113">0</span><span class="sxs-lookup"><span data-stu-id="46cc5-113">0</span></span>|<span data-ttu-id="46cc5-114">Valor predeterminado de dispositivo, sin intención.</span><span class="sxs-lookup"><span data-stu-id="46cc5-114">Device default value, no intent.</span></span>|
|<span data-ttu-id="46cc5-115">habilitar</span><span class="sxs-lookup"><span data-stu-id="46cc5-115">enable</span></span>|<span data-ttu-id="46cc5-116">1</span><span class="sxs-lookup"><span data-stu-id="46cc5-116">1</span></span>|<span data-ttu-id="46cc5-117">Funcionalidad de bloque.</span><span class="sxs-lookup"><span data-stu-id="46cc5-117">Block functionality.</span></span>|
|<span data-ttu-id="46cc5-118">auditMode</span><span class="sxs-lookup"><span data-stu-id="46cc5-118">auditMode</span></span>|<span data-ttu-id="46cc5-119">2</span><span class="sxs-lookup"><span data-stu-id="46cc5-119">2</span></span>|<span data-ttu-id="46cc5-120">Permitir la funcionalidad pero los registros que se genere.</span><span class="sxs-lookup"><span data-stu-id="46cc5-120">Allow functionality but generate logs.</span></span>|
|<span data-ttu-id="46cc5-121">blockDiskModification</span><span class="sxs-lookup"><span data-stu-id="46cc5-121">blockDiskModification</span></span>|<span data-ttu-id="46cc5-122">3</span><span class="sxs-lookup"><span data-stu-id="46cc5-122">3</span></span>|<span data-ttu-id="46cc5-123">Bloquear las aplicaciones que no se confía escribir en sectores de disco.</span><span class="sxs-lookup"><span data-stu-id="46cc5-123">Block untrusted apps from writing to disk sectors.</span></span>|
|<span data-ttu-id="46cc5-124">auditDiskModification</span><span class="sxs-lookup"><span data-stu-id="46cc5-124">auditDiskModification</span></span>|<span data-ttu-id="46cc5-125">4</span><span class="sxs-lookup"><span data-stu-id="46cc5-125">4</span></span>|<span data-ttu-id="46cc5-126">Generar registros al escriben aplicaciones que no se confía a sectores de disco.</span><span class="sxs-lookup"><span data-stu-id="46cc5-126">Generate logs when untrusted apps write to disk sectors.</span></span>|





