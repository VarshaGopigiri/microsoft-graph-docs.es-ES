---
title: List groups
description: Lista de todos los grupos disponibles en una organización, incluidos pero sin limitarse a ellos los grupos de Office 365.
localization_priority: Priority
author: dkershaw10
ms.prod: groups
ms.openlocfilehash: 05d3872fbc376933a0ff2fe772a79239e4d62928
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27955173"
---
# <a name="list-groups"></a><span data-ttu-id="c6507-103">Enumerar grupos</span><span class="sxs-lookup"><span data-stu-id="c6507-103">List groups</span></span>
<span data-ttu-id="c6507-p101">Lista de todos los grupos disponibles en una organización, incluidos pero sin limitarse a ellos los grupos de Office 365. Se devuelven las [propiedades predeterminadas](../api/group-get.md#default-properties) de cada grupo.</span><span class="sxs-lookup"><span data-stu-id="c6507-p101">List all the groups available in an organization, including but not limited to Office 365 Groups. The [default properties](../api/group-get.md#default-properties) of each group are returned.</span></span>

<span data-ttu-id="c6507-106">Para enumerar únicamente grupos de Office 365 (también denominados grupos unificados), aplique un filtro en **groupTypes**:</span><span class="sxs-lookup"><span data-stu-id="c6507-106">To list only Office 365 Groups (aka unified groups), apply a filter on **groupTypes**:</span></span>
```
GET https://graph.microsoft.com/v1.0/groups?$filter=groupTypes/any(c:c+eq+'Unified')
```

<span data-ttu-id="c6507-107">Puede usar la opción de consulta de OData `$orderby` para ordenar grupos de una organización por el valor **displayName**, tal y como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c6507-107">You can use the OData query option `$orderby` to sort groups in an organization by the **displayName** values, as shown in the following example:</span></span>
```
GET https://graph.microsoft.com/v1.0/groups?$orderby=displayName
```

## <a name="permissions"></a><span data-ttu-id="c6507-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="c6507-108">Permissions</span></span>
<span data-ttu-id="c6507-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c6507-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c6507-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c6507-111">Permission type</span></span>      | <span data-ttu-id="c6507-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c6507-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c6507-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c6507-113">Delegated (work or school account)</span></span> | <span data-ttu-id="c6507-114">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c6507-114">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="c6507-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c6507-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c6507-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c6507-116">Not supported.</span></span>    |
|<span data-ttu-id="c6507-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c6507-117">Application</span></span> | <span data-ttu-id="c6507-118">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c6507-118">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c6507-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c6507-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups
```

## <a name="optional-query-parameters"></a><span data-ttu-id="c6507-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c6507-120">Optional query parameters</span></span>
<span data-ttu-id="c6507-121">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c6507-121">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="c6507-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c6507-122">Request headers</span></span>
| <span data-ttu-id="c6507-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="c6507-123">Name</span></span>       | <span data-ttu-id="c6507-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="c6507-124">Type</span></span> | <span data-ttu-id="c6507-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6507-125">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="c6507-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="c6507-126">Authorization</span></span>  | <span data-ttu-id="c6507-127">string</span><span class="sxs-lookup"><span data-stu-id="c6507-127">string</span></span>  | <span data-ttu-id="c6507-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c6507-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c6507-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c6507-130">Request body</span></span>
<span data-ttu-id="c6507-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c6507-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c6507-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6507-132">Response</span></span>
<span data-ttu-id="c6507-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [group](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c6507-133">If successful, this method returns a `200 OK` response code and collection of [group](../resources/group.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c6507-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6507-134">Example</span></span>
#### <a name="request"></a><span data-ttu-id="c6507-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c6507-135">Request</span></span>
<span data-ttu-id="c6507-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c6507-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_groups"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups
```

#### <a name="response"></a><span data-ttu-id="c6507-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6507-137">Response</span></span>
<span data-ttu-id="c6507-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c6507-138">The following is an example of the response.</span></span>

><span data-ttu-id="c6507-139">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="c6507-139">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="c6507-140">Se devolverán las [propiedades predeterminadas](../api/group-get.md#default-properties) de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c6507-140">The [default properties](../api/group-get.md#default-properties) will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: xxx

 {
  "value": [
    {
      "id": "id-value",
      "description": "description-value",
      "displayName": "displayName-value",
      "groupTypes": [
        "groupTypes-value"
      ],
      "mail": "mail-value",
      "mailEnabled": true,
      "mailNickname": "mailNickname-value",
      "onPremisesLastSyncDateTime": "onPremisesLastSyncDateTime-value",
      "onPremisesSecurityIdentifier": "onPremisesSecurityIdentifier-value",
      "onPremisesSyncEnabled": true,
      "proxyAddresses": [
        "proxyAddresses-value"
      ],
      "securityEnabled": true,
      "visibility": "visibility-value"
    }
  ]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List groups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
