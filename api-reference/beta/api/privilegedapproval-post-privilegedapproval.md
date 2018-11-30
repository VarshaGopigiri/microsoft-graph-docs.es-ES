---
title: Crear privilegedApproval
description: Utilice esta API para crear un nuevo privilegedApproval.
ms.openlocfilehash: 549f4e37ae60cf81d73163c1badd35247113119b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089609"
---
# <a name="create-privilegedapproval"></a><span data-ttu-id="89c5d-103">Crear privilegedApproval</span><span class="sxs-lookup"><span data-stu-id="89c5d-103">Create privilegedApproval</span></span>

> <span data-ttu-id="89c5d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="89c5d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="89c5d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="89c5d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="89c5d-106">Utilice esta API para crear un nuevo privilegedApproval.</span><span class="sxs-lookup"><span data-stu-id="89c5d-106">Use this API to create a new privilegedApproval.</span></span>
## <a name="permissions"></a><span data-ttu-id="89c5d-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="89c5d-107">Permissions</span></span>
<span data-ttu-id="89c5d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="89c5d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="89c5d-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="89c5d-110">Permission type</span></span>      | <span data-ttu-id="89c5d-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="89c5d-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="89c5d-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="89c5d-112">Delegated (work or school account)</span></span> | <span data-ttu-id="89c5d-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="89c5d-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="89c5d-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="89c5d-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="89c5d-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="89c5d-115">Not supported.</span></span>    |
|<span data-ttu-id="89c5d-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="89c5d-116">Application</span></span> | <span data-ttu-id="89c5d-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="89c5d-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="89c5d-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="89c5d-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedApproval

```
## <a name="request-headers"></a><span data-ttu-id="89c5d-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="89c5d-119">Request headers</span></span>
| <span data-ttu-id="89c5d-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="89c5d-120">Name</span></span>       | <span data-ttu-id="89c5d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="89c5d-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="89c5d-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="89c5d-122">Authorization</span></span>  | <span data-ttu-id="89c5d-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="89c5d-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="89c5d-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="89c5d-125">Request body</span></span>
<span data-ttu-id="89c5d-126">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [privilegedApproval](../resources/privilegedapproval.md) .</span><span class="sxs-lookup"><span data-stu-id="89c5d-126">In the request body, supply a JSON representation of [privilegedApproval](../resources/privilegedapproval.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="89c5d-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="89c5d-127">Response</span></span>

<span data-ttu-id="89c5d-128">Si tiene éxito, este método devuelve `201 Created` objeto de código y [privilegedApproval](../resources/privilegedapproval.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="89c5d-128">If successful, this method returns `201 Created` response code and [privilegedApproval](../resources/privilegedapproval.md) object in the response body.</span></span>

<span data-ttu-id="89c5d-129">Tenga en cuenta que el inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="89c5d-129">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="89c5d-130">De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="89c5d-130">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>

## <a name="example"></a><span data-ttu-id="89c5d-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="89c5d-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="89c5d-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="89c5d-132">Request</span></span>
<span data-ttu-id="89c5d-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="89c5d-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_privilegedapproval_from_privilegedapproval"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedApproval
Content-type: application/json
Content-length: 180

{
  "userId": "userId-value",
  "roleId": "roleId-value",
  "approvalType": "approvalType-value",
  "approvalState": "approvalState-value",
  "approvalDuration": "datetime-value"
}
```
<span data-ttu-id="89c5d-134">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [privilegedApproval](../resources/privilegedapproval.md) .</span><span class="sxs-lookup"><span data-stu-id="89c5d-134">In the request body, supply a JSON representation of [privilegedApproval](../resources/privilegedapproval.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="89c5d-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="89c5d-135">Response</span></span>
<span data-ttu-id="89c5d-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="89c5d-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedApproval"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 200

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
  "description": "Create privilegedApproval",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->