---
title: Lista de plantillas de sincronización existente
description: Las plantillas de sincronización asociadas con una aplicación determinada o una entidad de seguridad de servicio de la lista.
ms.openlocfilehash: 0842d5923368fa0df72af03e51d45dc3444e6dce
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088666"
---
# <a name="list-existing-synchronization-templates"></a><span data-ttu-id="d6bb8-103">Lista de plantillas de sincronización existente</span><span class="sxs-lookup"><span data-stu-id="d6bb8-103">List existing synchronization templates</span></span>

> <span data-ttu-id="d6bb8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d6bb8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d6bb8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d6bb8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d6bb8-106">Las plantillas de sincronización asociadas con una aplicación determinada o una entidad de seguridad de servicio de la lista.</span><span class="sxs-lookup"><span data-stu-id="d6bb8-106">List the synchronization templates associated with a given application or service principal.</span></span>

## <a name="permissions"></a><span data-ttu-id="d6bb8-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d6bb8-107">Permissions</span></span>
<span data-ttu-id="d6bb8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d6bb8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d6bb8-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d6bb8-110">Permission type</span></span>                        | <span data-ttu-id="d6bb8-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d6bb8-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="d6bb8-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d6bb8-112">Delegated (work or school account)</span></span>     |<span data-ttu-id="d6bb8-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d6bb8-113">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="d6bb8-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d6bb8-114">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="d6bb8-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d6bb8-115">Not supported.</span></span>|
|<span data-ttu-id="d6bb8-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d6bb8-116">Application</span></span>                            |<span data-ttu-id="d6bb8-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d6bb8-117">Not supported.</span></span>| 

### <a name="http-request"></a><span data-ttu-id="d6bb8-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d6bb8-118">HTTP Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET servicePrincipals/{id}/synchronization/templates
GET applications/{id}/synchronization/templates
```

## <a name="request-headers"></a><span data-ttu-id="d6bb8-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d6bb8-119">Request headers</span></span>

| <span data-ttu-id="d6bb8-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="d6bb8-120">Name</span></span>           | <span data-ttu-id="d6bb8-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6bb8-121">Type</span></span>    | <span data-ttu-id="d6bb8-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6bb8-122">Description</span></span>|
|:---------------|:--------|:-----------|
| <span data-ttu-id="d6bb8-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="d6bb8-123">Authorization</span></span>  | <span data-ttu-id="d6bb8-124">string</span><span class="sxs-lookup"><span data-stu-id="d6bb8-124">string</span></span>  | <span data-ttu-id="d6bb8-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d6bb8-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d6bb8-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d6bb8-127">Request body</span></span>

<span data-ttu-id="d6bb8-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d6bb8-128">Do not supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="d6bb8-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d6bb8-129">Response</span></span>

<span data-ttu-id="d6bb8-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y acollection de objetos [synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d6bb8-130">If successful, this method returns a `200 OK` response code and acollection of [synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md) objects in the response body.</span></span>

### <a name="example"></a><span data-ttu-id="d6bb8-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d6bb8-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="d6bb8-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d6bb8-132">Request</span></span>
<span data-ttu-id="d6bb8-133">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="d6bb8-133">The following is an example of a request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_synchronizationtemplate"
}-->
```http
GET https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/templates
```

##### <a name="response"></a><span data-ttu-id="d6bb8-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d6bb8-134">Response</span></span>
<span data-ttu-id="d6bb8-135">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="d6bb8-135">The following is an example of a response.</span></span>
><span data-ttu-id="d6bb8-136">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="d6bb8-136">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="d6bb8-137">Se devolverán todas las propiedades en una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d6bb8-137">All the properties will be returned in an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.synchronizationTemplate",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK

{
    "value": [
        {
            "id": "Slack",
            "factoryTag": "CustomSCIM",
            "schema": {
                    "directories": [],
                    "synchronizationRules": []
                    }
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get synchronizationTemplate",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->