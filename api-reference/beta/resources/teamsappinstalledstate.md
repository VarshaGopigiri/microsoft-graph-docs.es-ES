---
title: Members
description: Describe el estado actual de la instalación de un teamsApp.
author: nkramer
ms.openlocfilehash: a73c68298c4cdf65deee68fb3bd707d50bc2475a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27316796"
---
#<a name="teamsappinstalledstate-enum-type"></a><span data-ttu-id="389fa-103">tipo de enumeración teamsAppInstalledState</span><span class="sxs-lookup"><span data-stu-id="389fa-103">teamsAppInstalledState enum type</span></span>

> <span data-ttu-id="389fa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="389fa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="389fa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="389fa-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="389fa-106">Describe el estado actual de la instalación de un [teamsApp](teamsapp.md).</span><span class="sxs-lookup"><span data-stu-id="389fa-106">Describes the current installation status of a [teamsApp](teamsapp.md).</span></span>

## <a name="members"></a><span data-ttu-id="389fa-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="389fa-107">Members</span></span>

| <span data-ttu-id="389fa-108">Miembro	</span><span class="sxs-lookup"><span data-stu-id="389fa-108">Member</span></span> | <span data-ttu-id="389fa-109">Valor</span><span class="sxs-lookup"><span data-stu-id="389fa-109">Value</span></span>| <span data-ttu-id="389fa-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="389fa-110">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="389fa-111">estáninstaladas</span><span class="sxs-lookup"><span data-stu-id="389fa-111">notInstalled</span></span>|<span data-ttu-id="389fa-112">0</span><span class="sxs-lookup"><span data-stu-id="389fa-112">0</span></span>|<span data-ttu-id="389fa-113">No se instala la aplicación al equipo.</span><span class="sxs-lookup"><span data-stu-id="389fa-113">App is not installed to team.</span></span>|
|<span data-ttu-id="389fa-114">instalado</span><span class="sxs-lookup"><span data-stu-id="389fa-114">installed</span></span>|<span data-ttu-id="389fa-115">1</span><span class="sxs-lookup"><span data-stu-id="389fa-115">1</span></span>|<span data-ttu-id="389fa-116">Aplicación se instala normalmente.</span><span class="sxs-lookup"><span data-stu-id="389fa-116">App is installed normally.</span></span>|
|<span data-ttu-id="389fa-117">installedAndHidden</span><span class="sxs-lookup"><span data-stu-id="389fa-117">installedAndHidden</span></span>|<span data-ttu-id="389fa-118">2</span><span class="sxs-lookup"><span data-stu-id="389fa-118">2</span></span>|<span data-ttu-id="389fa-119">Aplicación está instalada pero se oculta de la vista.</span><span class="sxs-lookup"><span data-stu-id="389fa-119">App is installed but hidden from view.</span></span>|
|<span data-ttu-id="389fa-120">installedAndPermanent</span><span class="sxs-lookup"><span data-stu-id="389fa-120">installedAndPermanent</span></span>|<span data-ttu-id="389fa-121">3</span><span class="sxs-lookup"><span data-stu-id="389fa-121">3</span></span>|<span data-ttu-id="389fa-122">Aplicación se instala de forma permanente y no se puede quitar.</span><span class="sxs-lookup"><span data-stu-id="389fa-122">App is permanently installed and may not be removed.</span></span>|
