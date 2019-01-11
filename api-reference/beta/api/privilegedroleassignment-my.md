---
title: 'privilegedRoleAssignment: Mi'
description: Obtener las asignaciones de roles con privilegios del solicitante.
localization_priority: Normal
ms.openlocfilehash: fca950413d2f0a50b6ea9e09b859d2ecf926261b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27840260"
---
# <a name="privilegedroleassignment-my"></a><span data-ttu-id="fdd10-103">privilegedRoleAssignment: Mi</span><span class="sxs-lookup"><span data-stu-id="fdd10-103">privilegedRoleAssignment: my</span></span>

> <span data-ttu-id="fdd10-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fdd10-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fdd10-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fdd10-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fdd10-106">Obtener las asignaciones de roles con privilegios del solicitante.</span><span class="sxs-lookup"><span data-stu-id="fdd10-106">Get the requestor's privileged role assignments.</span></span>

## <a name="permissions"></a><span data-ttu-id="fdd10-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="fdd10-107">Permissions</span></span>
<span data-ttu-id="fdd10-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fdd10-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fdd10-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fdd10-110">Permission type</span></span>      | <span data-ttu-id="fdd10-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fdd10-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fdd10-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fdd10-112">Delegated (work or school account)</span></span> | <span data-ttu-id="fdd10-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="fdd10-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="fdd10-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fdd10-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fdd10-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fdd10-115">Not supported.</span></span>    |
|<span data-ttu-id="fdd10-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fdd10-116">Application</span></span> | <span data-ttu-id="fdd10-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fdd10-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="fdd10-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fdd10-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedRoleAssignments/my
```
## <a name="request-headers"></a><span data-ttu-id="fdd10-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fdd10-119">Request headers</span></span>
| <span data-ttu-id="fdd10-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="fdd10-120">Name</span></span>       | <span data-ttu-id="fdd10-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="fdd10-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="fdd10-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="fdd10-122">Authorization</span></span>  | <span data-ttu-id="fdd10-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fdd10-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="fdd10-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fdd10-125">Request body</span></span>
<span data-ttu-id="fdd10-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fdd10-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fdd10-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fdd10-127">Response</span></span>

<span data-ttu-id="fdd10-128">Si tiene éxito, este método devuelve `200 OK` objeto de colección de respuesta código y [privilegedRoleAssignment](../resources/privilegedroleassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fdd10-128">If successful, this method returns `200 OK` response code and [privilegedRoleAssignment](../resources/privilegedroleassignment.md) collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fdd10-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fdd10-129">Example</span></span>
<span data-ttu-id="fdd10-130">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="fdd10-130">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="fdd10-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fdd10-131">Request</span></span>
<span data-ttu-id="fdd10-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fdd10-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "privilegedroleassignment_my"
}-->
```http
GET https://graph.microsoft.com/beta/privilegedRoleAssignments/my
```

##### <a name="response"></a><span data-ttu-id="fdd10-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fdd10-133">Response</span></span>
<span data-ttu-id="fdd10-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fdd10-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedRoleAssignment",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 237

{
  "value": [
    {
      "id": "id-value",
      "userId": "userId-value",
      "roleId": "roleId-value",
      "isElevated": true,
      "expirationDateTime": "2016-10-19T10:37:00Z",
      "resultMessage": "resultMessage-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedRoleAssignment: my",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
