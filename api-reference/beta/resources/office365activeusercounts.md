---
title: tipo de recurso office365ActiveUserCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 2eaeccb1fa3b67c6b3e1d2d7c88a1dfad4e40e88
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959128"
---
# <a name="office365activeusercounts-resource-type"></a><span data-ttu-id="8fab7-103">tipo de recurso office365ActiveUserCounts</span><span class="sxs-lookup"><span data-stu-id="8fab7-103">office365ActiveUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="8fab7-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8fab7-104">Properties</span></span>

| <span data-ttu-id="8fab7-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8fab7-105">Property</span></span>          | <span data-ttu-id="8fab7-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="8fab7-106">Type</span></span>   | <span data-ttu-id="8fab7-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fab7-107">Description</span></span>                              |
| :---------------- | :----- | ---------------------------------------- |
| <span data-ttu-id="8fab7-108">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="8fab7-108">reportRefreshDate</span></span> | <span data-ttu-id="8fab7-109">Fecha</span><span class="sxs-lookup"><span data-stu-id="8fab7-109">Date</span></span>   | <span data-ttu-id="8fab7-110">La fecha más reciente del contenido.</span><span class="sxs-lookup"><span data-stu-id="8fab7-110">The latest date of the content.</span></span>          |
| <span data-ttu-id="8fab7-111">office365</span><span class="sxs-lookup"><span data-stu-id="8fab7-111">office365</span></span>         | <span data-ttu-id="8fab7-112">Int64</span><span class="sxs-lookup"><span data-stu-id="8fab7-112">Int64</span></span>  | <span data-ttu-id="8fab7-113">El número de usuarios activos en Office 365.</span><span class="sxs-lookup"><span data-stu-id="8fab7-113">The number of active users in Office 365.</span></span> <span data-ttu-id="8fab7-114">Este número incluye todos los usuarios activos en Exchange, OneDrive, SharePoint, Skype para profesionales, Yammer y Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="8fab7-114">This number includes all the active users in Exchange, OneDrive, SharePoint, Skype For Business, Yammer, and Microsoft Teams.</span></span> <span data-ttu-id="8fab7-115">Puede encontrar la definición de usuario activo para cada producto en la descripción de la propiedad respectivos.</span><span class="sxs-lookup"><span data-stu-id="8fab7-115">You can find the definition of active user for each product in the respective property description.</span></span> |
| <span data-ttu-id="8fab7-116">Exchange</span><span class="sxs-lookup"><span data-stu-id="8fab7-116">exchange</span></span>          | <span data-ttu-id="8fab7-117">Int64</span><span class="sxs-lookup"><span data-stu-id="8fab7-117">Int64</span></span>  | <span data-ttu-id="8fab7-118">El número de usuarios activos en Exchange.</span><span class="sxs-lookup"><span data-stu-id="8fab7-118">The number of active users in Exchange.</span></span> <span data-ttu-id="8fab7-119">Cualquier usuario que puedan leer y enviar correo electrónico se considera un usuario activo.</span><span class="sxs-lookup"><span data-stu-id="8fab7-119">Any user who can read and send email is considered an active user.</span></span> |
| <span data-ttu-id="8fab7-120">oneDrive</span><span class="sxs-lookup"><span data-stu-id="8fab7-120">oneDrive</span></span>          | <span data-ttu-id="8fab7-121">Int64</span><span class="sxs-lookup"><span data-stu-id="8fab7-121">Int64</span></span>  | <span data-ttu-id="8fab7-122">El número de usuarios activos en OneDrive.</span><span class="sxs-lookup"><span data-stu-id="8fab7-122">The number of active users in OneDrive.</span></span> <span data-ttu-id="8fab7-123">Cualquier usuario que ve o edita los archivos, archivos compartidos interna o externamente o sincronizado archivos se considera un usuario activo.</span><span class="sxs-lookup"><span data-stu-id="8fab7-123">Any user who viewed or edited files, shared files internally or externally, or synced files is considered an active user.</span></span> |
| <span data-ttu-id="8fab7-124">sharePoint</span><span class="sxs-lookup"><span data-stu-id="8fab7-124">sharePoint</span></span>        | <span data-ttu-id="8fab7-125">Int64</span><span class="sxs-lookup"><span data-stu-id="8fab7-125">Int64</span></span>  | <span data-ttu-id="8fab7-126">El número de usuarios activos en SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8fab7-126">The number of active users in SharePoint.</span></span> <span data-ttu-id="8fab7-127">Cualquier usuario que ve o edita los archivos, archivos compartidos internamente o externamente, sincronizado los archivos o las páginas de SharePoint se considera un usuario activo.</span><span class="sxs-lookup"><span data-stu-id="8fab7-127">Any user who viewed or edited files, shared files internally or externally, synced files, or viewed SharePoint pages is considered an active user.</span></span> |
| <span data-ttu-id="8fab7-128">skypeForBusiness</span><span class="sxs-lookup"><span data-stu-id="8fab7-128">skypeForBusiness</span></span>  | <span data-ttu-id="8fab7-129">Int64</span><span class="sxs-lookup"><span data-stu-id="8fab7-129">Int64</span></span>  | <span data-ttu-id="8fab7-130">El número de usuarios activos en Skype para profesionales.</span><span class="sxs-lookup"><span data-stu-id="8fab7-130">The number of active users in Skype For Business.</span></span> <span data-ttu-id="8fab7-131">Cualquier usuario que organiza o participaron en conferencias o se unió a las sesiones de punto a punto se considera un usuario activo.</span><span class="sxs-lookup"><span data-stu-id="8fab7-131">Any user who organized or participated in conferences, or joined peer-to-peer sessions is considered an active user.</span></span> |
| <span data-ttu-id="8fab7-132">yammer</span><span class="sxs-lookup"><span data-stu-id="8fab7-132">yammer</span></span>            | <span data-ttu-id="8fab7-133">Int64</span><span class="sxs-lookup"><span data-stu-id="8fab7-133">Int64</span></span>  | <span data-ttu-id="8fab7-134">El número de usuarios activos en Yammer.</span><span class="sxs-lookup"><span data-stu-id="8fab7-134">The number of active users in Yammer.</span></span> <span data-ttu-id="8fab7-135">Cualquier usuario que puede enviar, leer o mensajes se considera un usuario activo.</span><span class="sxs-lookup"><span data-stu-id="8fab7-135">Any user who can post, read, or like messages is considered an active user.</span></span> |
| <span data-ttu-id="8fab7-136">equipos</span><span class="sxs-lookup"><span data-stu-id="8fab7-136">teams</span></span>             | <span data-ttu-id="8fab7-137">Int64</span><span class="sxs-lookup"><span data-stu-id="8fab7-137">Int64</span></span>  | <span data-ttu-id="8fab7-138">El número de usuarios activos en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="8fab7-138">The number of active users in Microsoft Teams.</span></span> <span data-ttu-id="8fab7-139">Cualquier usuario que mensajes expuestos en los canales de equipo, los mensajes enviados en las sesiones de chat privado o participaron en las reuniones o las llamadas se considera un usuario activo.</span><span class="sxs-lookup"><span data-stu-id="8fab7-139">Any user who posted messages in team channels, sent messages in private chat sessions, or participated in meetings or calls is considered an active user.</span></span> |
| <span data-ttu-id="8fab7-140">reportDate</span><span class="sxs-lookup"><span data-stu-id="8fab7-140">reportDate</span></span>        | <span data-ttu-id="8fab7-141">Fecha</span><span class="sxs-lookup"><span data-stu-id="8fab7-141">Date</span></span>   | <span data-ttu-id="8fab7-142">La fecha en la que se activa un número de usuarios.</span><span class="sxs-lookup"><span data-stu-id="8fab7-142">The date on which a number of users were active.</span></span> |
| <span data-ttu-id="8fab7-143">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="8fab7-143">reportPeriod</span></span>      | <span data-ttu-id="8fab7-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="8fab7-144">String</span></span> | <span data-ttu-id="8fab7-145">El número de días que cubre el informe.</span><span class="sxs-lookup"><span data-stu-id="8fab7-145">The number of days the report covers.</span></span>    |

## <a name="json-representation"></a><span data-ttu-id="8fab7-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8fab7-146">JSON representation</span></span>

<span data-ttu-id="8fab7-147">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="8fab7-147">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365ActiveUserCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "office365": 1024, 
  "exchange": 1024, 
  "oneDrive": 1024, 
  "sharePoint": 1024, 
  "skypeForBusiness": 1024, 
  "yammer": 1024, 
  "teams": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
