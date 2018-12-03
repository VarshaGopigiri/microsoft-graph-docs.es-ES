---
title: Obtener informe de actividades de Skype Empresarial
description: Puede obtener detalles sobre la actividad en toda la organización. Estos detalles pueden resultarle útiles para investigar, planear y tomar otras decisiones empresariales para la organización.
ms.openlocfilehash: 3681c733ae641dfd421171c864a737ea083eec41
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086490"
---
# <a name="skype-for-business-activity-reports"></a><span data-ttu-id="6de7c-104">Obtener informe de actividades de Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="6de7c-104">Skype for Business activity reports</span></span>

> <span data-ttu-id="6de7c-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6de7c-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6de7c-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6de7c-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6de7c-107">Puede obtener detalles sobre la actividad en toda la organización.</span><span class="sxs-lookup"><span data-stu-id="6de7c-107">You can get details on activity across your organization.</span></span> <span data-ttu-id="6de7c-108">Estos detalles pueden resultarle útiles para investigar, planear y tomar otras decisiones empresariales para la organización.</span><span class="sxs-lookup"><span data-stu-id="6de7c-108">These details can help you investigate, plan, and make other business decisions for your organization.</span></span>

> <span data-ttu-id="6de7c-109">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de Skype Empresarial](https://support.office.com/client/Skype-for-Business-Online-activity-8cbe2eb2-1194-4fd7-b1ee-9f9287c82424).</span><span class="sxs-lookup"><span data-stu-id="6de7c-109">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business activity](https://support.office.com/client/Skype-for-Business-Online-activity-8cbe2eb2-1194-4fd7-b1ee-9f9287c82424).</span></span>

## <a name="reports"></a><span data-ttu-id="6de7c-110">Informes</span><span class="sxs-lookup"><span data-stu-id="6de7c-110">Reports</span></span>

| <span data-ttu-id="6de7c-111">Función</span><span class="sxs-lookup"><span data-stu-id="6de7c-111">Function</span></span>                                 | <span data-ttu-id="6de7c-112">Tipo de valor devuelto de CSV</span><span class="sxs-lookup"><span data-stu-id="6de7c-112">CSV return type</span></span> | <span data-ttu-id="6de7c-113">Tipo de valor devuelto de JSON</span><span class="sxs-lookup"><span data-stu-id="6de7c-113">JSON return type</span></span>                         | <span data-ttu-id="6de7c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="6de7c-114">Description</span></span>                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [<span data-ttu-id="6de7c-115">Obtener detalles del usuario</span><span class="sxs-lookup"><span data-stu-id="6de7c-115">Get user detail</span></span>](../api/reportroot-getskypeforbusinessactivityuserdetail.md) | <span data-ttu-id="6de7c-116">Secuencia</span><span class="sxs-lookup"><span data-stu-id="6de7c-116">Stream</span></span>          | [<span data-ttu-id="6de7c-117">skypeForBusinessActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="6de7c-117">skypeForBusinessActivityUserDetail</span></span>](../resources/skypeforbusinessactivityuserdetail.md) | <span data-ttu-id="6de7c-118">Obtiene información sobre la actividad de Skype Empresarial por usuario.</span><span class="sxs-lookup"><span data-stu-id="6de7c-118">Get details about Skype for Business activity by user.</span></span> |
| [<span data-ttu-id="6de7c-119">Obtener recuentos de actividad</span><span class="sxs-lookup"><span data-stu-id="6de7c-119">Get activity counts</span></span>](../api/reportroot-getskypeforbusinessactivitycounts.md) | <span data-ttu-id="6de7c-120">Secuencia</span><span class="sxs-lookup"><span data-stu-id="6de7c-120">Stream</span></span>          | [<span data-ttu-id="6de7c-121">skypeForBusinessActivityCounts</span><span class="sxs-lookup"><span data-stu-id="6de7c-121">skypeForBusinessActivityCounts</span></span>](../resources/skypeforbusinessactivitycounts.md) | <span data-ttu-id="6de7c-122">Obtiene las tendencias sobre el número de usuarios que organizaron y participaron en sesiones de conferencia realizadas en la organización con Skype Empresarial.</span><span class="sxs-lookup"><span data-stu-id="6de7c-122">Get the trends on how many users organized and participated in conference sessions held in your organization through Skype for Business.</span></span> <span data-ttu-id="6de7c-123">En el informe, también se incluye el número de sesiones de punto a punto.</span><span class="sxs-lookup"><span data-stu-id="6de7c-123">The report also includes the number of peer-to-peer sessions.</span></span> |
| [<span data-ttu-id="6de7c-124">Obtener número de usuarios</span><span class="sxs-lookup"><span data-stu-id="6de7c-124">Get user counts</span></span>](../api/reportroot-getskypeforbusinessactivityusercounts.md) | <span data-ttu-id="6de7c-125">Secuencia</span><span class="sxs-lookup"><span data-stu-id="6de7c-125">Stream</span></span>          | [<span data-ttu-id="6de7c-126">skypeForBusinessActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="6de7c-126">skypeForBusinessActivityUserCounts</span></span>](../resources/skypeforbusinessactivityusercounts.md) | <span data-ttu-id="6de7c-127">Obtiene las tendencias sobre el número de usuarios únicos que organizaron y participaron en sesiones de conferencia realizadas en la organización con Skype Empresarial.</span><span class="sxs-lookup"><span data-stu-id="6de7c-127">Get the trends on how many unique users organized and participated in conference sessions held in your organization through Skype for Business.</span></span> <span data-ttu-id="6de7c-128">En el informe, también se incluye el número de sesiones de punto a punto.</span><span class="sxs-lookup"><span data-stu-id="6de7c-128">The report also includes the number of peer-to-peer sessions.</span></span> |