---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Proteger archivos
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: fb62dc05c60e26a6d1d6683913eeec0403d1c41c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950812"
---
# <a name="check-in-changes-to-a-driveitem-resource"></a><span data-ttu-id="7d56b-102">Insertar cambios en el repositorio en un recurso DriveItem</span><span class="sxs-lookup"><span data-stu-id="7d56b-102">Check-in changes to a DriveItem resource</span></span>

> <span data-ttu-id="7d56b-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7d56b-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7d56b-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7d56b-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7d56b-105">Inserte un recurso DriveItem que se ha extraído del repositorio, lo que hace que la versión del documento esté disponible para otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="7d56b-105">Check-in a checked out DriveItem resource, which makes the version of the document available to others.</span></span>

## <a name="permissions"></a><span data-ttu-id="7d56b-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="7d56b-106">Permissions</span></span>

<span data-ttu-id="7d56b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7d56b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7d56b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7d56b-109">Permission type</span></span>      | <span data-ttu-id="7d56b-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7d56b-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7d56b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7d56b-111">Delegated (work or school account)</span></span> | <span data-ttu-id="7d56b-112">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7d56b-112">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="7d56b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7d56b-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7d56b-114">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7d56b-114">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="7d56b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7d56b-115">Application</span></span> | <span data-ttu-id="7d56b-116">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7d56b-116">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="7d56b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7d56b-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{driveId}/items/{itemId}/checkin
POST /groups/{groupId}/drive/items/{itemId}/checkin
POST /me/drive/items/{item-id}/checkin
POST /sites/{siteId}/drive/items/{itemId}/checkin
POST /users/{userId}/drive/items/{itemId}/checkin
```

### <a name="request-body"></a><span data-ttu-id="7d56b-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7d56b-118">Request body</span></span>

<span data-ttu-id="7d56b-119">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="7d56b-119">In the request body, provide a JSON object with the following parameters.</span></span>


|   <span data-ttu-id="7d56b-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="7d56b-120">Name</span></span>    | <span data-ttu-id="7d56b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="7d56b-121">Value</span></span>  |                                                <span data-ttu-id="7d56b-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d56b-122">Description</span></span>                                                |
| :-------- | :----- | :-------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="7d56b-123">checkInAs</span><span class="sxs-lookup"><span data-stu-id="7d56b-123">checkInAs</span></span> | <span data-ttu-id="7d56b-124">string</span><span class="sxs-lookup"><span data-stu-id="7d56b-124">string</span></span> | <span data-ttu-id="7d56b-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="7d56b-125">Optional.</span></span> <span data-ttu-id="7d56b-126">El estado deseado del documento una vez completada la operación de inserción.</span><span class="sxs-lookup"><span data-stu-id="7d56b-126">The desired status of the document after the check-in operation is complete.</span></span> <span data-ttu-id="7d56b-127">Puede ser `published` o no especificarse.</span><span class="sxs-lookup"><span data-stu-id="7d56b-127">Can be `published` or unspecified.</span></span> |
| <span data-ttu-id="7d56b-128">comment</span><span class="sxs-lookup"><span data-stu-id="7d56b-128">comment</span></span>   | <span data-ttu-id="7d56b-129">string</span><span class="sxs-lookup"><span data-stu-id="7d56b-129">string</span></span> | <span data-ttu-id="7d56b-130">Un comentario de inserción asociado a la versión.</span><span class="sxs-lookup"><span data-stu-id="7d56b-130">A check-in comment that is associated with the version.</span></span>                                                   |

## <a name="example"></a><span data-ttu-id="7d56b-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7d56b-131">Example</span></span>

<span data-ttu-id="7d56b-132">Este ejemplo inserta un archivo identificado por `{item-id}` en el repositorio.</span><span class="sxs-lookup"><span data-stu-id="7d56b-132">This example checks in a file identified by `{item-id}`.</span></span>

<!-- { "blockType": "request", "name": "checkin-item", "scopes": "files.readwrite", "target": "action" } -->

```http
POST /drives/{drive-id}/items/{item-id}/checkin
Content-Type: application/json

{
  "comment": "Updating the latest guidelines"
}
```

## <a name="response"></a><span data-ttu-id="7d56b-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7d56b-133">Response</span></span>

<span data-ttu-id="7d56b-134">Si se realiza correctamente, la llamada API devuelve `204 No content`.</span><span class="sxs-lookup"><span data-stu-id="7d56b-134">If successful, the API call returns a `204 No content`.</span></span>

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No content
```

### <a name="remarks"></a><span data-ttu-id="7d56b-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7d56b-135">Remarks</span></span>


[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "Create a copy of an existing item.",
  "keywords": "copy existing item",
  "section": "documentation",
  "tocPath": "Items/Copy"
} -->
