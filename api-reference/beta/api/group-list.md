---
title: List groups
description: Lista de todos los grupos disponibles en una organización, incluidos pero sin limitarse a ellos los grupos de Office 365.
localization_priority: Priority
ms.openlocfilehash: dd243d1f07b98564bb5aa4751664337c0f0654cc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27813275"
---
# <a name="list-groups"></a><span data-ttu-id="9d2e9-103">Enumerar grupos</span><span class="sxs-lookup"><span data-stu-id="9d2e9-103">List groups</span></span>

> <span data-ttu-id="9d2e9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9d2e9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9d2e9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9d2e9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9d2e9-p102">Lista de todos los grupos disponibles en una organización, incluidos pero sin limitarse a ellos los grupos de Office 365. Se devuelven las [propiedades predeterminadas](../api/group-get.md#default-properties) de cada grupo.</span><span class="sxs-lookup"><span data-stu-id="9d2e9-p102">List all the groups available in an organization, including but not limited to Office 365 Groups. The [default properties](../api/group-get.md#default-properties) of each group are returned.</span></span>

<span data-ttu-id="9d2e9-108">Para enumerar únicamente grupos de Office 365 (también denominados grupos unificados), aplique un filtro en **groupTypes**:</span><span class="sxs-lookup"><span data-stu-id="9d2e9-108">To list only Office 365 Groups (aka unified groups), apply a filter on **groupTypes**:</span></span>
```
GET https://graph.microsoft.com/beta/groups?$filter=groupTypes/any(c:c+eq+'Unified')
```

<span data-ttu-id="9d2e9-109">Puede usar la opción de consulta de OData `$orderby` para ordenar grupos de una organización por el valor **displayName**, tal y como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9d2e9-109">You can use the OData query option `$orderby` to sort groups in an organization by the **displayName** values, as shown in the following example:</span></span>
```
GET https://graph.microsoft.com/beta/groups?$orderby=displayName
```

<span data-ttu-id="9d2e9-110">Para devolver los grupos que contienen a miembros con errores de licencia, use el parámetro de consulta **$filter** :</span><span class="sxs-lookup"><span data-stu-id="9d2e9-110">To return groups containing members with license errors, use the **$filter** query parameter:</span></span> 

```http 
GET https://graph.microsoft.com/beta/groups?$filter=hasMembersWithLicenseErrors+eq+true 
```
## <a name="permissions"></a><span data-ttu-id="9d2e9-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="9d2e9-111">Permissions</span></span>
<span data-ttu-id="9d2e9-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9d2e9-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9d2e9-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9d2e9-114">Permission type</span></span>      | <span data-ttu-id="9d2e9-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9d2e9-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9d2e9-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9d2e9-116">Delegated (work or school account)</span></span> | <span data-ttu-id="9d2e9-117">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9d2e9-117">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="9d2e9-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9d2e9-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9d2e9-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9d2e9-119">Not supported.</span></span>    |
|<span data-ttu-id="9d2e9-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9d2e9-120">Application</span></span> | <span data-ttu-id="9d2e9-121">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9d2e9-121">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9d2e9-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9d2e9-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups
```

## <a name="optional-query-parameters"></a><span data-ttu-id="9d2e9-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9d2e9-123">Optional query parameters</span></span>
<span data-ttu-id="9d2e9-124">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9d2e9-124">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="9d2e9-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9d2e9-125">Request headers</span></span>
| <span data-ttu-id="9d2e9-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="9d2e9-126">Name</span></span>       | <span data-ttu-id="9d2e9-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d2e9-127">Type</span></span> | <span data-ttu-id="9d2e9-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d2e9-128">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="9d2e9-129">Autorización</span><span class="sxs-lookup"><span data-stu-id="9d2e9-129">Authorization</span></span>  | <span data-ttu-id="9d2e9-130">string</span><span class="sxs-lookup"><span data-stu-id="9d2e9-130">string</span></span>  | <span data-ttu-id="9d2e9-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9d2e9-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9d2e9-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9d2e9-133">Request body</span></span>
<span data-ttu-id="9d2e9-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9d2e9-134">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9d2e9-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9d2e9-135">Response</span></span>
<span data-ttu-id="9d2e9-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [group](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9d2e9-136">If successful, this method returns a `200 OK` response code and collection of [group](../resources/group.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9d2e9-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9d2e9-137">Example</span></span>
#### <a name="request"></a><span data-ttu-id="9d2e9-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9d2e9-138">Request</span></span>
<span data-ttu-id="9d2e9-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9d2e9-139">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_groups"
}-->
```http
GET https://graph.microsoft.com/beta/groups
```

#### <a name="response"></a><span data-ttu-id="9d2e9-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9d2e9-140">Response</span></span>
<span data-ttu-id="9d2e9-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9d2e9-141">The following is an example of the response.</span></span>
><span data-ttu-id="9d2e9-142">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="9d2e9-142">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="9d2e9-143">Se devolverán las [propiedades predeterminadas](../api/group-get.md#default-properties) de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9d2e9-143">The [default properties](../api/group-get.md#default-properties) will be returned from an actual call.</span></span>

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
