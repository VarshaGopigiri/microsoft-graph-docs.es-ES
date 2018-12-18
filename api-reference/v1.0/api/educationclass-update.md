---
title: Actualizar propiedades de educationclass
description: Actualice las propiedades de una clase.
author: mmast-msft
ms.openlocfilehash: 9a11ae5e1a2139df4ade3417c940d00dea2d1888
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27358712"
---
# <a name="update-educationclass-properties"></a><span data-ttu-id="faef8-103">Actualizar propiedades de educationclass</span><span class="sxs-lookup"><span data-stu-id="faef8-103">Update educationclass properties</span></span>

<span data-ttu-id="faef8-104">Actualice las propiedades de una clase.</span><span class="sxs-lookup"><span data-stu-id="faef8-104">Update the properties of a class.</span></span>

## <a name="permissions"></a><span data-ttu-id="faef8-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="faef8-105">Permissions</span></span>
<span data-ttu-id="faef8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="faef8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="faef8-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="faef8-108">Permission type</span></span>      | <span data-ttu-id="faef8-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="faef8-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="faef8-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="faef8-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="faef8-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="faef8-111">Not supported.</span></span>  |
|<span data-ttu-id="faef8-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="faef8-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="faef8-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="faef8-113">Not supported.</span></span>   |
|<span data-ttu-id="faef8-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="faef8-114">Application</span></span> | <span data-ttu-id="faef8-115">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="faef8-115">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="faef8-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="faef8-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /education/classes/{id}
```
## <a name="request-headers"></a><span data-ttu-id="faef8-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="faef8-117">Request headers</span></span>
| <span data-ttu-id="faef8-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="faef8-118">Header</span></span>       | <span data-ttu-id="faef8-119">Valor</span><span class="sxs-lookup"><span data-stu-id="faef8-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="faef8-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="faef8-120">Authorization</span></span>  | <span data-ttu-id="faef8-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="faef8-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="faef8-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="faef8-123">Content-Type</span></span>  | <span data-ttu-id="faef8-124">application/json</span><span class="sxs-lookup"><span data-stu-id="faef8-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="faef8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="faef8-125">Request body</span></span>
<span data-ttu-id="faef8-126">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="faef8-126">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="faef8-127">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="faef8-127">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="faef8-128">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="faef8-128">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="faef8-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="faef8-129">Property</span></span>     | <span data-ttu-id="faef8-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="faef8-130">Type</span></span>   |<span data-ttu-id="faef8-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="faef8-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="faef8-132">description</span><span class="sxs-lookup"><span data-stu-id="faef8-132">description</span></span>|<span data-ttu-id="faef8-133">String</span><span class="sxs-lookup"><span data-stu-id="faef8-133">String</span></span>| <span data-ttu-id="faef8-134">Descripción de la clase</span><span class="sxs-lookup"><span data-stu-id="faef8-134">Description of the class.</span></span>|
|<span data-ttu-id="faef8-135">displayName</span><span class="sxs-lookup"><span data-stu-id="faef8-135">displayName</span></span>|<span data-ttu-id="faef8-136">String</span><span class="sxs-lookup"><span data-stu-id="faef8-136">String</span></span>| <span data-ttu-id="faef8-137">Nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="faef8-137">Name of the class.</span></span>|
|<span data-ttu-id="faef8-138">mailNickname</span><span class="sxs-lookup"><span data-stu-id="faef8-138">mailNickname</span></span>|<span data-ttu-id="faef8-139">String</span><span class="sxs-lookup"><span data-stu-id="faef8-139">String</span></span>| <span data-ttu-id="faef8-140">Alias de correo electrónico para enviar correo electrónico a todos los usuarios si esa característica está habilitada.</span><span class="sxs-lookup"><span data-stu-id="faef8-140">Email alias for sending email to all users if that feature is enabled.</span></span> |
<span data-ttu-id="faef8-141"><!-- Please verify the revised description here. -->| classCode | Cadena | Clase de código utilizado por la escuela. | | externalId | Cadena | Identificador de la clase desde el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="faef8-141"><!-- Please verify the revised description here. --> |classCode|String| Class code used by the school.| |externalId|String| ID of the class from the syncing system.</span></span> <span data-ttu-id="faef8-142">| |externalName|String|Nombre de la clase en el sistema de sincronización.| |externalSource|string| Forma en que se ha creado la clase.</span><span class="sxs-lookup"><span data-stu-id="faef8-142">| |externalName|String|Name of the class in the syncing system.| |externalSource|string| How this class was created.</span></span> <span data-ttu-id="faef8-143">Los valores posibles son: `sis`, `manual`, `enum_sentinel`. |</span><span class="sxs-lookup"><span data-stu-id="faef8-143">The possible values are: `sis`, `manual`, `enum_sentinel`.|</span></span>

## <a name="response"></a><span data-ttu-id="faef8-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="faef8-144">Response</span></span>
<span data-ttu-id="faef8-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [educationClass](../resources/educationclass.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="faef8-145">If successful, this method returns a `200 OK` response code and an updated [educationClass](../resources/educationclass.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="faef8-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="faef8-146">Example</span></span>
##### <a name="request"></a><span data-ttu-id="faef8-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="faef8-147">Request</span></span>
<span data-ttu-id="faef8-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="faef8-148">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_educationclass"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/education/classes/{class-id}
Content-type: application/json
Content-length: 224

{
  "description": "History - World History 1",
  "displayName": "World History Level 1",
}
```
##### <a name="response"></a><span data-ttu-id="faef8-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="faef8-149">Response</span></span>
<span data-ttu-id="faef8-150">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="faef8-150">The following is an example of the response.</span></span> 

><span data-ttu-id="faef8-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="faef8-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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