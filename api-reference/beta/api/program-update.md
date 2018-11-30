---
title: Programa de actualización
description: En Azure AD tener acceso a la característica de revisiones, actualizar un objeto de programa existente.
ms.openlocfilehash: e3d8ca75683a076f156e359431204517b60e7c6d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088501"
---
# <a name="update-program"></a><span data-ttu-id="90373-103">Programa de actualización</span><span class="sxs-lookup"><span data-stu-id="90373-103">Update program</span></span>

> <span data-ttu-id="90373-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="90373-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="90373-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="90373-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="90373-106">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, actualizar un objeto de [programa](../resources/program.md) existente.</span><span class="sxs-lookup"><span data-stu-id="90373-106">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, update an existing [program](../resources/program.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="90373-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="90373-107">Permissions</span></span>
<span data-ttu-id="90373-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="90373-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="90373-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="90373-110">Permission type</span></span>                        | <span data-ttu-id="90373-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="90373-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="90373-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="90373-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="90373-113">`ProgramControl.ReadWrite.All`.</span><span class="sxs-lookup"><span data-stu-id="90373-113"></span></span>  <span data-ttu-id="90373-114">También debe ser el usuario iniciado en un rol de Active directory que le permita actualizar un programa.</span><span class="sxs-lookup"><span data-stu-id="90373-114">The signed in user must also be in a directory role which permits them to update a program.</span></span> |
|<span data-ttu-id="90373-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="90373-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="90373-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="90373-116">Not supported.</span></span> |
|<span data-ttu-id="90373-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="90373-117">Application</span></span>                            | <span data-ttu-id="90373-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="90373-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="90373-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="90373-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /programs('{programId}')
```
## <a name="request-headers"></a><span data-ttu-id="90373-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="90373-120">Request headers</span></span>
| <span data-ttu-id="90373-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="90373-121">Name</span></span>         | <span data-ttu-id="90373-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="90373-122">Type</span></span>        | <span data-ttu-id="90373-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="90373-123">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="90373-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="90373-124">Authorization</span></span> | <span data-ttu-id="90373-125">string</span><span class="sxs-lookup"><span data-stu-id="90373-125">string</span></span> | <span data-ttu-id="90373-126">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="90373-126">Bearer \{token\}.</span></span> <span data-ttu-id="90373-127">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="90373-127">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="90373-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="90373-128">Request body</span></span>
<span data-ttu-id="90373-129">En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto de [programa](../resources/program.md) .</span><span class="sxs-lookup"><span data-stu-id="90373-129">In the request body, supply a JSON representation of a [program](../resources/program.md) object.</span></span>

<span data-ttu-id="90373-130">En la siguiente tabla se muestra las propiedades que se pueden proporcionar al actualizar un programa.</span><span class="sxs-lookup"><span data-stu-id="90373-130">The following table shows the properties that can be supplied when you update a program.</span></span>

| <span data-ttu-id="90373-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="90373-131">Property</span></span>     | <span data-ttu-id="90373-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="90373-132">Type</span></span>        | <span data-ttu-id="90373-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="90373-133">Description</span></span> |
|:-------------|:------------|:------------|
| `displayName`               |`String`                              |  <span data-ttu-id="90373-134">El nombre del programa.</span><span class="sxs-lookup"><span data-stu-id="90373-134">The name of the program.</span></span>                   |
| `description`               |`String`                              |  <span data-ttu-id="90373-135">La descripción del programa.</span><span class="sxs-lookup"><span data-stu-id="90373-135">The description of the program.</span></span>           |


## <a name="response"></a><span data-ttu-id="90373-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90373-136">Response</span></span>
<span data-ttu-id="90373-137">Si tiene éxito, este método devuelve una `204, Accepted` objeto de [programa](../resources/program.md) y el código de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="90373-137">If successful, this method returns a `204, Accepted` response code and [program](../resources/program.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="90373-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="90373-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="90373-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="90373-139">Request</span></span>
<span data-ttu-id="90373-140">En el cuerpo de la solicitud, proporcionar una representación JSON de los parámetros del objeto [programa](../resources/program.md) para cambiar.</span><span class="sxs-lookup"><span data-stu-id="90373-140">In the request body, supply a JSON representation of the [program](../resources/program.md) object parameters to change.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_program"
}-->
```http
PATCH https://graph.microsoft.com/beta/programs('7e59d237-2fb0-4e5d-b7bb-d4f9f9129213')
Content-type: application/json

{
    "displayName": "testprogram3 new name"
}
```

##### <a name="response"></a><span data-ttu-id="90373-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90373-141">Response</span></span>
><span data-ttu-id="90373-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="90373-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.program"
} -->
```http
HTTP/1.1 204 Accepted
Content-type: application/json

{
    "id": "7e59d237-2fb0-4e5d-b7bb-d4f9f9129213",
    "displayName": "testprogram3 new name",
    "description": "test description"
}
```

## <a name="see-also"></a><span data-ttu-id="90373-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="90373-144">See also</span></span>

| <span data-ttu-id="90373-145">Método</span><span class="sxs-lookup"><span data-stu-id="90373-145">Method</span></span>           | <span data-ttu-id="90373-146">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90373-146">Return Type</span></span>    |<span data-ttu-id="90373-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="90373-147">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="90373-148">ProgramControls de lista de un programa</span><span class="sxs-lookup"><span data-stu-id="90373-148">List programControls of a program</span></span>](program-listcontrols.md) |     <span data-ttu-id="90373-149">colección de [programControl](../resources/programcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="90373-149">[programControl](../resources/programcontrol.md) collection</span></span>|    <span data-ttu-id="90373-150">Obtener una colección de los controles de un programa.</span><span class="sxs-lookup"><span data-stu-id="90373-150">Get a collection of the controls of a program.</span></span>|
|[<span data-ttu-id="90373-151">Crear programControl</span><span class="sxs-lookup"><span data-stu-id="90373-151">Create programControl</span></span>](programcontrol-create.md) |        [<span data-ttu-id="90373-152">programControl</span><span class="sxs-lookup"><span data-stu-id="90373-152">programControl</span></span>](../resources/programcontrol.md)    |   <span data-ttu-id="90373-153">Agregar un programControl a un programa.</span><span class="sxs-lookup"><span data-stu-id="90373-153">Add a programControl to a program.</span></span>|

<!-- {
  "type": "#page.annotation",
  "description": "Update program",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
