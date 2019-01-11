---
title: Obtener groupLifecyclePolicy
description: Recupera las propiedades y relaciones de un objeto groupLifecyclePolicies.
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: 0908fea443fbe52185fc3bc2a759cd62cebfa511
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27874686"
---
# <a name="get-grouplifecyclepolicy"></a><span data-ttu-id="2c5af-103">Obtener groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="2c5af-103">Get groupLifecyclePolicy</span></span>

<span data-ttu-id="2c5af-104">Recupera las propiedades y relaciones de un objeto [groupLifecyclePolicies](../resources/grouplifecyclepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2c5af-104">Retrieve the properties and relationships of a [groupLifecyclePolicies](../resources/grouplifecyclepolicy.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="2c5af-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="2c5af-105">Permissions</span></span>

<span data-ttu-id="2c5af-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2c5af-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2c5af-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2c5af-108">Permission type</span></span>      | <span data-ttu-id="2c5af-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2c5af-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2c5af-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2c5af-110">Delegated (work or school account)</span></span> | <span data-ttu-id="2c5af-111">Directory.Read.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2c5af-111">Directory.Read.All or Directory.ReadWrite.All</span></span> |
|<span data-ttu-id="2c5af-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2c5af-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2c5af-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2c5af-113">Not supported.</span></span>    |
|<span data-ttu-id="2c5af-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2c5af-114">Application</span></span> | <span data-ttu-id="2c5af-115">Directory.Read.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2c5af-115">Directory.Read.All or Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="2c5af-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2c5af-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groupLifecyclePolicies/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="2c5af-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="2c5af-117">Optional query parameters</span></span>
<span data-ttu-id="2c5af-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c5af-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="2c5af-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2c5af-119">Request headers</span></span>
| <span data-ttu-id="2c5af-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="2c5af-120">Name</span></span> | <span data-ttu-id="2c5af-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c5af-121">Description</span></span> |
|:----------|:----------|
| <span data-ttu-id="2c5af-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="2c5af-122">Authorization</span></span> | <span data-ttu-id="2c5af-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2c5af-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2c5af-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2c5af-125">Request body</span></span>
<span data-ttu-id="2c5af-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2c5af-126">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="2c5af-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c5af-127">Response</span></span>
<span data-ttu-id="2c5af-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c5af-128">If successful, this method returns a `200 OK` response code and [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="2c5af-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2c5af-129">Example</span></span>

##### <a name="request"></a><span data-ttu-id="2c5af-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2c5af-130">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_grouplifecyclepolicy"
}-->
```http
GET https://graph.microsoft.com/v1.0/groupLifecyclePolicies/{id}
```
##### <a name="response"></a><span data-ttu-id="2c5af-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c5af-131">Response</span></span>

<span data-ttu-id="2c5af-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2c5af-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupLifecyclePolicy"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 174

{
  "id": "ffffffff-ffff-ffff-ffff-ffffffffffff",
  "groupLifetimeInDays": 100,
  "managedGroupTypes": "Selected",
  "alternateNotificationEmails": "admin@contoso.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get groupLifecyclePolicy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
