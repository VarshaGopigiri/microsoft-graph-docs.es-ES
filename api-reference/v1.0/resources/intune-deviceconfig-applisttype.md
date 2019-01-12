---
title: tipo de enumeración appListType
description: Posibles valores de la lista de aplicaciones de cumplimiento.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: f1439ab860ab6a1fbf9ff4deb30320bb57fba338
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27967241"
---
# <a name="applisttype-enum-type"></a><span data-ttu-id="effde-103">tipo de enumeración appListType</span><span class="sxs-lookup"><span data-stu-id="effde-103">appListType enum type</span></span>

> <span data-ttu-id="effde-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="effde-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="effde-105">Posibles valores de la lista de aplicaciones de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="effde-105">Possible values of the compliance app list.</span></span>
## <a name="members"></a><span data-ttu-id="effde-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="effde-106">Members</span></span>
|<span data-ttu-id="effde-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="effde-107">Member</span></span>|<span data-ttu-id="effde-108">Valor</span><span class="sxs-lookup"><span data-stu-id="effde-108">Value</span></span>|<span data-ttu-id="effde-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="effde-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="effde-110">none</span><span class="sxs-lookup"><span data-stu-id="effde-110">none</span></span>|<span data-ttu-id="effde-111">0</span><span class="sxs-lookup"><span data-stu-id="effde-111">0</span></span>|<span data-ttu-id="effde-112">Valor predeterminado, sin intención.</span><span class="sxs-lookup"><span data-stu-id="effde-112">Default value, no intent.</span></span>|
|<span data-ttu-id="effde-113">appsInListCompliant</span><span class="sxs-lookup"><span data-stu-id="effde-113">appsInListCompliant</span></span>|<span data-ttu-id="effde-114">1</span><span class="sxs-lookup"><span data-stu-id="effde-114">1</span></span>|<span data-ttu-id="effde-115">La lista representa las aplicaciones que se considerarán compatibles con (solo son compatibles con las aplicaciones de la lista).</span><span class="sxs-lookup"><span data-stu-id="effde-115">The list represents the apps that will be considered compliant (only apps on the list are compliant).</span></span>|
|<span data-ttu-id="effde-116">appsNotInListCompliant</span><span class="sxs-lookup"><span data-stu-id="effde-116">appsNotInListCompliant</span></span>|<span data-ttu-id="effde-117">2</span><span class="sxs-lookup"><span data-stu-id="effde-117">2</span></span>|<span data-ttu-id="effde-118">La lista representa las aplicaciones que se considerarán no conformes (todas las aplicaciones son compatibles excepto en la lista de aplicaciones).</span><span class="sxs-lookup"><span data-stu-id="effde-118">The list represents the apps that will be considered non compliant (all apps are compliant except apps on the list).</span></span>|



