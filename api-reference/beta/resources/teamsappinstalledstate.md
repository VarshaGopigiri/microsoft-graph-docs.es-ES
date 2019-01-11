---
title: Miembros
description: Describe el estado actual de la instalación de un teamsApp.
author: nkramer
localization_priority: Normal
ms.openlocfilehash: 4e453a28b0c3ebc2957cf7e1a92a846e8e4758e6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27847575"
---
#<a name="teamsappinstalledstate-enum-type"></a><span data-ttu-id="121ad-103">tipo de enumeración teamsAppInstalledState</span><span class="sxs-lookup"><span data-stu-id="121ad-103">teamsAppInstalledState enum type</span></span>

> <span data-ttu-id="121ad-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="121ad-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="121ad-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="121ad-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="121ad-106">Describe el estado actual de la instalación de un [teamsApp](teamsapp.md).</span><span class="sxs-lookup"><span data-stu-id="121ad-106">Describes the current installation status of a [teamsApp](teamsapp.md).</span></span>

## <a name="members"></a><span data-ttu-id="121ad-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="121ad-107">Members</span></span>

| <span data-ttu-id="121ad-108">Miembro	</span><span class="sxs-lookup"><span data-stu-id="121ad-108">Member</span></span> | <span data-ttu-id="121ad-109">Valor</span><span class="sxs-lookup"><span data-stu-id="121ad-109">Value</span></span>| <span data-ttu-id="121ad-110">Description</span><span class="sxs-lookup"><span data-stu-id="121ad-110">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="121ad-111">estáninstaladas</span><span class="sxs-lookup"><span data-stu-id="121ad-111">notInstalled</span></span>|<span data-ttu-id="121ad-112">0</span><span class="sxs-lookup"><span data-stu-id="121ad-112">0</span></span>|<span data-ttu-id="121ad-113">No se instala la aplicación al equipo.</span><span class="sxs-lookup"><span data-stu-id="121ad-113">App is not installed to team.</span></span>|
|<span data-ttu-id="121ad-114">instalado</span><span class="sxs-lookup"><span data-stu-id="121ad-114">installed</span></span>|<span data-ttu-id="121ad-115">1</span><span class="sxs-lookup"><span data-stu-id="121ad-115">1</span></span>|<span data-ttu-id="121ad-116">Aplicación se instala normalmente.</span><span class="sxs-lookup"><span data-stu-id="121ad-116">App is installed normally.</span></span>|
|<span data-ttu-id="121ad-117">installedAndHidden</span><span class="sxs-lookup"><span data-stu-id="121ad-117">installedAndHidden</span></span>|<span data-ttu-id="121ad-118">2</span><span class="sxs-lookup"><span data-stu-id="121ad-118">2</span></span>|<span data-ttu-id="121ad-119">Aplicación está instalada pero se oculta de la vista.</span><span class="sxs-lookup"><span data-stu-id="121ad-119">App is installed but hidden from view.</span></span>|
|<span data-ttu-id="121ad-120">installedAndPermanent</span><span class="sxs-lookup"><span data-stu-id="121ad-120">installedAndPermanent</span></span>|<span data-ttu-id="121ad-121">3</span><span class="sxs-lookup"><span data-stu-id="121ad-121">3</span></span>|<span data-ttu-id="121ad-122">Aplicación se instala de forma permanente y no se puede quitar.</span><span class="sxs-lookup"><span data-stu-id="121ad-122">App is permanently installed and may not be removed.</span></span>|
