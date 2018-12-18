---
title: tipo de enumeración runState
description: Indica el tipo de estado de ejecución de la secuencia de comandos de administración de dispositivos.
author: tfitzmac
ms.openlocfilehash: 87c845c02bd5a1571ab2f6382acbcc92cf81170d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27349276"
---
# <a name="runstate-enum-type"></a><span data-ttu-id="aed00-103">tipo de enumeración runState</span><span class="sxs-lookup"><span data-stu-id="aed00-103">runState enum type</span></span>

> <span data-ttu-id="aed00-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="aed00-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="aed00-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="aed00-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="aed00-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="aed00-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="aed00-107">Indica el tipo de estado de ejecución de la secuencia de comandos de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="aed00-107">Indicates the type of execution status of the device management script.</span></span>
## <a name="members"></a><span data-ttu-id="aed00-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="aed00-108">Members</span></span>
|<span data-ttu-id="aed00-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="aed00-109">Member</span></span>|<span data-ttu-id="aed00-110">Valor</span><span class="sxs-lookup"><span data-stu-id="aed00-110">Value</span></span>|<span data-ttu-id="aed00-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="aed00-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="aed00-112">desconocido</span><span class="sxs-lookup"><span data-stu-id="aed00-112">unknown</span></span>|<span data-ttu-id="aed00-113">0</span><span class="sxs-lookup"><span data-stu-id="aed00-113">0</span></span>|<span data-ttu-id="aed00-114">Resultado desconocido.</span><span class="sxs-lookup"><span data-stu-id="aed00-114">Unknown result.</span></span>|
|<span data-ttu-id="aed00-115">correcto</span><span class="sxs-lookup"><span data-stu-id="aed00-115">success</span></span>|<span data-ttu-id="aed00-116">1</span><span class="sxs-lookup"><span data-stu-id="aed00-116">1</span></span>|<span data-ttu-id="aed00-117">Secuencia de comandos se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="aed00-117">Script is run successfully.</span></span>|
|<span data-ttu-id="aed00-118">conmutación por error</span><span class="sxs-lookup"><span data-stu-id="aed00-118">fail</span></span>|<span data-ttu-id="aed00-119">2</span><span class="sxs-lookup"><span data-stu-id="aed00-119">2</span></span>|<span data-ttu-id="aed00-120">No se pudo ejecutar el script.</span><span class="sxs-lookup"><span data-stu-id="aed00-120">Script failed to run.</span></span>|





