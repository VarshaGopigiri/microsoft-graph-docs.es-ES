---
title: Crear datos adjuntos
description: Utilice esta API para agregar datos adjuntos a un outlookTask.
author: angelgolfer-ms
ms.openlocfilehash: 3b3cc5d6d4357e74c0b63166a492eafe97813b06
ms.sourcegitcommit: 6b1ba9b3be038cd6247de54a255bad560034fe42
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2019
ms.locfileid: "27771677"
---
# <a name="create-attachment"></a><span data-ttu-id="03eb7-103">Crear dato adjunto</span><span class="sxs-lookup"><span data-stu-id="03eb7-103">Create attachment</span></span>

> <span data-ttu-id="03eb7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="03eb7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="03eb7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="03eb7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="03eb7-106">Utilice esta API para agregar [datos adjuntos](../resources/attachment.md) a un [outlookTask](../resources/outlooktask.md).</span><span class="sxs-lookup"><span data-stu-id="03eb7-106">Use this API to add an [attachment](../resources/attachment.md) to an [outlookTask](../resources/outlooktask.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="03eb7-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="03eb7-107">Permissions</span></span>

<span data-ttu-id="03eb7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="03eb7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="03eb7-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="03eb7-110">Permission type</span></span>      | <span data-ttu-id="03eb7-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="03eb7-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="03eb7-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="03eb7-112">Delegated (work or school account)</span></span> | <span data-ttu-id="03eb7-113">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="03eb7-113">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="03eb7-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="03eb7-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="03eb7-115">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="03eb7-115">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="03eb7-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="03eb7-116">Application</span></span> | <span data-ttu-id="03eb7-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="03eb7-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="03eb7-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="03eb7-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/outlook/tasks/{id}/attachments
POST /users/{id|userPrincipalName}/outlook/tasks/{id}/attachments
```

## <a name="request-headers"></a><span data-ttu-id="03eb7-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="03eb7-119">Request headers</span></span>

| <span data-ttu-id="03eb7-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="03eb7-120">Name</span></span>       | <span data-ttu-id="03eb7-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="03eb7-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="03eb7-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="03eb7-122">Authorization</span></span>  | <span data-ttu-id="03eb7-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="03eb7-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="03eb7-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="03eb7-125">Content-Type</span></span> | <span data-ttu-id="03eb7-126">Una cadena que representa el tipo de datos en el cuerpo de una entidad.</span><span class="sxs-lookup"><span data-stu-id="03eb7-126">A string that represents the type of data in the body of an entity.</span></span> <span data-ttu-id="03eb7-127">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="03eb7-127">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="03eb7-128">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="03eb7-128">Request body</span></span>

<span data-ttu-id="03eb7-129">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="03eb7-129">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="03eb7-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03eb7-130">Response</span></span>

<span data-ttu-id="03eb7-131">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03eb7-131">If successful, this method returns `201 Created` response code and [attachment](../resources/attachment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="03eb7-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="03eb7-132">Example</span></span>

### <a name="request"></a><span data-ttu-id="03eb7-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="03eb7-133">Request</span></span>

<span data-ttu-id="03eb7-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="03eb7-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_attachment_from_outlooktask"
}-->

```http
POST https://graph.microsoft.com/beta/users/{id}/outlook/tasks/{id}/attachments
Content-type: application/json
Content-length: 142

{
  "lastModifiedDateTime": "datetime-value",
  "name": "name-value",
  "contentType": "contentType-value",
  "size": 99,
  "isInline": true
}
```

### <a name="response"></a><span data-ttu-id="03eb7-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03eb7-135">Response</span></span>

<span data-ttu-id="03eb7-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="03eb7-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment"
} -->

```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 162

{
  "lastModifiedDateTime": "datetime-value",
  "name": "name-value",
  "contentType": "contentType-value",
  "size": 99,
  "isInline": true,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create attachment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->