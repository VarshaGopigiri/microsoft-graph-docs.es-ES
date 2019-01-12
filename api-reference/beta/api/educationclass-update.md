---
title: Actualizar propiedades de educationclass
description: Actualice las propiedades de una clase.
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 7932dc3072689468ceff813a99466d287ce77a1a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950567"
---
# <a name="update-educationclass-properties"></a><span data-ttu-id="ecf78-103">Actualizar propiedades de educationclass</span><span class="sxs-lookup"><span data-stu-id="ecf78-103">Update educationclass properties</span></span>

> <span data-ttu-id="ecf78-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ecf78-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ecf78-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ecf78-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ecf78-106">Actualice las propiedades de una clase.</span><span class="sxs-lookup"><span data-stu-id="ecf78-106">Update the properties of a class.</span></span>

## <a name="permissions"></a><span data-ttu-id="ecf78-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ecf78-107">Permissions</span></span>
<span data-ttu-id="ecf78-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ecf78-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ecf78-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ecf78-110">Permission type</span></span>      | <span data-ttu-id="ecf78-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ecf78-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ecf78-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ecf78-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="ecf78-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ecf78-113">Not supported.</span></span>  |
|<span data-ttu-id="ecf78-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ecf78-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ecf78-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ecf78-115">Not supported.</span></span>   |
|<span data-ttu-id="ecf78-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ecf78-116">Application</span></span> | <span data-ttu-id="ecf78-117">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ecf78-117">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="ecf78-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ecf78-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /education/classes/{id}
```
## <a name="request-headers"></a><span data-ttu-id="ecf78-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ecf78-119">Request headers</span></span>
| <span data-ttu-id="ecf78-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ecf78-120">Header</span></span>       | <span data-ttu-id="ecf78-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ecf78-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ecf78-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="ecf78-122">Authorization</span></span>  | <span data-ttu-id="ecf78-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ecf78-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="ecf78-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ecf78-125">Content-Type</span></span>  | <span data-ttu-id="ecf78-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ecf78-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ecf78-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ecf78-127">Request body</span></span>
<span data-ttu-id="ecf78-128">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="ecf78-128">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="ecf78-129">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ecf78-129">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="ecf78-130">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="ecf78-130">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="ecf78-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ecf78-131">Property</span></span>     | <span data-ttu-id="ecf78-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="ecf78-132">Type</span></span>   |<span data-ttu-id="ecf78-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="ecf78-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ecf78-134">description</span><span class="sxs-lookup"><span data-stu-id="ecf78-134">description</span></span>|<span data-ttu-id="ecf78-135">String</span><span class="sxs-lookup"><span data-stu-id="ecf78-135">String</span></span>| <span data-ttu-id="ecf78-136">Descripción de la clase</span><span class="sxs-lookup"><span data-stu-id="ecf78-136">Description of the class.</span></span>|
|<span data-ttu-id="ecf78-137">displayName</span><span class="sxs-lookup"><span data-stu-id="ecf78-137">displayName</span></span>|<span data-ttu-id="ecf78-138">String</span><span class="sxs-lookup"><span data-stu-id="ecf78-138">String</span></span>| <span data-ttu-id="ecf78-139">Nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="ecf78-139">Name of the class.</span></span>|
|<span data-ttu-id="ecf78-140">mailNickname</span><span class="sxs-lookup"><span data-stu-id="ecf78-140">mailNickname</span></span>|<span data-ttu-id="ecf78-141">String</span><span class="sxs-lookup"><span data-stu-id="ecf78-141">String</span></span>| <span data-ttu-id="ecf78-142">Alias de correo electrónico para enviar correo electrónico a todos los usuarios si esa característica está habilitada.</span><span class="sxs-lookup"><span data-stu-id="ecf78-142">Email alias for sending email to all users if that feature is enabled.</span></span> |
<span data-ttu-id="ecf78-143"><!-- Please verify the revised description here. -->| classCode | Cadena | Clase de código utilizado por la escuela. | | externalId | Cadena | Identificador de la clase desde el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="ecf78-143"><!-- Please verify the revised description here. --> |classCode|String| Class code used by the school.| |externalId|String| ID of the class from the syncing system.</span></span> <span data-ttu-id="ecf78-144">| |externalName|String|Nombre de la clase en el sistema de sincronización.| |externalSource|string| Forma en que se ha creado la clase.</span><span class="sxs-lookup"><span data-stu-id="ecf78-144">| |externalName|String|Name of the class in the syncing system.| |externalSource|string| How this class was created.</span></span> <span data-ttu-id="ecf78-145">Los valores posibles son: `sis`, `manual` y `enum_sentinel`.|</span><span class="sxs-lookup"><span data-stu-id="ecf78-145">Possible values are: `sis`, `manual`, `enum_sentinel`.|</span></span>

## <a name="response"></a><span data-ttu-id="ecf78-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ecf78-146">Response</span></span>
<span data-ttu-id="ecf78-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [educationClass](../resources/educationclass.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ecf78-147">If successful, this method returns a `200 OK` response code and an updated [educationClass](../resources/educationclass.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ecf78-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ecf78-148">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ecf78-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ecf78-149">Request</span></span>
<span data-ttu-id="ecf78-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ecf78-150">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_educationclass"
}-->
```http
PATCH https://graph.microsoft.com/beta/education/classes/11014
Content-type: application/json
Content-length: 224

{
  "description": "History - World History 1",
  "displayName": "World History Level 1",
}
```
##### <a name="response"></a><span data-ttu-id="ecf78-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ecf78-151">Response</span></span>
<span data-ttu-id="ecf78-152">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ecf78-152">The following is an example of the response.</span></span> 

><span data-ttu-id="ecf78-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ecf78-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationClass"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 224

{
  "id": "11014",
  "description": "World History Level 1",
  "classCode": "301",
  "createdBy": {
        "user": {
          "displayName": "Susana Rocha",
          "id": "14012",
        }
      },
  "displayName": "History - World History 1",
  "externalId": "301",
  "externalName": "World History Level 1",
  "externalSource": "Fabrikam High School",
  "mailNickname": "Fabrikam"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update educationclass",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
