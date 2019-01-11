---
title: 'bookingBusiness: publicar'
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: 58dfc0487a12524f3d87992c5d3cc288e092db01
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809411"
---
# <a name="bookingbusiness-publish"></a><span data-ttu-id="64218-104">bookingBusiness: publicar</span><span class="sxs-lookup"><span data-stu-id="64218-104">bookingBusiness: publish</span></span>

 > <span data-ttu-id="64218-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="64218-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="64218-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="64218-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="64218-107">Ponga la página programación de este negocio a disposición de los clientes externos.</span><span class="sxs-lookup"><span data-stu-id="64218-107">Make the scheduling page of this business available to external customers.</span></span> 

<span data-ttu-id="64218-108">Establezca la propiedad **isPublished** en true y la propiedad **publicUrl** a la dirección URL de la página de programación.</span><span class="sxs-lookup"><span data-stu-id="64218-108">Set the **isPublished** property to true, and **publicUrl** property to the URL of the scheduling page.</span></span>

## <a name="permissions"></a><span data-ttu-id="64218-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="64218-109">Permissions</span></span>
<span data-ttu-id="64218-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="64218-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="64218-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="64218-112">Permission type</span></span>      | <span data-ttu-id="64218-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="64218-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="64218-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="64218-114">Delegated (work or school account)</span></span> |  <span data-ttu-id="64218-115">Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="64218-115">Bookings.Manage.All</span></span>   |
|<span data-ttu-id="64218-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="64218-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="64218-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="64218-117">Not supported.</span></span>   |
|<span data-ttu-id="64218-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="64218-118">Application</span></span> | <span data-ttu-id="64218-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="64218-119">Not supported.</span></span>  |  

## <a name="http-request"></a><span data-ttu-id="64218-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="64218-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /bookingBusinesses/{id}/publish

```
## <a name="request-headers"></a><span data-ttu-id="64218-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="64218-121">Request headers</span></span>
| <span data-ttu-id="64218-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="64218-122">Name</span></span>       | <span data-ttu-id="64218-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="64218-123">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="64218-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="64218-124">Authorization</span></span>  | <span data-ttu-id="64218-125">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="64218-125">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="64218-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="64218-126">Request body</span></span>

## <a name="response"></a><span data-ttu-id="64218-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="64218-127">Response</span></span>
<span data-ttu-id="64218-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="64218-p104">If successful, this method returns `204 No content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="64218-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="64218-130">Example</span></span>
<span data-ttu-id="64218-131">Este es un ejemplo de cómo realizar una llamada a esta API.</span><span class="sxs-lookup"><span data-stu-id="64218-131">The following is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="64218-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="64218-132">Request</span></span>
<span data-ttu-id="64218-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="64218-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "bookingbusiness_publish"
}-->
```http
POST https://graph.microsoft.com/beta/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/publish
```

##### <a name="response"></a><span data-ttu-id="64218-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="64218-134">Response</span></span>
<span data-ttu-id="64218-135">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="64218-135">The following is an example of the response.</span></span> 
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
  "description": "bookingBusiness: publish",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
