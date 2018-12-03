---
title: Mostrar groupLifecyclePolicies
description: Recupera una lista de objetos groupLifecyclePolicy a la que pertenece un grupo.
ms.openlocfilehash: c3045b39df0b50bfd8f69bac386d336930a55492
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029534"
---
# <a name="list-grouplifecyclepolicies"></a><span data-ttu-id="a53c0-103">Mostrar groupLifecyclePolicies</span><span class="sxs-lookup"><span data-stu-id="a53c0-103">List groupLifecyclePolicies</span></span>

<span data-ttu-id="a53c0-104">Recupera una lista de objetos [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) a la que pertenece un grupo.</span><span class="sxs-lookup"><span data-stu-id="a53c0-104">Retrieves a list of [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) objects to which a group belongs.</span></span>

## <a name="permissions"></a><span data-ttu-id="a53c0-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="a53c0-105">Permissions</span></span>

<span data-ttu-id="a53c0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a53c0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a53c0-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a53c0-108">Permission type</span></span>      | <span data-ttu-id="a53c0-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a53c0-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a53c0-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a53c0-110">Delegated (work or school account)</span></span> | <span data-ttu-id="a53c0-111">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="a53c0-111">Directory.Read.All</span></span>    |
|<span data-ttu-id="a53c0-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a53c0-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a53c0-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a53c0-113">Not supported.</span></span>    |
|<span data-ttu-id="a53c0-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a53c0-114">Application</span></span> | <span data-ttu-id="a53c0-115">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="a53c0-115">Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a53c0-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a53c0-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/groupLifecyclePolicies
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a53c0-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a53c0-117">Optional query parameters</span></span>
<span data-ttu-id="a53c0-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a53c0-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a53c0-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a53c0-119">Request headers</span></span>
| <span data-ttu-id="a53c0-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="a53c0-120">Name</span></span> | <span data-ttu-id="a53c0-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="a53c0-121">Description</span></span> |
|:----------|:----------|
| <span data-ttu-id="a53c0-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="a53c0-122">Authorization</span></span> | <span data-ttu-id="a53c0-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a53c0-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a53c0-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a53c0-125">Request body</span></span>
<span data-ttu-id="a53c0-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a53c0-126">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="a53c0-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a53c0-127">Response</span></span>
<span data-ttu-id="a53c0-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a53c0-128">If successful, this method returns a `200 OK` response code and collection of [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a53c0-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a53c0-129">Example</span></span>

##### <a name="request"></a><span data-ttu-id="a53c0-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a53c0-130">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_grouplifecyclepolicies"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/groupLifecyclePolicies
```
##### <a name="response"></a><span data-ttu-id="a53c0-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a53c0-131">Response</span></span>

<span data-ttu-id="a53c0-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a53c0-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupLifecyclePolicy",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 222

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