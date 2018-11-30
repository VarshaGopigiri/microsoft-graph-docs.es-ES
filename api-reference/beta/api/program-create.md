---
title: Creación de programa
description: En Azure AD tener acceso a la característica de revisiones, crear un nuevo objeto de programa.
ms.openlocfilehash: 1ac3fa1f0b555fc92449adf0e57217d0a7d50375
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089154"
---
# <a name="create-program"></a><span data-ttu-id="a7bdf-103">Creación de programa</span><span class="sxs-lookup"><span data-stu-id="a7bdf-103">Create program</span></span>

> <span data-ttu-id="a7bdf-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a7bdf-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a7bdf-106">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, cree un nuevo objeto de [programa](../resources/program.md) .</span><span class="sxs-lookup"><span data-stu-id="a7bdf-106">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, create a new [program](../resources/program.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="a7bdf-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a7bdf-107">Permissions</span></span>
<span data-ttu-id="a7bdf-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a7bdf-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a7bdf-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a7bdf-110">Permission type</span></span>                        | <span data-ttu-id="a7bdf-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a7bdf-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="a7bdf-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a7bdf-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="a7bdf-113">`ProgramControl.ReadWrite.All`.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-113"></span></span>  <span data-ttu-id="a7bdf-114">También debe ser el usuario iniciado en un rol de Active directory que le permita crear un programa.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-114">The signed in user must also be in a directory role which permits them to create a program.</span></span> |
|<span data-ttu-id="a7bdf-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a7bdf-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a7bdf-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-116">Not supported.</span></span> |
|<span data-ttu-id="a7bdf-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a7bdf-117">Application</span></span>                            | <span data-ttu-id="a7bdf-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a7bdf-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a7bdf-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /programs
```
## <a name="request-headers"></a><span data-ttu-id="a7bdf-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a7bdf-120">Request headers</span></span>
| <span data-ttu-id="a7bdf-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="a7bdf-121">Name</span></span>         | <span data-ttu-id="a7bdf-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7bdf-122">Type</span></span>        | <span data-ttu-id="a7bdf-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7bdf-123">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="a7bdf-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="a7bdf-124">Authorization</span></span> | <span data-ttu-id="a7bdf-125">string</span><span class="sxs-lookup"><span data-stu-id="a7bdf-125">string</span></span> | <span data-ttu-id="a7bdf-126">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-126">Bearer \{token\}.</span></span> <span data-ttu-id="a7bdf-127">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-127">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a7bdf-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a7bdf-128">Request body</span></span>
<span data-ttu-id="a7bdf-129">En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto de [programa](../resources/program.md) .</span><span class="sxs-lookup"><span data-stu-id="a7bdf-129">In the request body, supply a JSON representation of a [program](../resources/program.md) object.</span></span>

<span data-ttu-id="a7bdf-130">La siguiente tabla muestran las propiedades que son necesarias cuando se crea un programa.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-130">The following table shows the properties that are required when you create a program.</span></span>

| <span data-ttu-id="a7bdf-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a7bdf-131">Property</span></span>     | <span data-ttu-id="a7bdf-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7bdf-132">Type</span></span>        | <span data-ttu-id="a7bdf-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7bdf-133">Description</span></span> |
|:-------------|:------------|:------------|
| `displayName`               |`String`                              |  <span data-ttu-id="a7bdf-134">El nombre del programa.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-134">The name of the program.</span></span>                   |
| `description`               |`String`                              |  <span data-ttu-id="a7bdf-135">La descripción del programa.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-135">The description of the program.</span></span>           |


## <a name="response"></a><span data-ttu-id="a7bdf-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7bdf-136">Response</span></span>
<span data-ttu-id="a7bdf-137">Si tiene éxito, este método devuelve una `201, Created` objeto de [programa](../resources/program.md) y el código de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-137">If successful, this method returns a `201, Created` response code and [program](../resources/program.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a7bdf-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a7bdf-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a7bdf-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a7bdf-139">Request</span></span>
<span data-ttu-id="a7bdf-140">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto de [programa](../resources/program.md) .</span><span class="sxs-lookup"><span data-stu-id="a7bdf-140">In the request body, supply a JSON representation of the [program](../resources/program.md) object.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_program_from_programs"
}-->
```http
POST https://graph.microsoft.com/beta/programs
Content-type: application/json

{
    "displayName": "testprogram3",
    "description": "test description"
}
```

##### <a name="response"></a><span data-ttu-id="a7bdf-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7bdf-141">Response</span></span>
><span data-ttu-id="a7bdf-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.program"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "id": "7e59d237-2fb0-4e5d-b7bb-d4f9f9129213",
    "displayName": "testprogram3",
    "description": "test description"
}
```

## <a name="see-also"></a><span data-ttu-id="a7bdf-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7bdf-144">See also</span></span>

| <span data-ttu-id="a7bdf-145">Método</span><span class="sxs-lookup"><span data-stu-id="a7bdf-145">Method</span></span>           | <span data-ttu-id="a7bdf-146">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7bdf-146">Return Type</span></span>    |<span data-ttu-id="a7bdf-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7bdf-147">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="a7bdf-148">Programas de lista</span><span class="sxs-lookup"><span data-stu-id="a7bdf-148">List programs</span></span>](program-list.md) | <span data-ttu-id="a7bdf-149">colección de [programa](../resources/program.md)</span><span class="sxs-lookup"><span data-stu-id="a7bdf-149">[program](../resources/program.md) collection</span></span>|  <span data-ttu-id="a7bdf-150">Obtener una colección de todos los programas.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-150">Get a collection of all the programs.</span></span>|
|[<span data-ttu-id="a7bdf-151">ProgramControls de lista de un programa</span><span class="sxs-lookup"><span data-stu-id="a7bdf-151">List programControls of a program</span></span>](program-listcontrols.md) |     <span data-ttu-id="a7bdf-152">colección de [programControl](../resources/programcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="a7bdf-152">[programControl](../resources/programcontrol.md) collection</span></span>|    <span data-ttu-id="a7bdf-153">Obtener una colección de los controles de un programa.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-153">Get a collection of the controls of a program.</span></span>|
|[<span data-ttu-id="a7bdf-154">Programa de actualización</span><span class="sxs-lookup"><span data-stu-id="a7bdf-154">Update program</span></span>](program-update.md) |  [<span data-ttu-id="a7bdf-155">programa</span><span class="sxs-lookup"><span data-stu-id="a7bdf-155">program</span></span>](../resources/program.md)| <span data-ttu-id="a7bdf-156">Actualizar un programa.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-156">Update a program.</span></span>|
|[<span data-ttu-id="a7bdf-157">Crear programControl</span><span class="sxs-lookup"><span data-stu-id="a7bdf-157">Create programControl</span></span>](programcontrol-create.md) |        [<span data-ttu-id="a7bdf-158">programControl</span><span class="sxs-lookup"><span data-stu-id="a7bdf-158">programControl</span></span>](../resources/programcontrol.md)    |   <span data-ttu-id="a7bdf-159">Agregar un programControl a un programa.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-159">Add a programControl to a program.</span></span>|

<!-- {
  "type": "#page.annotation",
  "description": "Create program",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
