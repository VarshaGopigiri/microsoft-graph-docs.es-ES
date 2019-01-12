---
title: Miembros
description: Describe el estado actual de la instalación de un teamsApp.
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: ca42b56e2c374dbaea1df676e3a84569b192e78c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27937176"
---
#<a name="teamsappinstalledstate-enum-type"></a><span data-ttu-id="a6c4f-103">tipo de enumeración teamsAppInstalledState</span><span class="sxs-lookup"><span data-stu-id="a6c4f-103">teamsAppInstalledState enum type</span></span>

> <span data-ttu-id="a6c4f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a6c4f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a6c4f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a6c4f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a6c4f-106">Describe el estado actual de la instalación de un [teamsApp](teamsapp.md).</span><span class="sxs-lookup"><span data-stu-id="a6c4f-106">Describes the current installation status of a [teamsApp](teamsapp.md).</span></span>

## <a name="members"></a><span data-ttu-id="a6c4f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a6c4f-107">Members</span></span>

| <span data-ttu-id="a6c4f-108">Miembro	</span><span class="sxs-lookup"><span data-stu-id="a6c4f-108">Member</span></span> | <span data-ttu-id="a6c4f-109">Valor</span><span class="sxs-lookup"><span data-stu-id="a6c4f-109">Value</span></span>| <span data-ttu-id="a6c4f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6c4f-110">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="a6c4f-111">estáninstaladas</span><span class="sxs-lookup"><span data-stu-id="a6c4f-111">notInstalled</span></span>|<span data-ttu-id="a6c4f-112">0</span><span class="sxs-lookup"><span data-stu-id="a6c4f-112">0</span></span>|<span data-ttu-id="a6c4f-113">No se instala la aplicación al equipo.</span><span class="sxs-lookup"><span data-stu-id="a6c4f-113">App is not installed to team.</span></span>|
|<span data-ttu-id="a6c4f-114">instalado</span><span class="sxs-lookup"><span data-stu-id="a6c4f-114">installed</span></span>|<span data-ttu-id="a6c4f-115">1</span><span class="sxs-lookup"><span data-stu-id="a6c4f-115">1</span></span>|<span data-ttu-id="a6c4f-116">Aplicación se instala normalmente.</span><span class="sxs-lookup"><span data-stu-id="a6c4f-116">App is installed normally.</span></span>|
|<span data-ttu-id="a6c4f-117">installedAndHidden</span><span class="sxs-lookup"><span data-stu-id="a6c4f-117">installedAndHidden</span></span>|<span data-ttu-id="a6c4f-118">2</span><span class="sxs-lookup"><span data-stu-id="a6c4f-118">2</span></span>|<span data-ttu-id="a6c4f-119">Aplicación está instalada pero se oculta de la vista.</span><span class="sxs-lookup"><span data-stu-id="a6c4f-119">App is installed but hidden from view.</span></span>|
|<span data-ttu-id="a6c4f-120">installedAndPermanent</span><span class="sxs-lookup"><span data-stu-id="a6c4f-120">installedAndPermanent</span></span>|<span data-ttu-id="a6c4f-121">3</span><span class="sxs-lookup"><span data-stu-id="a6c4f-121">3</span></span>|<span data-ttu-id="a6c4f-122">Aplicación se instala de forma permanente y no se puede quitar.</span><span class="sxs-lookup"><span data-stu-id="a6c4f-122">App is permanently installed and may not be removed.</span></span>|
