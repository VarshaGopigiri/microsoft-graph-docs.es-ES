---
title: tipo de enumeración enrollmentState
description: Todavía no documentado
ms.openlocfilehash: 8e8e20c0fd04e4da57eddfa7384052a6ab468152
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089086"
---
# <a name="enrollmentstate-enum-type"></a><span data-ttu-id="d62dd-103">tipo de enumeración enrollmentState</span><span class="sxs-lookup"><span data-stu-id="d62dd-103">enrollmentState enum type</span></span>

> <span data-ttu-id="d62dd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d62dd-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d62dd-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d62dd-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d62dd-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d62dd-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d62dd-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="d62dd-107">Not yet documented</span></span>
## <a name="members"></a><span data-ttu-id="d62dd-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d62dd-108">Members</span></span>
|<span data-ttu-id="d62dd-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="d62dd-109">Member</span></span>|<span data-ttu-id="d62dd-110">Valor</span><span class="sxs-lookup"><span data-stu-id="d62dd-110">Value</span></span>|<span data-ttu-id="d62dd-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d62dd-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d62dd-112">desconocido</span><span class="sxs-lookup"><span data-stu-id="d62dd-112">unknown</span></span>|<span data-ttu-id="d62dd-113">0</span><span class="sxs-lookup"><span data-stu-id="d62dd-113">0</span></span>|<span data-ttu-id="d62dd-114">Se desconoce el estado de inscripción de dispositivo</span><span class="sxs-lookup"><span data-stu-id="d62dd-114">Device enrollment state is unknown</span></span>|
|<span data-ttu-id="d62dd-115">inscrito</span><span class="sxs-lookup"><span data-stu-id="d62dd-115">enrolled</span></span>|<span data-ttu-id="d62dd-116">1</span><span class="sxs-lookup"><span data-stu-id="d62dd-116">1</span></span>|<span data-ttu-id="d62dd-117">Dispositivo está inscrito.</span><span class="sxs-lookup"><span data-stu-id="d62dd-117">Device is Enrolled.</span></span>|
|<span data-ttu-id="d62dd-118">pendingReset</span><span class="sxs-lookup"><span data-stu-id="d62dd-118">pendingReset</span></span>|<span data-ttu-id="d62dd-119">2</span><span class="sxs-lookup"><span data-stu-id="d62dd-119">2</span></span>|<span data-ttu-id="d62dd-120">Inscritos pero lo está inscrito a través de perfil de inscripción y el perfil inscrito es diferente del perfil asignado.</span><span class="sxs-lookup"><span data-stu-id="d62dd-120">Enrolled but it's enrolled via enrollment profile and the enrolled profile is different from the assigned profile.</span></span>|
|<span data-ttu-id="d62dd-121">failed</span><span class="sxs-lookup"><span data-stu-id="d62dd-121">failed</span></span>|<span data-ttu-id="d62dd-122">3</span><span class="sxs-lookup"><span data-stu-id="d62dd-122">3</span></span>|<span data-ttu-id="d62dd-123">No se inscriben y no hay registro de errores de inscripción.</span><span class="sxs-lookup"><span data-stu-id="d62dd-123">Not enrolled and there is enrollment failure record.</span></span>|
|<span data-ttu-id="d62dd-124">notContacted</span><span class="sxs-lookup"><span data-stu-id="d62dd-124">notContacted</span></span>|<span data-ttu-id="d62dd-125">4</span><span class="sxs-lookup"><span data-stu-id="d62dd-125">4</span></span>|<span data-ttu-id="d62dd-126">Dispositivo se importa, pero no se inscriben.</span><span class="sxs-lookup"><span data-stu-id="d62dd-126">Device is imported but not enrolled.</span></span>|
|<span data-ttu-id="d62dd-127">bloqueado</span><span class="sxs-lookup"><span data-stu-id="d62dd-127">blocked</span></span>|<span data-ttu-id="d62dd-128">5</span><span class="sxs-lookup"><span data-stu-id="d62dd-128">5</span></span>|<span data-ttu-id="d62dd-129">Dispositivo está inscrito como userless, pero se bloquea de mover a inscripción de usuario porque no se pudo instalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d62dd-129">Device is enrolled as userless, but is blocked from moving to user enrollment because the app failed to install.</span></span>|





