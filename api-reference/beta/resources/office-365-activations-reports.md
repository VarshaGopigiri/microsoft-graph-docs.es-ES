---
title: Obtener informe de activaciones de Office 365
description: El informe de activación de Office 365 le ofrece una vista de los cuales los usuarios han activado sus suscripciones a Office 365 en al menos un dispositivo. Proporciona un desglose de la Office 365 ProPlus, Project y Visio Pro para las activaciones de suscripción de Office 365, así como el desglose de las activaciones de escritorio y dispositivos. Este informe puede ayudarlo a identificar a los usuarios que es posible que necesiten compatibilidad adicional para activar su suscripción de Office.
ms.openlocfilehash: 745ca24de47f576522f2f81e3f9d7b70921d81ea
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089776"
---
# <a name="office-365-activations-reports"></a><span data-ttu-id="8ba32-105">Obtener informe de activaciones de Office 365</span><span class="sxs-lookup"><span data-stu-id="8ba32-105">Office 365 activations reports</span></span>

> <span data-ttu-id="8ba32-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8ba32-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8ba32-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8ba32-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8ba32-108">El informe de activación de Office 365 le ofrece una vista de los cuales los usuarios han activado sus suscripciones a Office 365 en al menos un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ba32-108">The Office 365 activation report gives you a view of which users have activated their Office 365 subscriptions on at least one device.</span></span> <span data-ttu-id="8ba32-109">Proporciona un desglose de la Office 365 ProPlus, Project y Visio Pro para las activaciones de suscripción de Office 365, así como el desglose de las activaciones de escritorio y dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8ba32-109">It provides a breakdown of the Office 365 ProPlus, Project, and Visio Pro for Office 365 subscription activations, as well as the breakdown of activations across desktop and devices.</span></span> <span data-ttu-id="8ba32-110">Este informe puede ayudarlo a identificar a los usuarios que es posible que necesiten compatibilidad adicional para activar su suscripción de Office.</span><span class="sxs-lookup"><span data-stu-id="8ba32-110">This report could help you identify users who might need additional support to activate their Office subscription.</span></span>

> <span data-ttu-id="8ba32-111">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Activaciones de Microsoft Office](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60).</span><span class="sxs-lookup"><span data-stu-id="8ba32-111">**Note:** For details about different report views and names, see [Office 365 Reports - Microsoft Office activations](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60).</span></span>

## <a name="reports"></a><span data-ttu-id="8ba32-112">Informes</span><span class="sxs-lookup"><span data-stu-id="8ba32-112">Reports</span></span>
| <span data-ttu-id="8ba32-113">Función</span><span class="sxs-lookup"><span data-stu-id="8ba32-113">Function</span></span>                                 | <span data-ttu-id="8ba32-114">Tipo de valor devuelto de CSV</span><span class="sxs-lookup"><span data-stu-id="8ba32-114">CSV return type</span></span> | <span data-ttu-id="8ba32-115">Tipo de valor devuelto de JSON</span><span class="sxs-lookup"><span data-stu-id="8ba32-115">JSON return type</span></span>                         | <span data-ttu-id="8ba32-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ba32-116">Description</span></span>                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [<span data-ttu-id="8ba32-117">Obtener detalles del usuario</span><span class="sxs-lookup"><span data-stu-id="8ba32-117">Get user detail</span></span>](../api/reportroot-getoffice365activationsuserdetail.md) | <span data-ttu-id="8ba32-118">Secuencia</span><span class="sxs-lookup"><span data-stu-id="8ba32-118">Stream</span></span>          | [<span data-ttu-id="8ba32-119">office365ActivationsUserDetail</span><span class="sxs-lookup"><span data-stu-id="8ba32-119">office365ActivationsUserDetail</span></span>](../resources/office365activationsuserdetail.md) | <span data-ttu-id="8ba32-120">Obtiene información sobre qué usuarios activaron Office 365.</span><span class="sxs-lookup"><span data-stu-id="8ba32-120">Get details about users who have activated Office 365.</span></span> |
| [<span data-ttu-id="8ba32-121">Obtener recuentos de activación</span><span class="sxs-lookup"><span data-stu-id="8ba32-121">Get activation counts</span></span>](../api/reportroot-getoffice365activationcounts.md) | <span data-ttu-id="8ba32-122">Secuencia</span><span class="sxs-lookup"><span data-stu-id="8ba32-122">Stream</span></span>          | [<span data-ttu-id="8ba32-123">office365ActivationCounts</span><span class="sxs-lookup"><span data-stu-id="8ba32-123">office365ActivationCounts</span></span>](../resources/office365activationcounts.md) | <span data-ttu-id="8ba32-124">Obtiene el número de activaciones de Office 365 en dispositivos y equipos de escritorio.</span><span class="sxs-lookup"><span data-stu-id="8ba32-124">Get the count of Office 365 activations on desktops and devices.</span></span> |
| [<span data-ttu-id="8ba32-125">Obtener número de usuarios</span><span class="sxs-lookup"><span data-stu-id="8ba32-125">Get user counts</span></span>](../api/reportroot-getoffice365activationsusercounts.md) | <span data-ttu-id="8ba32-126">Secuencia</span><span class="sxs-lookup"><span data-stu-id="8ba32-126">Stream</span></span>          | [<span data-ttu-id="8ba32-127">office365ActivationsUserCounts</span><span class="sxs-lookup"><span data-stu-id="8ba32-127">office365ActivationsUserCounts</span></span>](../resources/office365activationsusercounts.md) | <span data-ttu-id="8ba32-128">Obtiene el número de usuarios habilitados y el número de usuarios que activaron la suscripción de Office en dispositivos o equipos de escritorio.</span><span class="sxs-lookup"><span data-stu-id="8ba32-128">Get the count of users that are enabled and those that have activated the Office subscription on desktop or devices.</span></span> |