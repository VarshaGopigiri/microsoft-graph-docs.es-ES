---
title: Eliminar synchronizationSchema
description: Elimina el esquema personalizado y restablece el esquema a la configuración predeterminada. Si se elimina el esquema en el contexto de la plantilla, restablece el esquema en el valor predeterminado uno asociado con la plantilla `factoryTag`.
ms.openlocfilehash: 81c1a918b10e8f4553b3e99312f20bb538bfbe4f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089155"
---
# <a name="delete-synchronizationschema"></a><span data-ttu-id="d181f-104">Eliminar synchronizationSchema</span><span class="sxs-lookup"><span data-stu-id="d181f-104">Delete synchronizationSchema</span></span>

> <span data-ttu-id="d181f-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d181f-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d181f-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d181f-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d181f-107">Elimina el esquema personalizado y restablece el esquema a la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d181f-107">Deletes the customized schema and resets the schema to the default configuration.</span></span> <span data-ttu-id="d181f-108">Si se elimina el esquema en el contexto de la plantilla, restablece el esquema en el valor predeterminado uno asociado con la plantilla `factoryTag`.</span><span class="sxs-lookup"><span data-stu-id="d181f-108">If the schema is deleted in the context of the template, it resets the schema to the default one associated with the template's `factoryTag`.</span></span>

## <a name="permissions"></a><span data-ttu-id="d181f-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="d181f-109">Permissions</span></span>
<span data-ttu-id="d181f-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d181f-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d181f-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d181f-112">Permission type</span></span>                        | <span data-ttu-id="d181f-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d181f-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="d181f-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d181f-114">Delegated (work or school account)</span></span>     |<span data-ttu-id="d181f-115">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d181f-115">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="d181f-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d181f-116">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="d181f-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d181f-117">Not supported.</span></span>|
|<span data-ttu-id="d181f-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d181f-118">Application</span></span>                            |<span data-ttu-id="d181f-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d181f-119">Not supported.</span></span>| 

## <a name="http-request"></a><span data-ttu-id="d181f-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d181f-120">HTTP Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /servicePrincipals/{id}/synchronization/jobs/{jobId}/schema
DELETE /applications/{id}/synchronization/templates/{templateId}/schema
```

## <a name="request-headers"></a><span data-ttu-id="d181f-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d181f-121">Request headers</span></span>

| <span data-ttu-id="d181f-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="d181f-122">Name</span></span>           | <span data-ttu-id="d181f-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="d181f-123">Type</span></span>    | <span data-ttu-id="d181f-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="d181f-124">Description</span></span>|
|:---------------|:--------|:-----------|
| <span data-ttu-id="d181f-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="d181f-125">Authorization</span></span>  | <span data-ttu-id="d181f-126">string</span><span class="sxs-lookup"><span data-stu-id="d181f-126">string</span></span>  | <span data-ttu-id="d181f-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d181f-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d181f-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d181f-129">Request body</span></span>

<span data-ttu-id="d181f-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d181f-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d181f-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d181f-131">Response</span></span>

<span data-ttu-id="d181f-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 No Content`.</span><span class="sxs-lookup"><span data-stu-id="d181f-132">If successful, this method returns a `201 No Content` response code.</span></span> <span data-ttu-id="d181f-133">No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d181f-133">It does not return anything in response body.</span></span>

## <a name="example"></a><span data-ttu-id="d181f-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d181f-134">Example</span></span>

##### <a name="request"></a><span data-ttu-id="d181f-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d181f-135">Request</span></span>
<span data-ttu-id="d181f-136">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="d181f-136">The following is an example of a request.</span></span>

```http
DELETE https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs/{jobId}/schema
```

##### <a name="response"></a><span data-ttu-id="d181f-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d181f-137">Response</span></span>
<span data-ttu-id="d181f-138">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="d181f-138">The following is an example of a response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete synchronizationSchema",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->