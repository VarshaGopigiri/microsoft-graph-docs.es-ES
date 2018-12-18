---
title: Mostrar groupLifecyclePolicies
description: Muestra todos los objetos groupLifecyclePolicies.
author: dkershaw10
ms.openlocfilehash: e926d071121986e1aa06511ef8ec84e6b0cd55b8
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27350333"
---
# <a name="list-grouplifecyclepolicies"></a><span data-ttu-id="30805-103">Mostrar groupLifecyclePolicies</span><span class="sxs-lookup"><span data-stu-id="30805-103">List groupLifecyclePolicies</span></span>

> <span data-ttu-id="30805-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="30805-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="30805-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="30805-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="30805-106">Muestra todos los objetos [groupLifecyclePolicies](../resources/grouplifecyclepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="30805-106">List all the [groupLifecyclePolicies](../resources/grouplifecyclepolicy.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="30805-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="30805-107">Permissions</span></span>

<span data-ttu-id="30805-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="30805-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="30805-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="30805-110">Permission type</span></span>      | <span data-ttu-id="30805-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="30805-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="30805-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="30805-112">Delegated (work or school account)</span></span> | <span data-ttu-id="30805-113">Directory.Read.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="30805-113">Directory.Read.All or Directory.ReadWrite.All</span></span> |
|<span data-ttu-id="30805-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="30805-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="30805-115">No admitido</span><span class="sxs-lookup"><span data-stu-id="30805-115">Not supported</span></span> |
|<span data-ttu-id="30805-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="30805-116">Application</span></span> | <span data-ttu-id="30805-117">Directory.Read.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="30805-117">Directory.Read.All or Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="30805-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="30805-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groupLifecyclePolicies
```
## <a name="optional-query-parameters"></a><span data-ttu-id="30805-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="30805-119">Optional query parameters</span></span>
<span data-ttu-id="30805-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="30805-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="30805-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="30805-121">Request headers</span></span>
| <span data-ttu-id="30805-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="30805-122">Name</span></span> | <span data-ttu-id="30805-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="30805-123">Description</span></span> |
|:----------|:----------|
| <span data-ttu-id="30805-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="30805-124">Authorization</span></span> | <span data-ttu-id="30805-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="30805-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="30805-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="30805-127">Request body</span></span>
<span data-ttu-id="30805-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="30805-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="30805-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30805-129">Response</span></span>

<span data-ttu-id="30805-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="30805-130">If successful, this method returns a `200 OK` response code and a collection of [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="30805-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="30805-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="30805-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="30805-132">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_grouplifecyclepolicy"
}-->
```http
GET https://graph.microsoft.com/beta/groupLifecyclePolicies
```
##### <a name="response"></a><span data-ttu-id="30805-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30805-133">Response</span></span>

<span data-ttu-id="30805-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="30805-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupLifecyclePolicy",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 223

{
  "value": [
    {
      "id": "ffffffff-ffff-ffff-ffff-ffffffffffff",
      "groupLifetimeInDays": 100,
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