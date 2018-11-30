---
title: tipo de recurso office365ServicesUserCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 975a70b040ac5886ea36219a5407f580a42aeadc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084075"
---
# <a name="office365servicesusercounts-resource-type"></a><span data-ttu-id="61741-103">tipo de recurso office365ServicesUserCounts</span><span class="sxs-lookup"><span data-stu-id="61741-103">office365ServicesUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="61741-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="61741-104">Properties</span></span>

| <span data-ttu-id="61741-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="61741-105">Property</span></span>                 | <span data-ttu-id="61741-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="61741-106">Type</span></span>   | <span data-ttu-id="61741-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="61741-107">Description</span></span>                              |
| :----------------------- | :----- | ---------------------------------------- |
| <span data-ttu-id="61741-108">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="61741-108">reportRefreshDate</span></span>        | <span data-ttu-id="61741-109">Fecha</span><span class="sxs-lookup"><span data-stu-id="61741-109">Date</span></span>   | <span data-ttu-id="61741-110">La fecha más reciente del contenido.</span><span class="sxs-lookup"><span data-stu-id="61741-110">The latest date of the content.</span></span>          |
| <span data-ttu-id="61741-111">exchangeActive</span><span class="sxs-lookup"><span data-stu-id="61741-111">exchangeActive</span></span>           | <span data-ttu-id="61741-112">Int64</span><span class="sxs-lookup"><span data-stu-id="61741-112">Int64</span></span>  | <span data-ttu-id="61741-113">El número de usuarios activos en Exchange.</span><span class="sxs-lookup"><span data-stu-id="61741-113">The number of active users on Exchange.</span></span> <span data-ttu-id="61741-114">Cualquier usuario que puedan leer y enviar correo electrónico se considera un usuario activo.</span><span class="sxs-lookup"><span data-stu-id="61741-114">Any user who can read and send email is considered an active user.</span></span> |
| <span data-ttu-id="61741-115">exchangeInactive</span><span class="sxs-lookup"><span data-stu-id="61741-115">exchangeInactive</span></span>         | <span data-ttu-id="61741-116">Int64</span><span class="sxs-lookup"><span data-stu-id="61741-116">Int64</span></span>  | <span data-ttu-id="61741-117">El número de usuarios inactivos en Exchange.</span><span class="sxs-lookup"><span data-stu-id="61741-117">The number of inactive users on Exchange.</span></span> |
| <span data-ttu-id="61741-118">oneDriveActive</span><span class="sxs-lookup"><span data-stu-id="61741-118">oneDriveActive</span></span>           | <span data-ttu-id="61741-119">Int64</span><span class="sxs-lookup"><span data-stu-id="61741-119">Int64</span></span>  | <span data-ttu-id="61741-120">El número de usuarios activos en OneDrive.</span><span class="sxs-lookup"><span data-stu-id="61741-120">The number of active users on OneDrive.</span></span> <span data-ttu-id="61741-121">Cualquier usuario que ve o edita los archivos, archivos compartidos interna o externamente o sincronizado archivos se considera un usuario activo.</span><span class="sxs-lookup"><span data-stu-id="61741-121">Any user who viewed or edited files, shared files internally or externally, or synced files is considered an active user.</span></span> |
| <span data-ttu-id="61741-122">oneDriveInactive</span><span class="sxs-lookup"><span data-stu-id="61741-122">oneDriveInactive</span></span>         | <span data-ttu-id="61741-123">Int64</span><span class="sxs-lookup"><span data-stu-id="61741-123">Int64</span></span>  | <span data-ttu-id="61741-124">El número de usuarios inactivos en OneDrive.</span><span class="sxs-lookup"><span data-stu-id="61741-124">The number of inactive users on OneDrive.</span></span> |
| <span data-ttu-id="61741-125">sharePointActive</span><span class="sxs-lookup"><span data-stu-id="61741-125">sharePointActive</span></span>         | <span data-ttu-id="61741-126">Int64</span><span class="sxs-lookup"><span data-stu-id="61741-126">Int64</span></span>  | <span data-ttu-id="61741-127">El número de usuarios activos de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="61741-127">The number of active users on SharePoint.</span></span> <span data-ttu-id="61741-128">Cualquier usuario que ve o edita los archivos, archivos compartidos internamente o externamente, sincronizado los archivos o las páginas de SharePoint se considera un usuario activo.</span><span class="sxs-lookup"><span data-stu-id="61741-128">Any user who viewed or edited files, shared files internally or externally, synced files, or viewed SharePoint pages is considered an active user.</span></span> |
| <span data-ttu-id="61741-129">sharePointInactive</span><span class="sxs-lookup"><span data-stu-id="61741-129">sharePointInactive</span></span>       | <span data-ttu-id="61741-130">Int64</span><span class="sxs-lookup"><span data-stu-id="61741-130">Int64</span></span>  | <span data-ttu-id="61741-131">El número de usuarios inactivos en SharePoint.</span><span class="sxs-lookup"><span data-stu-id="61741-131">The number of inactive users on SharePoint.</span></span> |
| <span data-ttu-id="61741-132">skypeForBusinessActive</span><span class="sxs-lookup"><span data-stu-id="61741-132">skypeForBusinessActive</span></span>   | <span data-ttu-id="61741-133">Int64</span><span class="sxs-lookup"><span data-stu-id="61741-133">Int64</span></span>  | <span data-ttu-id="61741-134">El número de usuarios activos en Skype para su negocio.</span><span class="sxs-lookup"><span data-stu-id="61741-134">The number of active users on Skype For Business.</span></span> <span data-ttu-id="61741-135">Cualquier usuario que organiza o participaron en conferencias o se unió a las sesiones de punto a punto se considera un usuario activo.</span><span class="sxs-lookup"><span data-stu-id="61741-135">Any user who organized or participated in conferences, or joined peer-to-peer sessions is considered an active user.</span></span> |
| <span data-ttu-id="61741-136">skypeForBusinessInactive</span><span class="sxs-lookup"><span data-stu-id="61741-136">skypeForBusinessInactive</span></span> | <span data-ttu-id="61741-137">Int64</span><span class="sxs-lookup"><span data-stu-id="61741-137">Int64</span></span>  | <span data-ttu-id="61741-138">El número de usuarios inactivos en Skype para su negocio.</span><span class="sxs-lookup"><span data-stu-id="61741-138">The number of inactive users on Skype For Business.</span></span> |
| <span data-ttu-id="61741-139">yammerActive</span><span class="sxs-lookup"><span data-stu-id="61741-139">yammerActive</span></span>             | <span data-ttu-id="61741-140">Int64</span><span class="sxs-lookup"><span data-stu-id="61741-140">Int64</span></span>  | <span data-ttu-id="61741-141">El número de usuarios activos en Yammer.</span><span class="sxs-lookup"><span data-stu-id="61741-141">The number of active users on Yammer.</span></span> <span data-ttu-id="61741-142">Cualquier usuario que puede enviar, leer o mensajes se considera un usuario activo.</span><span class="sxs-lookup"><span data-stu-id="61741-142">Any user who can post, read, or like messages is considered an active user.</span></span> |
| <span data-ttu-id="61741-143">yammerInactive</span><span class="sxs-lookup"><span data-stu-id="61741-143">yammerInactive</span></span>           | <span data-ttu-id="61741-144">Int64</span><span class="sxs-lookup"><span data-stu-id="61741-144">Int64</span></span>  | <span data-ttu-id="61741-145">El número de usuarios inactivos en Yammer.</span><span class="sxs-lookup"><span data-stu-id="61741-145">The number of inactive users on Yammer.</span></span>  |
| <span data-ttu-id="61741-146">teamsActive</span><span class="sxs-lookup"><span data-stu-id="61741-146">teamsActive</span></span>              | <span data-ttu-id="61741-147">Int64</span><span class="sxs-lookup"><span data-stu-id="61741-147">Int64</span></span>  | <span data-ttu-id="61741-148">El número de usuarios activos en los equipos.</span><span class="sxs-lookup"><span data-stu-id="61741-148">The number of active users on Teams.</span></span> <span data-ttu-id="61741-149">Cualquier usuario que mensajes expuestos en los canales de equipo, los mensajes enviados en las sesiones de chat privado o participaron en las reuniones o las llamadas se considera un usuario activo.</span><span class="sxs-lookup"><span data-stu-id="61741-149">Any user who posted messages in team channels, sent messages in private chat sessions, or participated in meetings or calls is considered an active user.</span></span> |
| <span data-ttu-id="61741-150">teamsInactive</span><span class="sxs-lookup"><span data-stu-id="61741-150">teamsInactive</span></span>            | <span data-ttu-id="61741-151">Int64</span><span class="sxs-lookup"><span data-stu-id="61741-151">Int64</span></span>  | <span data-ttu-id="61741-152">El número de usuarios activos en los equipos.</span><span class="sxs-lookup"><span data-stu-id="61741-152">The number of active users on Teams.</span></span>     |
| <span data-ttu-id="61741-153">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="61741-153">reportPeriod</span></span>             | <span data-ttu-id="61741-154">String</span><span class="sxs-lookup"><span data-stu-id="61741-154">String</span></span> | <span data-ttu-id="61741-155">El número de días que cubre el informe.</span><span class="sxs-lookup"><span data-stu-id="61741-155">The number of days the report covers.</span></span>    |

## <a name="json-representation"></a><span data-ttu-id="61741-156">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="61741-156">JSON representation</span></span>

<span data-ttu-id="61741-157">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="61741-157">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365ServicesUserCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "exchangeActive": 1024, 
  "exchangeInactive": 1024, 
  "oneDriveActive": 1024, 
  "oneDriveInactive": 1024, 
  "sharePointActive": 1024, 
  "sharePointInactive": 1024, 
  "skypeForBusinessActive": 1024, 
  "skypeForBusinessInactive": 1024, 
  "yammerActive": 1024, 
  "yammerInactive": 1024, 
  "teamsActive": 1024, 
  "teamsInactive": 1024, 
  "reportPeriod": "String"
}
```
