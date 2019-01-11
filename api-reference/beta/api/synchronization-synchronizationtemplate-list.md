---
title: Lista de plantillas de sincronización existente
description: Las plantillas de sincronización asociadas con una aplicación determinada o una entidad de seguridad de servicio de la lista.
localization_priority: Normal
ms.openlocfilehash: 49e9e257322886fe294807207276f8b6d6919909
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27839441"
---
# <a name="list-existing-synchronization-templates"></a><span data-ttu-id="b1def-103">Lista de plantillas de sincronización existente</span><span class="sxs-lookup"><span data-stu-id="b1def-103">List existing synchronization templates</span></span>

> <span data-ttu-id="b1def-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b1def-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b1def-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b1def-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b1def-106">Las plantillas de sincronización asociadas con una aplicación determinada o una entidad de seguridad de servicio de la lista.</span><span class="sxs-lookup"><span data-stu-id="b1def-106">List the synchronization templates associated with a given application or service principal.</span></span>

## <a name="permissions"></a><span data-ttu-id="b1def-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b1def-107">Permissions</span></span>
<span data-ttu-id="b1def-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b1def-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b1def-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b1def-110">Permission type</span></span>                        | <span data-ttu-id="b1def-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b1def-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="b1def-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b1def-112">Delegated (work or school account)</span></span>     |<span data-ttu-id="b1def-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b1def-113">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="b1def-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b1def-114">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="b1def-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b1def-115">Not supported.</span></span>|
|<span data-ttu-id="b1def-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b1def-116">Application</span></span>                            |<span data-ttu-id="b1def-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b1def-117">Not supported.</span></span>| 

### <a name="http-request"></a><span data-ttu-id="b1def-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b1def-118">HTTP Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET servicePrincipals/{id}/synchronization/templates
GET applications/{id}/synchronization/templates
```

## <a name="request-headers"></a><span data-ttu-id="b1def-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b1def-119">Request headers</span></span>

| <span data-ttu-id="b1def-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="b1def-120">Name</span></span>           | <span data-ttu-id="b1def-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1def-121">Type</span></span>    | <span data-ttu-id="b1def-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1def-122">Description</span></span>|
|:---------------|:--------|:-----------|
| <span data-ttu-id="b1def-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="b1def-123">Authorization</span></span>  | <span data-ttu-id="b1def-124">string</span><span class="sxs-lookup"><span data-stu-id="b1def-124">string</span></span>  | <span data-ttu-id="b1def-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b1def-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b1def-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b1def-127">Request body</span></span>

<span data-ttu-id="b1def-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b1def-128">Do not supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="b1def-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b1def-129">Response</span></span>

<span data-ttu-id="b1def-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y acollection de objetos [synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b1def-130">If successful, this method returns a `200 OK` response code and acollection of [synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md) objects in the response body.</span></span>

### <a name="example"></a><span data-ttu-id="b1def-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b1def-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="b1def-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b1def-132">Request</span></span>
<span data-ttu-id="b1def-133">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="b1def-133">The following is an example of a request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_synchronizationtemplate"
}-->
```http
GET https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/templates
```

##### <a name="response"></a><span data-ttu-id="b1def-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b1def-134">Response</span></span>
<span data-ttu-id="b1def-135">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="b1def-135">The following is an example of a response.</span></span>
><span data-ttu-id="b1def-136">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="b1def-136">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="b1def-137">Se devolverán todas las propiedades en una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b1def-137">All the properties will be returned in an actual call.</span></span>
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
