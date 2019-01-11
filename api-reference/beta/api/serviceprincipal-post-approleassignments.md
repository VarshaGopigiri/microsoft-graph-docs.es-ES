---
title: Crear appRoleAssignment
description: Utilice esta API para crear un nuevo appRoleAssignment.
localization_priority: Normal
ms.openlocfilehash: ce498312f294ff11b97f12b136a6f48ebb4d3791
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27886985"
---
# <a name="create-approleassignment"></a><span data-ttu-id="77a67-103">Crear appRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="77a67-103">Create appRoleAssignment</span></span>

> <span data-ttu-id="77a67-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="77a67-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="77a67-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="77a67-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="77a67-106">Utilice esta API para crear un nuevo appRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="77a67-106">Use this API to create a new appRoleAssignment.</span></span>

## <a name="permissions"></a><span data-ttu-id="77a67-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="77a67-107">Permissions</span></span>
<span data-ttu-id="77a67-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="77a67-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="77a67-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="77a67-110">Permission type</span></span>      | <span data-ttu-id="77a67-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="77a67-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="77a67-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="77a67-112">Delegated (work or school account)</span></span> | <span data-ttu-id="77a67-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="77a67-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="77a67-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="77a67-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="77a67-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="77a67-115">Not supported.</span></span>    |
|<span data-ttu-id="77a67-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="77a67-116">Application</span></span> | <span data-ttu-id="77a67-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="77a67-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="77a67-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="77a67-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /servicePrincipals/{id}/appRoleAssignments

```
## <a name="request-headers"></a><span data-ttu-id="77a67-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="77a67-119">Request headers</span></span>
| <span data-ttu-id="77a67-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="77a67-120">Name</span></span>       | <span data-ttu-id="77a67-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="77a67-121">Type</span></span> | <span data-ttu-id="77a67-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="77a67-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="77a67-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="77a67-123">Authorization</span></span>  | <span data-ttu-id="77a67-124">string</span><span class="sxs-lookup"><span data-stu-id="77a67-124">string</span></span>  | <span data-ttu-id="77a67-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="77a67-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="77a67-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="77a67-127">Request body</span></span>
<span data-ttu-id="77a67-128">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [appRoleAssignment](../resources/approleassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="77a67-128">In the request body, supply a JSON representation of [appRoleAssignment](../resources/approleassignment.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="77a67-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77a67-129">Response</span></span>

<span data-ttu-id="77a67-130">Si tiene éxito, este método devuelve `201 Created` objeto de código y [appRoleAssignment](../resources/approleassignment.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77a67-130">If successful, this method returns `201 Created` response code and [appRoleAssignment](../resources/approleassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="77a67-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="77a67-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="77a67-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="77a67-132">Request</span></span>
<span data-ttu-id="77a67-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="77a67-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_approleassignment_from_serviceprincipal"
}-->
```http
POST https://graph.microsoft.com/beta/servicePrincipals/{id}/appRoleAssignments
Content-type: application/json
Content-length: 233

{
  "creationTimestamp": "2016-10-19T10:37:00Z",
  "principalDisplayName": "principalDisplayName-value",
  "principalId": "principalId-value",
  "principalType": "principalType-value",
  "resourceDisplayName": "resourceDisplayName-value"
}
```
<span data-ttu-id="77a67-134">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [appRoleAssignment](../resources/approleassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="77a67-134">In the request body, supply a JSON representation of [appRoleAssignment](../resources/approleassignment.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="77a67-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77a67-135">Response</span></span>
<span data-ttu-id="77a67-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="77a67-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.approleassignment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 253

{
  "creationTimestamp": "2016-10-19T10:37:00Z",
  "id": "id-value",
  "principalDisplayName": "principalDisplayName-value",
  "principalId": "principalId-value",
  "principalType": "principalType-value",
  "resourceDisplayName": "resourceDisplayName-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create appRoleAssignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
