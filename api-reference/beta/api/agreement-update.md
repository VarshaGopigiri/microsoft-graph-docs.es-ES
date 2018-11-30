---
title: Contrato de actualización
description: Actualizar las propiedades de un objeto de contrato.
ms.openlocfilehash: b9405a8c469876a349b5c1b0c00e6f6a5f225e72
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084079"
---
# <a name="update-agreement"></a><span data-ttu-id="e5363-103">Contrato de actualización</span><span class="sxs-lookup"><span data-stu-id="e5363-103">Update agreement</span></span>

> <span data-ttu-id="e5363-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e5363-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e5363-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e5363-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e5363-106">Actualizar las propiedades de un objeto de [contrato](../resources/agreement.md) .</span><span class="sxs-lookup"><span data-stu-id="e5363-106">Update the properties of an [agreement](../resources/agreement.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="e5363-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e5363-107">Permissions</span></span>
<span data-ttu-id="e5363-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e5363-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e5363-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e5363-110">Permission type</span></span>                        | <span data-ttu-id="e5363-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e5363-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="e5363-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e5363-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="e5363-113">Agreement.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e5363-113">Agreement.ReadWrite.All</span></span> |
|<span data-ttu-id="e5363-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e5363-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e5363-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e5363-115">Not supported.</span></span> |
|<span data-ttu-id="e5363-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e5363-116">Application</span></span>                            | <span data-ttu-id="e5363-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e5363-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e5363-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e5363-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /agreements/<id>
```
## <a name="request-headers"></a><span data-ttu-id="e5363-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e5363-119">Request headers</span></span>
| <span data-ttu-id="e5363-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="e5363-120">Name</span></span>         | <span data-ttu-id="e5363-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5363-121">Type</span></span>        | <span data-ttu-id="e5363-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5363-122">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="e5363-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="e5363-123">Authorization</span></span> | <span data-ttu-id="e5363-124">string</span><span class="sxs-lookup"><span data-stu-id="e5363-124">string</span></span> | <span data-ttu-id="e5363-125">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="e5363-125">Bearer \{token\}.</span></span> <span data-ttu-id="e5363-126">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e5363-126">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e5363-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e5363-127">Request body</span></span>
<span data-ttu-id="e5363-128">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="e5363-128">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="e5363-129">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e5363-129">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="e5363-130">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="e5363-130">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="e5363-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e5363-131">Property</span></span>     | <span data-ttu-id="e5363-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5363-132">Type</span></span>        | <span data-ttu-id="e5363-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5363-133">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="e5363-134">displayName</span><span class="sxs-lookup"><span data-stu-id="e5363-134">displayName</span></span>|<span data-ttu-id="e5363-135">String</span><span class="sxs-lookup"><span data-stu-id="e5363-135">String</span></span>|<span data-ttu-id="e5363-136">Nombre para mostrar del contrato.</span><span class="sxs-lookup"><span data-stu-id="e5363-136">Display name of the agreement.</span></span>|
|<span data-ttu-id="e5363-137">isViewingBeforeAcceptanceRequired</span><span class="sxs-lookup"><span data-stu-id="e5363-137">isViewingBeforeAcceptanceRequired</span></span>|<span data-ttu-id="e5363-138">Booleano</span><span class="sxs-lookup"><span data-stu-id="e5363-138">Boolean</span></span>|<span data-ttu-id="e5363-139">Si el usuario tiene que expandir y ver el contrato antes de Aceptar.</span><span class="sxs-lookup"><span data-stu-id="e5363-139">Whether the user has to expand and view the agreement before accepting.</span></span>|

## <a name="response"></a><span data-ttu-id="e5363-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5363-140">Response</span></span>
<span data-ttu-id="e5363-141">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado de [acuerdo](../resources/agreement.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e5363-141">If successful, this method returns a `200 OK` response code and an updated [agreement](../resources/agreement.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e5363-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e5363-142">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e5363-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e5363-143">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "update_agreement"
}-->
```http
PATCH https://graph.microsoft.com/beta/agreements/<id>
Content-type: application/json
Content-length: 85

{
  "displayName": "displayName-value",
  "isViewingBeforeAcceptanceRequired": true
}
```
##### <a name="response"></a><span data-ttu-id="e5363-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5363-144">Response</span></span>
><span data-ttu-id="e5363-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e5363-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.agreement"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 105

{
  "displayName": "displayName-value",
  "isViewingBeforeAcceptanceRequired": true,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update agreement",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
