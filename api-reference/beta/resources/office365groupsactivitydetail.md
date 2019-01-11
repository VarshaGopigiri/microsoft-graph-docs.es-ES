---
title: tipo de recurso office365GroupsActivityDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 94dc10064c0005770294c8f783c77d41ce0c479b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27894274"
---
# <a name="office365groupsactivitydetail-resource-type"></a><span data-ttu-id="d7e8f-103">tipo de recurso office365GroupsActivityDetail</span><span class="sxs-lookup"><span data-stu-id="d7e8f-103">office365GroupsActivityDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="d7e8f-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d7e8f-104">Properties</span></span>

| <span data-ttu-id="d7e8f-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d7e8f-105">Property</span></span>                          | <span data-ttu-id="d7e8f-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="d7e8f-106">Type</span></span>    | <span data-ttu-id="d7e8f-107">Description</span><span class="sxs-lookup"><span data-stu-id="d7e8f-107">Description</span></span>                              |
| :-------------------------------- | :------ | ---------------------------------------- |
| <span data-ttu-id="d7e8f-108">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="d7e8f-108">reportRefreshDate</span></span>                 | <span data-ttu-id="d7e8f-109">Fecha</span><span class="sxs-lookup"><span data-stu-id="d7e8f-109">Date</span></span>    | <span data-ttu-id="d7e8f-110">La fecha más reciente del contenido.</span><span class="sxs-lookup"><span data-stu-id="d7e8f-110">The latest date of the content.</span></span>          |
| <span data-ttu-id="d7e8f-111">groupDisplayName</span><span class="sxs-lookup"><span data-stu-id="d7e8f-111">groupDisplayName</span></span>                  | <span data-ttu-id="d7e8f-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="d7e8f-112">String</span></span>  | <span data-ttu-id="d7e8f-113">El nombre para mostrar del grupo.</span><span class="sxs-lookup"><span data-stu-id="d7e8f-113">The display name of the group.</span></span>           |
| <span data-ttu-id="d7e8f-114">isDeleted</span><span class="sxs-lookup"><span data-stu-id="d7e8f-114">isDeleted</span></span>                         | <span data-ttu-id="d7e8f-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="d7e8f-115">Boolean</span></span> | <span data-ttu-id="d7e8f-116">Si este usuario se ha eliminado o suave eliminados.</span><span class="sxs-lookup"><span data-stu-id="d7e8f-116">Whether this user has been deleted or soft deleted.</span></span> |
| <span data-ttu-id="d7e8f-117">ownerPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d7e8f-117">ownerPrincipalName</span></span>                | <span data-ttu-id="d7e8f-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="d7e8f-118">String</span></span>  | <span data-ttu-id="d7e8f-119">El nombre de entidad de seguridad del propietario de grupo.</span><span class="sxs-lookup"><span data-stu-id="d7e8f-119">The group owner principal name.</span></span>          |
| <span data-ttu-id="d7e8f-120">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="d7e8f-120">lastActivityDate</span></span>                  | <span data-ttu-id="d7e8f-121">Fecha</span><span class="sxs-lookup"><span data-stu-id="d7e8f-121">Date</span></span>    | <span data-ttu-id="d7e8f-122">La fecha de última actividad para los siguientes escenarios: grupo de correo electrónico del buzón de correo recibido; usuario ve, edita, compartidos o sincronizados los archivos de biblioteca de documentos de SharePoint; usuario ve las páginas de SharePoint; usuario registrado, lea o había gustado los mensajes en grupos de Yammer.</span><span class="sxs-lookup"><span data-stu-id="d7e8f-122">The last activity date for the following scenarios:  group mailbox received email; user viewed, edited, shared, or synced files in SharePoint document library; user viewed SharePoint pages; user posted, read, or liked messages in Yammer groups.</span></span> |
| <span data-ttu-id="d7e8f-123">groupType</span><span class="sxs-lookup"><span data-stu-id="d7e8f-123">groupType</span></span>                         | <span data-ttu-id="d7e8f-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="d7e8f-124">String</span></span>  | <span data-ttu-id="d7e8f-125">El tipo de grupo.</span><span class="sxs-lookup"><span data-stu-id="d7e8f-125">The group type.</span></span> <span data-ttu-id="d7e8f-126">Los valores posibles son: **público** o **privado**.</span><span class="sxs-lookup"><span data-stu-id="d7e8f-126">Possible values are: **Public** or **Private**.</span></span> |
| <span data-ttu-id="d7e8f-127">memberCount</span><span class="sxs-lookup"><span data-stu-id="d7e8f-127">memberCount</span></span>                       | <span data-ttu-id="d7e8f-128">Int64</span><span class="sxs-lookup"><span data-stu-id="d7e8f-128">Int64</span></span>   | <span data-ttu-id="d7e8f-129">El recuento de miembros de grupo.</span><span class="sxs-lookup"><span data-stu-id="d7e8f-129">The group member count.</span></span>                  |
| <span data-ttu-id="d7e8f-130">externalMemberCount</span><span class="sxs-lookup"><span data-stu-id="d7e8f-130">externalMemberCount</span></span>               | <span data-ttu-id="d7e8f-131">Int64</span><span class="sxs-lookup"><span data-stu-id="d7e8f-131">Int64</span></span>   | <span data-ttu-id="d7e8f-132">El recuento de miembros externos del grupo.</span><span class="sxs-lookup"><span data-stu-id="d7e8f-132">The group external member count.</span></span>         |
| <span data-ttu-id="d7e8f-133">exchangeReceivedEmailCount</span><span class="sxs-lookup"><span data-stu-id="d7e8f-133">exchangeReceivedEmailCount</span></span>        | <span data-ttu-id="d7e8f-134">Int64</span><span class="sxs-lookup"><span data-stu-id="d7e8f-134">Int64</span></span>   | <span data-ttu-id="d7e8f-135">El número de correo electrónico que recibió el buzón de correo de grupo.</span><span class="sxs-lookup"><span data-stu-id="d7e8f-135">The number of email that the group mailbox received.</span></span> |
| <span data-ttu-id="d7e8f-136">sharePointActiveFileCount</span><span class="sxs-lookup"><span data-stu-id="d7e8f-136">sharePointActiveFileCount</span></span>         | <span data-ttu-id="d7e8f-137">Int64</span><span class="sxs-lookup"><span data-stu-id="d7e8f-137">Int64</span></span>   | <span data-ttu-id="d7e8f-138">El número de archivos activos en el sitio de grupo de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d7e8f-138">The number of active files in SharePoint Group site.</span></span> |
| <span data-ttu-id="d7e8f-139">yammerPostedMessageCount</span><span class="sxs-lookup"><span data-stu-id="d7e8f-139">yammerPostedMessageCount</span></span>          | <span data-ttu-id="d7e8f-140">Int64</span><span class="sxs-lookup"><span data-stu-id="d7e8f-140">Int64</span></span>   | <span data-ttu-id="d7e8f-141">El número de los mensajes enviados a grupos de Yammer.</span><span class="sxs-lookup"><span data-stu-id="d7e8f-141">The number of messages posted to Yammer groups.</span></span> |
| <span data-ttu-id="d7e8f-142">yammerReadMessageCount</span><span class="sxs-lookup"><span data-stu-id="d7e8f-142">yammerReadMessageCount</span></span>            | <span data-ttu-id="d7e8f-143">Int64</span><span class="sxs-lookup"><span data-stu-id="d7e8f-143">Int64</span></span>   | <span data-ttu-id="d7e8f-144">El número de mensajes leídos en grupos de Yammer.</span><span class="sxs-lookup"><span data-stu-id="d7e8f-144">The number of messages read in Yammer groups.</span></span> |
| <span data-ttu-id="d7e8f-145">yammerLikedMessageCount</span><span class="sxs-lookup"><span data-stu-id="d7e8f-145">yammerLikedMessageCount</span></span>           | <span data-ttu-id="d7e8f-146">Int64</span><span class="sxs-lookup"><span data-stu-id="d7e8f-146">Int64</span></span>   | <span data-ttu-id="d7e8f-147">El número de mensajes en grupos de Yammer.</span><span class="sxs-lookup"><span data-stu-id="d7e8f-147">The number of messages liked in Yammer groups.</span></span> |
| <span data-ttu-id="d7e8f-148">exchangeMailboxTotalItemCount</span><span class="sxs-lookup"><span data-stu-id="d7e8f-148">exchangeMailboxTotalItemCount</span></span>     | <span data-ttu-id="d7e8f-149">Int64</span><span class="sxs-lookup"><span data-stu-id="d7e8f-149">Int64</span></span>   | <span data-ttu-id="d7e8f-150">El número de elementos en el buzón de correo de grupo.</span><span class="sxs-lookup"><span data-stu-id="d7e8f-150">The number of items in the group mailbox.</span></span> |
| <span data-ttu-id="d7e8f-151">exchangeMailboxStorageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="d7e8f-151">exchangeMailboxStorageUsedInBytes</span></span> | <span data-ttu-id="d7e8f-152">Int64</span><span class="sxs-lookup"><span data-stu-id="d7e8f-152">Int64</span></span>   | <span data-ttu-id="d7e8f-153">El almacenamiento utilizado del buzón de grupo.</span><span class="sxs-lookup"><span data-stu-id="d7e8f-153">The storage used of the group mailbox.</span></span>   |
| <span data-ttu-id="d7e8f-154">sharePointTotalFileCount</span><span class="sxs-lookup"><span data-stu-id="d7e8f-154">sharePointTotalFileCount</span></span>          | <span data-ttu-id="d7e8f-155">Int64</span><span class="sxs-lookup"><span data-stu-id="d7e8f-155">Int64</span></span>   | <span data-ttu-id="d7e8f-156">El número total de archivos en el sitio de grupo de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d7e8f-156">The total number of files in SharePoint Group site.</span></span> |
| <span data-ttu-id="d7e8f-157">sharePointSiteStorageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="d7e8f-157">sharePointSiteStorageUsedInBytes</span></span>  | <span data-ttu-id="d7e8f-158">Int64</span><span class="sxs-lookup"><span data-stu-id="d7e8f-158">Int64</span></span>   | <span data-ttu-id="d7e8f-159">El almacenamiento usado por el sitio de grupo de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d7e8f-159">The storage used by SharePoint Group site.</span></span> |
| <span data-ttu-id="d7e8f-160">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="d7e8f-160">reportPeriod</span></span>                      | <span data-ttu-id="d7e8f-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="d7e8f-161">String</span></span>  | <span data-ttu-id="d7e8f-162">El número de días que cubre el informe.</span><span class="sxs-lookup"><span data-stu-id="d7e8f-162">The number of days the report covers.</span></span>    |

## <a name="json-representation"></a><span data-ttu-id="d7e8f-163">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d7e8f-163">JSON representation</span></span>

<span data-ttu-id="d7e8f-164">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d7e8f-164">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365GroupsActivityDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "groupDisplayName": "String", 
  "isDeleted": true, 
  "ownerPrincipalName": "String", 
  "lastActivityDate": "Date", 
  "groupType": "String", 
  "memberCount": 1024, 
  "externalMemberCount": 1024, 
  "exchangeReceivedEmailCount": 1024, 
  "sharePointActiveFileCount": 1024, 
  "yammerPostedMessageCount": 1024, 
  "yammerReadMessageCount": 1024, 
  "yammerLikedMessageCount": 1024, 
  "exchangeMailboxTotalItemCount": 1024, 
  "exchangeMailboxStorageUsedInBytes": 1024, 
  "sharePointTotalFileCount": 1024, 
  "sharePointSiteStorageUsedInBytes": 1024, 
  "reportPeriod": "String"
}
```
