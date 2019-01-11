---
title: Actualizar connectorGroups
description: Actualizar las propiedades del objeto connectorgroup.
localization_priority: Normal
ms.openlocfilehash: 9a4db622328edd4d3aea348fd078acdc832a9c52
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27843804"
---
# <a name="update-connectorgroups"></a><span data-ttu-id="84407-103">Actualizar connectorGroups</span><span class="sxs-lookup"><span data-stu-id="84407-103">Update connectorGroups</span></span>

> <span data-ttu-id="84407-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="84407-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="84407-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="84407-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="84407-106">Actualizar las propiedades del objeto connectorgroup.</span><span class="sxs-lookup"><span data-stu-id="84407-106">Update the properties of connectorgroup object.</span></span>
## <a name="permissions"></a><span data-ttu-id="84407-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="84407-107">Permissions</span></span>
<span data-ttu-id="84407-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="84407-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="84407-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="84407-110">Permission type</span></span>      | <span data-ttu-id="84407-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="84407-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="84407-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="84407-112">Delegated (work or school account)</span></span> | <span data-ttu-id="84407-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="84407-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="84407-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="84407-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="84407-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="84407-115">Not supported.</span></span>    |
|<span data-ttu-id="84407-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="84407-116">Application</span></span> | <span data-ttu-id="84407-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="84407-117">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="84407-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="84407-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /connectorGroups/{id}
```
## <a name="optional-request-headers"></a><span data-ttu-id="84407-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="84407-119">Optional request headers</span></span>
| <span data-ttu-id="84407-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="84407-120">Name</span></span>       | <span data-ttu-id="84407-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="84407-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="84407-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="84407-122">Authorization</span></span>  | <span data-ttu-id="84407-123">Bearer.</span><span class="sxs-lookup"><span data-stu-id="84407-123">Bearer.</span></span> <span data-ttu-id="84407-124">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="84407-124">Required</span></span>|

## <a name="request-body"></a><span data-ttu-id="84407-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="84407-125">Request body</span></span>
<span data-ttu-id="84407-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="84407-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="84407-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="84407-129">Property</span></span>     | <span data-ttu-id="84407-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="84407-130">Type</span></span>   |<span data-ttu-id="84407-131">Description</span><span class="sxs-lookup"><span data-stu-id="84407-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="84407-132">connectorGroupType</span><span class="sxs-lookup"><span data-stu-id="84407-132">connectorGroupType</span></span>|<span data-ttu-id="84407-133">string</span><span class="sxs-lookup"><span data-stu-id="84407-133">string</span></span>| <span data-ttu-id="84407-134">Los valores posibles son: `applicationProxy`.</span><span class="sxs-lookup"><span data-stu-id="84407-134">Possible values are: `applicationProxy`.</span></span>|
|<span data-ttu-id="84407-135">name</span><span class="sxs-lookup"><span data-stu-id="84407-135">name</span></span>|<span data-ttu-id="84407-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="84407-136">String</span></span>|<span data-ttu-id="84407-137">El nombre de la connectorGroup.</span><span class="sxs-lookup"><span data-stu-id="84407-137">The name of the connectorGroup.</span></span>|

## <a name="response"></a><span data-ttu-id="84407-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="84407-138">Response</span></span>

<span data-ttu-id="84407-139">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y actualizada [connectorGroup](../resources/connectorgroup.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="84407-139">If successful, this method returns a `200 OK` response code and updated [connectorGroup](../resources/connectorgroup.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="84407-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84407-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="84407-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="84407-141">Request</span></span>
<span data-ttu-id="84407-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="84407-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_connectorgroup"
}-->
```http
PATCH https://graph.microsoft.com/{ver}/connectorGroups/{id}
Content-type: application/json
Content-length: 99

{
  "name": "name-value",
  "connectorGroupType": "connectorGroupType-value",
}
```
##### <a name="response"></a><span data-ttu-id="84407-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="84407-143">Response</span></span>
<span data-ttu-id="84407-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="84407-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.connectorGroup"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 119

{
  "id": "id-value",
  "name": "name-value",
  "connectorGroupType": "connectorGroupType-value",
  "isDefault": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update connectorgroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
