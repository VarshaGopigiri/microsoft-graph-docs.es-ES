---
title: 'bookingBusiness: cancelar la publicación'
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: 7d0e083eded3ce0c1328c9532358cf7a054db52b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085338"
---
# <a name="bookingbusiness-unpublish"></a><span data-ttu-id="3800b-104">bookingBusiness: cancelar la publicación</span><span class="sxs-lookup"><span data-stu-id="3800b-104">bookingBusiness: unpublish</span></span>

 > <span data-ttu-id="3800b-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3800b-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3800b-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3800b-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="3800b-107">Hacer que la página programación de esta empresa no está disponible para los clientes externos.</span><span class="sxs-lookup"><span data-stu-id="3800b-107">Make the scheduling page of this business not available to external customers.</span></span> 

<span data-ttu-id="3800b-108">Establezca la propiedad **isPublished** en false y la propiedad **publicUrl** en null.</span><span class="sxs-lookup"><span data-stu-id="3800b-108">Set the **isPublished** property to false, and **publicUrl** property to null.</span></span>

## <a name="permissions"></a><span data-ttu-id="3800b-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="3800b-109">Permissions</span></span>
<span data-ttu-id="3800b-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3800b-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3800b-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3800b-112">Permission type</span></span>      | <span data-ttu-id="3800b-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3800b-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3800b-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3800b-114">Delegated (work or school account)</span></span> |  <span data-ttu-id="3800b-115">Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="3800b-115">Bookings.Manage.All</span></span>   |
|<span data-ttu-id="3800b-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3800b-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3800b-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3800b-117">Not supported.</span></span>   |
|<span data-ttu-id="3800b-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3800b-118">Application</span></span> | <span data-ttu-id="3800b-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3800b-119">Not supported.</span></span>  |  

## <a name="http-request"></a><span data-ttu-id="3800b-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3800b-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /bookingBusinesses/{id}/unpublish

```
## <a name="request-headers"></a><span data-ttu-id="3800b-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3800b-121">Request headers</span></span>
| <span data-ttu-id="3800b-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="3800b-122">Name</span></span>       | <span data-ttu-id="3800b-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="3800b-123">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="3800b-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="3800b-124">Authorization</span></span>  | <span data-ttu-id="3800b-125">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="3800b-125">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="3800b-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3800b-126">Request body</span></span>

## <a name="response"></a><span data-ttu-id="3800b-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3800b-127">Response</span></span>
<span data-ttu-id="3800b-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3800b-p104">If successful, this method returns `204 No content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3800b-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3800b-130">Example</span></span>
<span data-ttu-id="3800b-131">Este es un ejemplo de cómo realizar una llamada a esta API.</span><span class="sxs-lookup"><span data-stu-id="3800b-131">The following is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="3800b-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3800b-132">Request</span></span>
<span data-ttu-id="3800b-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3800b-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "bookingbusiness_unpublish"
}-->
```http
POST https://graph.microsoft.com/beta/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/unpublish
```

##### <a name="response"></a><span data-ttu-id="3800b-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3800b-134">Response</span></span>
<span data-ttu-id="3800b-135">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3800b-135">The following is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 204 No content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingBusiness: unpublish",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->