---
title: Miembros
description: 'Describe la visibilidad de un equipo. '
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: b469a4db4bf535eaa4a7c6300a393381c92158fc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27986450"
---
# <a name="teamvisibilitytype-enum-type"></a><span data-ttu-id="c0b69-103">tipo de enumeración teamVisibilityType</span><span class="sxs-lookup"><span data-stu-id="c0b69-103">teamVisibilityType enum type</span></span>

> <span data-ttu-id="c0b69-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c0b69-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c0b69-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c0b69-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c0b69-106">Describe la visibilidad de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="c0b69-106">Describes the visibility of a [team](../resources/team.md).</span></span> 

## <a name="members"></a><span data-ttu-id="c0b69-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c0b69-107">Members</span></span>

| <span data-ttu-id="c0b69-108">Miembro	</span><span class="sxs-lookup"><span data-stu-id="c0b69-108">Member</span></span> | <span data-ttu-id="c0b69-109">Valor</span><span class="sxs-lookup"><span data-stu-id="c0b69-109">Value</span></span>| <span data-ttu-id="c0b69-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0b69-110">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="c0b69-111">privada</span><span class="sxs-lookup"><span data-stu-id="c0b69-111">private</span></span>|<span data-ttu-id="c0b69-112">0</span><span class="sxs-lookup"><span data-stu-id="c0b69-112">0</span></span>|<span data-ttu-id="c0b69-113">Cualquier persona puede ver que el equipo, pero sólo el propietario puede agregar un usuario al equipo.</span><span class="sxs-lookup"><span data-stu-id="c0b69-113">Anyone can see the team but only the owner can add a user to the team.</span></span>|
|<span data-ttu-id="c0b69-114">public</span><span class="sxs-lookup"><span data-stu-id="c0b69-114">public</span></span>|<span data-ttu-id="c0b69-115">1</span><span class="sxs-lookup"><span data-stu-id="c0b69-115">1</span></span>|<span data-ttu-id="c0b69-116">Cualquier persona puede participar en el equipo.</span><span class="sxs-lookup"><span data-stu-id="c0b69-116">Anyone can join the team.</span></span>|
