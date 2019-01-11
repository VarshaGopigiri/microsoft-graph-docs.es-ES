---
title: Mostrar groupLifecyclePolicies
description: Recupera una lista de objetos groupLifecyclePolicy a la que pertenece un grupo.
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: 1b9559078e7859dc8b90240e513a8f4e03bccb69
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27883226"
---
# <a name="list-grouplifecyclepolicies"></a><span data-ttu-id="1a9d6-103">Mostrar groupLifecyclePolicies</span><span class="sxs-lookup"><span data-stu-id="1a9d6-103">List groupLifecyclePolicies</span></span>

> <span data-ttu-id="1a9d6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1a9d6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1a9d6-106">Recupera una lista de objetos [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) a la que pertenece un grupo.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-106">Retrieves a list of [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) objects to which a group belongs.</span></span>

## <a name="permissions"></a><span data-ttu-id="1a9d6-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="1a9d6-107">Permissions</span></span>

<span data-ttu-id="1a9d6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1a9d6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1a9d6-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1a9d6-110">Permission type</span></span>      | <span data-ttu-id="1a9d6-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1a9d6-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1a9d6-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1a9d6-112">Delegated (work or school account)</span></span> | <span data-ttu-id="1a9d6-113">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="1a9d6-113">Directory.Read.All</span></span>    |
|<span data-ttu-id="1a9d6-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1a9d6-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1a9d6-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-115">Not supported.</span></span>    |
|<span data-ttu-id="1a9d6-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1a9d6-116">Application</span></span> | <span data-ttu-id="1a9d6-117">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="1a9d6-117">Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="1a9d6-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1a9d6-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/groupLifecyclePolicies
```
## <a name="optional-query-parameters"></a><span data-ttu-id="1a9d6-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1a9d6-119">Optional query parameters</span></span>
<span data-ttu-id="1a9d6-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="1a9d6-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1a9d6-121">Request headers</span></span>
| <span data-ttu-id="1a9d6-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="1a9d6-122">Name</span></span> | <span data-ttu-id="1a9d6-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="1a9d6-123">Description</span></span> |
|:----------|:----------|
| <span data-ttu-id="1a9d6-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="1a9d6-124">Authorization</span></span> | <span data-ttu-id="1a9d6-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1a9d6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1a9d6-127">Request body</span></span>
<span data-ttu-id="1a9d6-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="1a9d6-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1a9d6-129">Response</span></span>
<span data-ttu-id="1a9d6-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-130">If successful, this method returns a `200 OK` response code and collection of [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="1a9d6-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1a9d6-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="1a9d6-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1a9d6-132">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_grouplifecyclepolicies"
}-->
```http
GET https://graph.microsoft.com/beta/groups/{id}/groupLifecyclePolicies
```
##### <a name="response"></a><span data-ttu-id="1a9d6-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1a9d6-133">Response</span></span>

<span data-ttu-id="1a9d6-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupLifecyclePolicy",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 227

{
  "value": [
    {
      "id": "ffffffff-ffff-ffff-ffff-ffffffffffff",
      "groupLifetimeInDays": 90,
      "managedGroupTypes": "Selected",
      "alternateNotificationEmails": "admin@contoso.com"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List groupLifecyclePolicies",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
