---
title: List groups
description: Lista de todos los grupos disponibles en una organización, incluidos pero sin limitarse a ellos los grupos de Office 365.
ms.openlocfilehash: 15d39db7c3b5c322b90a7d7bbfc29ac4d2e81794
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030749"
---
# <a name="list-groups"></a><span data-ttu-id="6b2e0-103">Enumerar grupos</span><span class="sxs-lookup"><span data-stu-id="6b2e0-103">List groups</span></span>
<span data-ttu-id="6b2e0-p101">Lista de todos los grupos disponibles en una organización, incluidos pero sin limitarse a ellos los grupos de Office 365. Se devuelven las [propiedades predeterminadas](../api/group-get.md#default-properties) de cada grupo.</span><span class="sxs-lookup"><span data-stu-id="6b2e0-p101">List all the groups available in an organization, including but not limited to Office 365 Groups. The [default properties](../api/group-get.md#default-properties) of each group are returned.</span></span>

<span data-ttu-id="6b2e0-106">Para enumerar únicamente grupos de Office 365 (también denominados grupos unificados), aplique un filtro en **groupTypes**:</span><span class="sxs-lookup"><span data-stu-id="6b2e0-106">To list only Office 365 Groups (aka unified groups), apply a filter on **groupTypes**:</span></span>
```
GET https://graph.microsoft.com/v1.0/groups?$filter=groupTypes/any(c:c+eq+'Unified')
```

<span data-ttu-id="6b2e0-107">Puede usar la opción de consulta de OData `$orderby` para ordenar grupos de una organización por el valor **displayName**, tal y como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6b2e0-107">You can use the OData query option `$orderby` to sort groups in an organization by the **displayName** values, as shown in the following example:</span></span>
```
GET https://graph.microsoft.com/v1.0/groups?$orderby=displayName
```

## <a name="permissions"></a><span data-ttu-id="6b2e0-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="6b2e0-108">Permissions</span></span>
<span data-ttu-id="6b2e0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6b2e0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6b2e0-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6b2e0-111">Permission type</span></span>      | <span data-ttu-id="6b2e0-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6b2e0-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6b2e0-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6b2e0-113">Delegated (work or school account)</span></span> | <span data-ttu-id="6b2e0-114">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6b2e0-114">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="6b2e0-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6b2e0-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6b2e0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6b2e0-116">Not supported.</span></span>    |
|<span data-ttu-id="6b2e0-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6b2e0-117">Application</span></span> | <span data-ttu-id="6b2e0-118">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6b2e0-118">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6b2e0-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6b2e0-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups
```

## <a name="optional-query-parameters"></a><span data-ttu-id="6b2e0-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6b2e0-120">Optional query parameters</span></span>
<span data-ttu-id="6b2e0-121">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6b2e0-121">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="6b2e0-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6b2e0-122">Request headers</span></span>
| <span data-ttu-id="6b2e0-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="6b2e0-123">Name</span></span>       | <span data-ttu-id="6b2e0-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="6b2e0-124">Type</span></span> | <span data-ttu-id="6b2e0-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b2e0-125">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="6b2e0-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="6b2e0-126">Authorization</span></span>  | <span data-ttu-id="6b2e0-127">string</span><span class="sxs-lookup"><span data-stu-id="6b2e0-127">string</span></span>  | <span data-ttu-id="6b2e0-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6b2e0-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6b2e0-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6b2e0-130">Request body</span></span>
<span data-ttu-id="6b2e0-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6b2e0-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6b2e0-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6b2e0-132">Response</span></span>
<span data-ttu-id="6b2e0-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [group](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6b2e0-133">If successful, this method returns a `200 OK` response code and collection of [group](../resources/group.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6b2e0-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6b2e0-134">Example</span></span>
#### <a name="request"></a><span data-ttu-id="6b2e0-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6b2e0-135">Request</span></span>
<span data-ttu-id="6b2e0-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6b2e0-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_groups"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups
```

#### <a name="response"></a><span data-ttu-id="6b2e0-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6b2e0-137">Response</span></span>
<span data-ttu-id="6b2e0-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6b2e0-138">The following is an example of the response.</span></span>

><span data-ttu-id="6b2e0-139">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="6b2e0-139">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="6b2e0-140">Se devolverán las [propiedades predeterminadas](../api/group-get.md#default-properties) de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6b2e0-140">The [default properties](../api/group-get.md#default-properties) will be returned from an actual call.</span></span>

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