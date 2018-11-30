---
title: Crear synchronizationTemplate
description: Crear una nueva plantilla de sincronización para una aplicación determinada.
ms.openlocfilehash: 1c7bc08eee4088796123d3c7fa2cac5c83becac2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085092"
---
# <a name="create-synchronizationtemplate"></a><span data-ttu-id="1997f-103">Crear synchronizationTemplate</span><span class="sxs-lookup"><span data-stu-id="1997f-103">Create synchronizationTemplate</span></span>

> <span data-ttu-id="1997f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1997f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1997f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1997f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1997f-106">Crear una nueva plantilla de sincronización para una aplicación determinada.</span><span class="sxs-lookup"><span data-stu-id="1997f-106">Create a new synchronization template for a given application.</span></span>

## <a name="permissions"></a><span data-ttu-id="1997f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="1997f-107">Permissions</span></span>
<span data-ttu-id="1997f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1997f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1997f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1997f-110">Permission type</span></span>                        | <span data-ttu-id="1997f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1997f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="1997f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1997f-112">Delegated (work or school account)</span></span>     |<span data-ttu-id="1997f-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1997f-113">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="1997f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1997f-114">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="1997f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1997f-115">Not supported.</span></span>|
|<span data-ttu-id="1997f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1997f-116">Application</span></span>                            |<span data-ttu-id="1997f-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1997f-117">Not supported.</span></span>| 

### <a name="http-request"></a><span data-ttu-id="1997f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1997f-118">HTTP Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /applications/{id}/synchronization/templates/
```

## <a name="request-headers"></a><span data-ttu-id="1997f-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1997f-119">Request headers</span></span>

| <span data-ttu-id="1997f-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="1997f-120">Name</span></span>           | <span data-ttu-id="1997f-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="1997f-121">Type</span></span>    | <span data-ttu-id="1997f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="1997f-122">Description</span></span>|
|:---------------|:--------|:-----------|
| <span data-ttu-id="1997f-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="1997f-123">Authorization</span></span>  | <span data-ttu-id="1997f-124">string</span><span class="sxs-lookup"><span data-stu-id="1997f-124">string</span></span>  | <span data-ttu-id="1997f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1997f-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1997f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1997f-127">Request body</span></span>

<span data-ttu-id="1997f-128">En el cuerpo de la solicitud, proporcione el objeto [synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md) que se creará.</span><span class="sxs-lookup"><span data-stu-id="1997f-128">In the request body, supply the [synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md) object to be created.</span></span> <span data-ttu-id="1997f-129">El `id`, `applicationId` y `factoryTag` propiedades son necesarias.</span><span class="sxs-lookup"><span data-stu-id="1997f-129">The `id`, `applicationId` and `factoryTag` properties are required.</span></span> <span data-ttu-id="1997f-130">Cuando no `schema` es siempre con la plantilla, el esquema predeterminado asociado con el `factoryTag` (propiedad) que se usará.</span><span class="sxs-lookup"><span data-stu-id="1997f-130">When no `schema` is provided with the template, the default schema associated with the `factoryTag` property will be used.</span></span>

### <a name="response"></a><span data-ttu-id="1997f-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1997f-131">Response</span></span>

<span data-ttu-id="1997f-132">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1997f-132">If successful, this method returns a `201 Created` response code and a [synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md) object in the response body.</span></span>

### <a name="example"></a><span data-ttu-id="1997f-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1997f-133">Example</span></span>

##### <a name="request"></a><span data-ttu-id="1997f-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1997f-134">Request</span></span>
<span data-ttu-id="1997f-135">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="1997f-135">The following is an example of a request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_synchronizationtemplate_from_synchronization"
}-->
```http
POST https://graph.microsoft.com/beta/applications/{id}/synchronization/templates
Content-type: application/json

{ 
    "id": "SCIM-Test1",
    "applicationId": "{id}",
    "factoryTag": "CustomSCIM"
}
```

##### <a name="response"></a><span data-ttu-id="1997f-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1997f-136">Response</span></span>
<span data-ttu-id="1997f-137">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="1997f-137">The following is an example of a response.</span></span>
><span data-ttu-id="1997f-138">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="1997f-138">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="1997f-139">Se devolverán todas las propiedades en una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1997f-139">All the properties will be returned in an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.synchronizationTemplate"
} -->
```http
HTTP/1.1 201 Created

{
    "id": "SCIM-Test1",
    "applicationId": "{id}",
    "factoryTag": "CustomSCIM",
    "schema": {
        "directories": [],
        "synchronizationRules": []
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create synchronizationTemplate",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->