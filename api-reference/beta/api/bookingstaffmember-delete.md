---
title: Eliminar bookingStaffMember
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: cca8d7794922244e1e6eab0f43bf0ac95c752897
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083711"
---
# <a name="delete-bookingstaffmember"></a><span data-ttu-id="85ecc-104">Eliminar bookingStaffMember</span><span class="sxs-lookup"><span data-stu-id="85ecc-104">Delete bookingStaffMember</span></span>

 > <span data-ttu-id="85ecc-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="85ecc-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="85ecc-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="85ecc-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="85ecc-107">Eliminar un [miembro de la plantilla](../resources/bookingstaffmember.md) en el especificado [bookingbusiness](../resources/bookingbusiness.md).</span><span class="sxs-lookup"><span data-stu-id="85ecc-107">Delete a [staff member](../resources/bookingstaffmember.md) in the specified [bookingbusiness](../resources/bookingbusiness.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="85ecc-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="85ecc-108">Permissions</span></span>
<span data-ttu-id="85ecc-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="85ecc-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="85ecc-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="85ecc-111">Permission type</span></span>      | <span data-ttu-id="85ecc-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="85ecc-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="85ecc-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="85ecc-113">Delegated (work or school account)</span></span> |  <span data-ttu-id="85ecc-114">Bookings.ReadWrite.All, Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="85ecc-114">Bookings.ReadWrite.All, Bookings.Manage.All</span></span>   |
|<span data-ttu-id="85ecc-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="85ecc-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="85ecc-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="85ecc-116">Not supported.</span></span>   |
|<span data-ttu-id="85ecc-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="85ecc-117">Application</span></span> | <span data-ttu-id="85ecc-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="85ecc-118">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="85ecc-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="85ecc-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /bookingBusinesses/{id}/staffMembers/{id}

```
## <a name="request-headers"></a><span data-ttu-id="85ecc-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="85ecc-120">Request headers</span></span>
| <span data-ttu-id="85ecc-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="85ecc-121">Name</span></span>       | <span data-ttu-id="85ecc-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="85ecc-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="85ecc-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="85ecc-123">Authorization</span></span>  | <span data-ttu-id="85ecc-124">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="85ecc-124">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="85ecc-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="85ecc-125">Request body</span></span>
<span data-ttu-id="85ecc-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="85ecc-126">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="85ecc-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="85ecc-127">Response</span></span>
<span data-ttu-id="85ecc-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="85ecc-p104">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="85ecc-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="85ecc-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="85ecc-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="85ecc-131">Request</span></span>
<span data-ttu-id="85ecc-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="85ecc-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_bookingstaffmember"
}-->
```http
DELETE https://graph.microsoft.com/beta/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/staffmembers/5fae928f-6d2d-417a-ad96-4b0caeb362d6
```
##### <a name="response"></a><span data-ttu-id="85ecc-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="85ecc-133">Response</span></span>
<span data-ttu-id="85ecc-134">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="85ecc-134">The following is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete bookingStaffMember",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->