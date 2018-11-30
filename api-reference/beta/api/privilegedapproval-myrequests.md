---
title: 'privilegedApproval: myRequests'
description: Obtenga las solicitudes de aprobación del solicitante.
ms.openlocfilehash: 22485c1ec1127b6c8a3e1f2b40e7d052e885c357
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089611"
---
# <a name="privilegedapproval-myrequests"></a><span data-ttu-id="26f23-103">privilegedApproval: myRequests</span><span class="sxs-lookup"><span data-stu-id="26f23-103">privilegedApproval: myRequests</span></span>

> <span data-ttu-id="26f23-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="26f23-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="26f23-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="26f23-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="26f23-106">Obtenga las solicitudes de aprobación del solicitante.</span><span class="sxs-lookup"><span data-stu-id="26f23-106">Get the requestor's approval requests.</span></span>

## <a name="permissions"></a><span data-ttu-id="26f23-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="26f23-107">Permissions</span></span>
<span data-ttu-id="26f23-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="26f23-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="26f23-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="26f23-110">Permission type</span></span>      | <span data-ttu-id="26f23-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="26f23-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="26f23-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="26f23-112">Delegated (work or school account)</span></span> | <span data-ttu-id="26f23-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="26f23-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="26f23-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="26f23-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="26f23-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="26f23-115">Not supported.</span></span>    |
|<span data-ttu-id="26f23-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="26f23-116">Application</span></span> | <span data-ttu-id="26f23-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="26f23-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="26f23-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="26f23-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedApproval/myRequests

```
## <a name="request-headers"></a><span data-ttu-id="26f23-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="26f23-119">Request headers</span></span>
| <span data-ttu-id="26f23-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="26f23-120">Name</span></span>       | <span data-ttu-id="26f23-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="26f23-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="26f23-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="26f23-122">Authorization</span></span>  | <span data-ttu-id="26f23-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="26f23-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="26f23-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="26f23-125">Request body</span></span>

## <a name="response"></a><span data-ttu-id="26f23-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="26f23-126">Response</span></span>

<span data-ttu-id="26f23-127">Si tiene éxito, este método devuelve `200 OK` objeto de código y [privilegedApproval](../resources/privilegedapproval.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="26f23-127">If successful, this method returns `200 OK` response code and [privilegedApproval](../resources/privilegedapproval.md) object in the response body.</span></span>

<span data-ttu-id="26f23-128">Tenga en cuenta que el inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="26f23-128">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="26f23-129">De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="26f23-129">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>

## <a name="example"></a><span data-ttu-id="26f23-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="26f23-130">Example</span></span>
<span data-ttu-id="26f23-131">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="26f23-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="26f23-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="26f23-132">Request</span></span>
<span data-ttu-id="26f23-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="26f23-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "privilegedapproval_myrequests"
}-->
```http
GET https://graph.microsoft.com/beta/privilegedApproval/myRequests
```

##### <a name="response"></a><span data-ttu-id="26f23-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="26f23-134">Response</span></span>
<span data-ttu-id="26f23-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="26f23-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedApproval"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 193

{
  "id": "id-value",
  "userId": "userId-value",
  "roleId": "roleId-value",
  "approvalType": "approvalType-value",
  "approvalState": "approvalState-value",
  "approvalDuration": "datetime-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedApproval: myRequests",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
