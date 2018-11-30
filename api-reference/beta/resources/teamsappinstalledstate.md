---
title: Members
description: Describe el estado actual de la instalación de un teamsApp.
ms.openlocfilehash: 7f358a621a25219e78e3a02ce081d07a27395d2c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089006"
---
#<a name="teamsappinstalledstate-enum-type"></a><span data-ttu-id="130fc-103">tipo de enumeración teamsAppInstalledState</span><span class="sxs-lookup"><span data-stu-id="130fc-103">teamsAppInstalledState enum type</span></span>

> <span data-ttu-id="130fc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="130fc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="130fc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="130fc-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="130fc-106">Describe el estado actual de la instalación de un [teamsApp](teamsapp.md).</span><span class="sxs-lookup"><span data-stu-id="130fc-106">Describes the current installation status of a [teamsApp](teamsapp.md).</span></span>

## <a name="members"></a><span data-ttu-id="130fc-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="130fc-107">Members</span></span>

| <span data-ttu-id="130fc-108">Miembro	</span><span class="sxs-lookup"><span data-stu-id="130fc-108">Member</span></span> | <span data-ttu-id="130fc-109">Valor</span><span class="sxs-lookup"><span data-stu-id="130fc-109">Value</span></span>| <span data-ttu-id="130fc-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="130fc-110">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="130fc-111">estáninstaladas</span><span class="sxs-lookup"><span data-stu-id="130fc-111">notInstalled</span></span>|<span data-ttu-id="130fc-112">0</span><span class="sxs-lookup"><span data-stu-id="130fc-112">0</span></span>|<span data-ttu-id="130fc-113">No se instala la aplicación al equipo.</span><span class="sxs-lookup"><span data-stu-id="130fc-113">App is not installed to team.</span></span>|
|<span data-ttu-id="130fc-114">instalado</span><span class="sxs-lookup"><span data-stu-id="130fc-114">installed</span></span>|<span data-ttu-id="130fc-115">1</span><span class="sxs-lookup"><span data-stu-id="130fc-115">1</span></span>|<span data-ttu-id="130fc-116">Aplicación se instala normalmente.</span><span class="sxs-lookup"><span data-stu-id="130fc-116">App is installed normally.</span></span>|
|<span data-ttu-id="130fc-117">installedAndHidden</span><span class="sxs-lookup"><span data-stu-id="130fc-117">installedAndHidden</span></span>|<span data-ttu-id="130fc-118">2</span><span class="sxs-lookup"><span data-stu-id="130fc-118">2</span></span>|<span data-ttu-id="130fc-119">Aplicación está instalada pero se oculta de la vista.</span><span class="sxs-lookup"><span data-stu-id="130fc-119">App is installed but hidden from view.</span></span>|
|<span data-ttu-id="130fc-120">installedAndPermanent</span><span class="sxs-lookup"><span data-stu-id="130fc-120">installedAndPermanent</span></span>|<span data-ttu-id="130fc-121">3</span><span class="sxs-lookup"><span data-stu-id="130fc-121">3</span></span>|<span data-ttu-id="130fc-122">Aplicación se instala de forma permanente y no se puede quitar.</span><span class="sxs-lookup"><span data-stu-id="130fc-122">App is permanently installed and may not be removed.</span></span>|
