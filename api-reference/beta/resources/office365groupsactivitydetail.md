---
title: tipo de recurso office365GroupsActivityDetail
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: a849932d646be61f3cedec76ecdafdaca941baaf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083921"
---
# <a name="office365groupsactivitydetail-resource-type"></a><span data-ttu-id="67810-103">tipo de recurso office365GroupsActivityDetail</span><span class="sxs-lookup"><span data-stu-id="67810-103">office365GroupsActivityDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="67810-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="67810-104">Properties</span></span>

| <span data-ttu-id="67810-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="67810-105">Property</span></span>                          | <span data-ttu-id="67810-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="67810-106">Type</span></span>    | <span data-ttu-id="67810-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="67810-107">Description</span></span>                              |
| :-------------------------------- | :------ | ---------------------------------------- |
| <span data-ttu-id="67810-108">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="67810-108">reportRefreshDate</span></span>                 | <span data-ttu-id="67810-109">Fecha</span><span class="sxs-lookup"><span data-stu-id="67810-109">Date</span></span>    | <span data-ttu-id="67810-110">La fecha más reciente del contenido.</span><span class="sxs-lookup"><span data-stu-id="67810-110">The latest date of the content.</span></span>          |
| <span data-ttu-id="67810-111">groupDisplayName</span><span class="sxs-lookup"><span data-stu-id="67810-111">groupDisplayName</span></span>                  | <span data-ttu-id="67810-112">String</span><span class="sxs-lookup"><span data-stu-id="67810-112">String</span></span>  | <span data-ttu-id="67810-113">El nombre para mostrar del grupo.</span><span class="sxs-lookup"><span data-stu-id="67810-113">The display name of the group.</span></span>           |
| <span data-ttu-id="67810-114">isDeleted</span><span class="sxs-lookup"><span data-stu-id="67810-114">isDeleted</span></span>                         | <span data-ttu-id="67810-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="67810-115">Boolean</span></span> | <span data-ttu-id="67810-116">Si este usuario se ha eliminado o suave eliminados.</span><span class="sxs-lookup"><span data-stu-id="67810-116">Whether this user has been deleted or soft deleted.</span></span> |
| <span data-ttu-id="67810-117">ownerPrincipalName</span><span class="sxs-lookup"><span data-stu-id="67810-117">ownerPrincipalName</span></span>                | <span data-ttu-id="67810-118">String</span><span class="sxs-lookup"><span data-stu-id="67810-118">String</span></span>  | <span data-ttu-id="67810-119">El nombre de entidad de seguridad del propietario de grupo.</span><span class="sxs-lookup"><span data-stu-id="67810-119">The group owner principal name.</span></span>          |
| <span data-ttu-id="67810-120">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="67810-120">lastActivityDate</span></span>                  | <span data-ttu-id="67810-121">Fecha</span><span class="sxs-lookup"><span data-stu-id="67810-121">Date</span></span>    | <span data-ttu-id="67810-122">La fecha de última actividad para los siguientes escenarios: grupo de correo electrónico del buzón de correo recibido; usuario ve, edita, compartidos o sincronizados los archivos de biblioteca de documentos de SharePoint; usuario ve las páginas de SharePoint; usuario registrado, lea o había gustado los mensajes en grupos de Yammer.</span><span class="sxs-lookup"><span data-stu-id="67810-122">The last activity date for the following scenarios:  group mailbox received email; user viewed, edited, shared, or synced files in SharePoint document library; user viewed SharePoint pages; user posted, read, or liked messages in Yammer groups.</span></span> |
| <span data-ttu-id="67810-123">groupType</span><span class="sxs-lookup"><span data-stu-id="67810-123">groupType</span></span>                         | <span data-ttu-id="67810-124">String</span><span class="sxs-lookup"><span data-stu-id="67810-124">String</span></span>  | <span data-ttu-id="67810-125">El tipo de grupo.</span><span class="sxs-lookup"><span data-stu-id="67810-125">The group type.</span></span> <span data-ttu-id="67810-126">Los valores posibles son: **público** o **privado**.</span><span class="sxs-lookup"><span data-stu-id="67810-126">Possible values are: **Public** or **Private**.</span></span> |
| <span data-ttu-id="67810-127">memberCount</span><span class="sxs-lookup"><span data-stu-id="67810-127">memberCount</span></span>                       | <span data-ttu-id="67810-128">Int64</span><span class="sxs-lookup"><span data-stu-id="67810-128">Int64</span></span>   | <span data-ttu-id="67810-129">El recuento de miembros de grupo.</span><span class="sxs-lookup"><span data-stu-id="67810-129">The group member count.</span></span>                  |
| <span data-ttu-id="67810-130">externalMemberCount</span><span class="sxs-lookup"><span data-stu-id="67810-130">externalMemberCount</span></span>               | <span data-ttu-id="67810-131">Int64</span><span class="sxs-lookup"><span data-stu-id="67810-131">Int64</span></span>   | <span data-ttu-id="67810-132">El recuento de miembros externos del grupo.</span><span class="sxs-lookup"><span data-stu-id="67810-132">The group external member count.</span></span>         |
| <span data-ttu-id="67810-133">exchangeReceivedEmailCount</span><span class="sxs-lookup"><span data-stu-id="67810-133">exchangeReceivedEmailCount</span></span>        | <span data-ttu-id="67810-134">Int64</span><span class="sxs-lookup"><span data-stu-id="67810-134">Int64</span></span>   | <span data-ttu-id="67810-135">El número de correo electrónico que recibió el buzón de correo de grupo.</span><span class="sxs-lookup"><span data-stu-id="67810-135">The number of email that the group mailbox received.</span></span> |
| <span data-ttu-id="67810-136">sharePointActiveFileCount</span><span class="sxs-lookup"><span data-stu-id="67810-136">sharePointActiveFileCount</span></span>         | <span data-ttu-id="67810-137">Int64</span><span class="sxs-lookup"><span data-stu-id="67810-137">Int64</span></span>   | <span data-ttu-id="67810-138">El número de archivos activos en el sitio de grupo de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="67810-138">The number of active files in SharePoint Group site.</span></span> |
| <span data-ttu-id="67810-139">yammerPostedMessageCount</span><span class="sxs-lookup"><span data-stu-id="67810-139">yammerPostedMessageCount</span></span>          | <span data-ttu-id="67810-140">Int64</span><span class="sxs-lookup"><span data-stu-id="67810-140">Int64</span></span>   | <span data-ttu-id="67810-141">El número de los mensajes enviados a grupos de Yammer.</span><span class="sxs-lookup"><span data-stu-id="67810-141">The number of messages posted to Yammer groups.</span></span> |
| <span data-ttu-id="67810-142">yammerReadMessageCount</span><span class="sxs-lookup"><span data-stu-id="67810-142">yammerReadMessageCount</span></span>            | <span data-ttu-id="67810-143">Int64</span><span class="sxs-lookup"><span data-stu-id="67810-143">Int64</span></span>   | <span data-ttu-id="67810-144">El número de mensajes leídos en grupos de Yammer.</span><span class="sxs-lookup"><span data-stu-id="67810-144">The number of messages read in Yammer groups.</span></span> |
| <span data-ttu-id="67810-145">yammerLikedMessageCount</span><span class="sxs-lookup"><span data-stu-id="67810-145">yammerLikedMessageCount</span></span>           | <span data-ttu-id="67810-146">Int64</span><span class="sxs-lookup"><span data-stu-id="67810-146">Int64</span></span>   | <span data-ttu-id="67810-147">El número de mensajes en grupos de Yammer.</span><span class="sxs-lookup"><span data-stu-id="67810-147">The number of messages liked in Yammer groups.</span></span> |
| <span data-ttu-id="67810-148">exchangeMailboxTotalItemCount</span><span class="sxs-lookup"><span data-stu-id="67810-148">exchangeMailboxTotalItemCount</span></span>     | <span data-ttu-id="67810-149">Int64</span><span class="sxs-lookup"><span data-stu-id="67810-149">Int64</span></span>   | <span data-ttu-id="67810-150">El número de elementos en el buzón de correo de grupo.</span><span class="sxs-lookup"><span data-stu-id="67810-150">The number of items in the group mailbox.</span></span> |
| <span data-ttu-id="67810-151">exchangeMailboxStorageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="67810-151">exchangeMailboxStorageUsedInBytes</span></span> | <span data-ttu-id="67810-152">Int64</span><span class="sxs-lookup"><span data-stu-id="67810-152">Int64</span></span>   | <span data-ttu-id="67810-153">El almacenamiento utilizado del buzón de grupo.</span><span class="sxs-lookup"><span data-stu-id="67810-153">The storage used of the group mailbox.</span></span>   |
| <span data-ttu-id="67810-154">sharePointTotalFileCount</span><span class="sxs-lookup"><span data-stu-id="67810-154">sharePointTotalFileCount</span></span>          | <span data-ttu-id="67810-155">Int64</span><span class="sxs-lookup"><span data-stu-id="67810-155">Int64</span></span>   | <span data-ttu-id="67810-156">El número total de archivos en el sitio de grupo de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="67810-156">The total number of files in SharePoint Group site.</span></span> |
| <span data-ttu-id="67810-157">sharePointSiteStorageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="67810-157">sharePointSiteStorageUsedInBytes</span></span>  | <span data-ttu-id="67810-158">Int64</span><span class="sxs-lookup"><span data-stu-id="67810-158">Int64</span></span>   | <span data-ttu-id="67810-159">El almacenamiento usado por el sitio de grupo de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="67810-159">The storage used by SharePoint Group site.</span></span> |
| <span data-ttu-id="67810-160">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="67810-160">reportPeriod</span></span>                      | <span data-ttu-id="67810-161">String</span><span class="sxs-lookup"><span data-stu-id="67810-161">String</span></span>  | <span data-ttu-id="67810-162">El número de días que cubre el informe.</span><span class="sxs-lookup"><span data-stu-id="67810-162">The number of days the report covers.</span></span>    |

## <a name="json-representation"></a><span data-ttu-id="67810-163">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="67810-163">JSON representation</span></span>

<span data-ttu-id="67810-164">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="67810-164">The following is a JSON representation of the resource.</span></span>

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
