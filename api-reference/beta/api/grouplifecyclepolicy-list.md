---
title: Mostrar groupLifecyclePolicies
description: Muestra todos los objetos groupLifecyclePolicies.
ms.openlocfilehash: 31ca45613fb47f7aa4f7430432b28bfd0469c7eb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083564"
---
# <a name="list-grouplifecyclepolicies"></a><span data-ttu-id="21a1b-103">Mostrar groupLifecyclePolicies</span><span class="sxs-lookup"><span data-stu-id="21a1b-103">List groupLifecyclePolicies</span></span>

> <span data-ttu-id="21a1b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="21a1b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="21a1b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="21a1b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="21a1b-106">Muestra todos los objetos [groupLifecyclePolicies](../resources/grouplifecyclepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="21a1b-106">List all the [groupLifecyclePolicies](../resources/grouplifecyclepolicy.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="21a1b-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="21a1b-107">Permissions</span></span>

<span data-ttu-id="21a1b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="21a1b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="21a1b-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="21a1b-110">Permission type</span></span>      | <span data-ttu-id="21a1b-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="21a1b-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="21a1b-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="21a1b-112">Delegated (work or school account)</span></span> | <span data-ttu-id="21a1b-113">Directory.Read.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="21a1b-113">Directory.Read.All or Directory.ReadWrite.All</span></span> |
|<span data-ttu-id="21a1b-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="21a1b-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="21a1b-115">No admitido</span><span class="sxs-lookup"><span data-stu-id="21a1b-115">Not supported</span></span> |
|<span data-ttu-id="21a1b-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="21a1b-116">Application</span></span> | <span data-ttu-id="21a1b-117">Directory.Read.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="21a1b-117">Directory.Read.All or Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="21a1b-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="21a1b-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groupLifecyclePolicies
```
## <a name="optional-query-parameters"></a><span data-ttu-id="21a1b-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="21a1b-119">Optional query parameters</span></span>
<span data-ttu-id="21a1b-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="21a1b-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="21a1b-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="21a1b-121">Request headers</span></span>
| <span data-ttu-id="21a1b-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="21a1b-122">Name</span></span> | <span data-ttu-id="21a1b-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="21a1b-123">Description</span></span> |
|:----------|:----------|
| <span data-ttu-id="21a1b-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="21a1b-124">Authorization</span></span> | <span data-ttu-id="21a1b-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="21a1b-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="21a1b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="21a1b-127">Request body</span></span>
<span data-ttu-id="21a1b-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="21a1b-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="21a1b-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21a1b-129">Response</span></span>

<span data-ttu-id="21a1b-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="21a1b-130">If successful, this method returns a `200 OK` response code and a collection of [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="21a1b-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="21a1b-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="21a1b-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="21a1b-132">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_grouplifecyclepolicy"
}-->
```http
GET https://graph.microsoft.com/beta/groupLifecyclePolicies
```
##### <a name="response"></a><span data-ttu-id="21a1b-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21a1b-133">Response</span></span>

<span data-ttu-id="21a1b-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="21a1b-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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