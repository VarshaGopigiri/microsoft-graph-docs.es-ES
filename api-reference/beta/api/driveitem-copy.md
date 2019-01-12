---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Copiar un archivo o carpeta
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 17c45f33425f77e6f4304360b6d52a0170752f4c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27946297"
---
# <a name="copy-a-driveitem"></a><span data-ttu-id="40ea3-102">Copiar un objeto DriveItem</span><span class="sxs-lookup"><span data-stu-id="40ea3-102">Copy a DriveItem</span></span>

> <span data-ttu-id="40ea3-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="40ea3-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="40ea3-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="40ea3-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="40ea3-105">Crea de forma asincrónica una copia de un objeto [driveItem][item-resource] (incluidos los elementos secundarios), en un nuevo elemento primario o con un nuevo nombre.</span><span class="sxs-lookup"><span data-stu-id="40ea3-105">Asynchronously creates a copy of an [driveItem][item-resource] (including any children), under a new parent item or with a new name.</span></span>

## <a name="permissions"></a><span data-ttu-id="40ea3-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="40ea3-106">Permissions</span></span>

<span data-ttu-id="40ea3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="40ea3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="40ea3-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="40ea3-109">Permission type</span></span>      | <span data-ttu-id="40ea3-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="40ea3-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="40ea3-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="40ea3-111">Delegated (work or school account)</span></span> | <span data-ttu-id="40ea3-112">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="40ea3-112">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="40ea3-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="40ea3-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="40ea3-114">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="40ea3-114">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="40ea3-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="40ea3-115">Application</span></span> | <span data-ttu-id="40ea3-116">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="40ea3-116">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="40ea3-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="40ea3-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{driveId}/items/{itemId}/copy
POST /groups/{groupId}/drive/items/{itemId}/copy
POST /me/drive/items/{item-id}/copy
POST /sites/{siteId}/drive/items/{itemId}/copy
POST /users/{userId}/drive/items/{itemId}/copy
```

### <a name="request-body"></a><span data-ttu-id="40ea3-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="40ea3-118">Request body</span></span>

<span data-ttu-id="40ea3-119">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="40ea3-119">In the request body, provide a JSON object with the following parameters.</span></span>


| <span data-ttu-id="40ea3-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="40ea3-120">Name</span></span>            | <span data-ttu-id="40ea3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="40ea3-121">Value</span></span>                                          | <span data-ttu-id="40ea3-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="40ea3-122">Description</span></span>                                                                                                 |
|:----------------|:-----------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40ea3-123">parentReference</span><span class="sxs-lookup"><span data-stu-id="40ea3-123">parentReference</span></span> | [<span data-ttu-id="40ea3-124">ItemReference</span><span class="sxs-lookup"><span data-stu-id="40ea3-124">ItemReference</span></span>](../resources/itemreference.md) | <span data-ttu-id="40ea3-p103">Opcional. Referencia al elemento primario en que se creará la copia.</span><span class="sxs-lookup"><span data-stu-id="40ea3-p103">Optional. Reference to the parent item the copy will be created in.</span></span>                                         |
| <span data-ttu-id="40ea3-127">name</span><span class="sxs-lookup"><span data-stu-id="40ea3-127">name</span></span>            | <span data-ttu-id="40ea3-128">string</span><span class="sxs-lookup"><span data-stu-id="40ea3-128">string</span></span>                                         | <span data-ttu-id="40ea3-p104">Opcional. El nuevo nombre de la copia. Si no se proporciona, se usará el mismo nombre que el original.</span><span class="sxs-lookup"><span data-stu-id="40ea3-p104">Optional. The new name for the copy. If this isn't provided, the same name will be used as the original.</span></span>    |

<span data-ttu-id="40ea3-132">**Nota:** El valor _parentReference_ debe incluir los parámetros `driveId` y `id` para la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="40ea3-132">**Note:** The _parentReference_ should include the `driveId` and `id` parameters for the target folder.</span></span>

## <a name="example"></a><span data-ttu-id="40ea3-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="40ea3-133">Example</span></span>

<span data-ttu-id="40ea3-134">Este ejemplo copia un archivo identificado por `{item-id}` en una carpeta identificada con un valor `driveId` y `id`.</span><span class="sxs-lookup"><span data-stu-id="40ea3-134">This example copies a file identified by `{item-id}` into a folder identified with a `driveId` and `id` value.</span></span>
<span data-ttu-id="40ea3-135">La nueva copia del archivo se denominará `contoso plan (copy).txt`.</span><span class="sxs-lookup"><span data-stu-id="40ea3-135">The new copy of the file will be named `contoso plan (copy).txt`.</span></span>

<!-- { "blockType": "request", "name": "copy-item", "scopes": "files.readwrite", "target": "action" } -->

```http
POST /me/drive/items/{item-id}/copy
Content-Type: application/json

{
  "parentReference": {
    "driveId": "6F7D00BF-FC4D-4E62-9769-6AEA81F3A21B",
    "id": "DCD0D3AD-8989-4F23-A5A2-2C086050513F"
  },
  "name": "contoso plan (copy).txt"
}
```

## <a name="response"></a><span data-ttu-id="40ea3-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="40ea3-136">Response</span></span>

<span data-ttu-id="40ea3-137">Devuelve detalles sobre cómo [supervisar el progreso](/graph/long-running-actions-overview) de la copia tras aceptar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="40ea3-137">Returns details about how to [monitor the progress](/graph/long-running-actions-overview) of the copy, upon accepting the request.</span></span>

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 202 Accepted
Location: https://contoso.sharepoint.com/_api/v2.0/monitor/4A3407B5-88FC-4504-8B21-0AABD3412717
```

<span data-ttu-id="40ea3-138">El valor del encabezado `Location` proporciona una dirección URL para un servicio que devolverá el estado actual de la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="40ea3-138">The value of the `Location` header provides a URL for a service that will return the current state of the copy operation.</span></span>
<span data-ttu-id="40ea3-139">Puede usar esta información para [determinar cuándo ha finalizado la copia](/graph/long-running-actions-overview).</span><span class="sxs-lookup"><span data-stu-id="40ea3-139">You can use this info to [determine when the copy has finished](/graph/long-running-actions-overview).</span></span>

### <a name="remarks"></a><span data-ttu-id="40ea3-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="40ea3-140">Remarks</span></span>

<span data-ttu-id="40ea3-p107">En muchos casos, la operación de copia se realiza de forma asincrónica. La respuesta de la API solo indicará que la operación de copia se ha aceptado o rechazado, debido a que el nombre de archivo de destino ya está en uso.</span><span class="sxs-lookup"><span data-stu-id="40ea3-p107">In many cases the copy action is performed asynchronously. The response from the API will only indicate that the copy operation was accepted or rejected, say due to the destination filename already being in use.</span></span>

[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "Create a copy of an existing item.",
  "keywords": "copy existing item",
  "section": "documentation",
  "tocPath": "Items/Copy"
} -->
