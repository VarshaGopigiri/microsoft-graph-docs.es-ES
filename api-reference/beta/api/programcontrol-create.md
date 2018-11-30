---
title: Crear programControl
description: En Azure AD tener acceso a la característica de revisiones, crear un nuevo objeto programControl.  Esto vincula una revisión de acceso a un programa.
ms.openlocfilehash: fa6a93b13391fd4b9e3c5816bb2a27259e730c0d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088702"
---
# <a name="create-programcontrol"></a><span data-ttu-id="c5a56-104">Crear programControl</span><span class="sxs-lookup"><span data-stu-id="c5a56-104">Create programControl</span></span>

> <span data-ttu-id="c5a56-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c5a56-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c5a56-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c5a56-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c5a56-107">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, cree un nuevo objeto [programControl](../resources/programcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="c5a56-107">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, create a new [programControl](../resources/programcontrol.md) object.</span></span>  <span data-ttu-id="c5a56-108">Esto vincula una revisión de acceso a un programa.</span><span class="sxs-lookup"><span data-stu-id="c5a56-108">This links an access review to a program.</span></span>

<span data-ttu-id="c5a56-109">Antes de realizar esta solicitud, el llamador debe tener anteriormente</span><span class="sxs-lookup"><span data-stu-id="c5a56-109">Prior to making this request, the caller must have previously</span></span>

 - <span data-ttu-id="c5a56-110">[crea un programa](program-create.md) o [recuperar un programa](program-list.md), para que el valor de `programId` para incluir en la solicitud,</span><span class="sxs-lookup"><span data-stu-id="c5a56-110">[created a program](program-create.md) or [retrieved a program](program-list.md), to have the value of `programId` to include in the request,</span></span>
 - <span data-ttu-id="c5a56-111">[crea una revisión de acceso](accessreview-create.md) o [recuperar una revisión de acceso](accessreview-get.md), para que el valor de `controlId` para incluir en la solicitud, y</span><span class="sxs-lookup"><span data-stu-id="c5a56-111">[created an access review](accessreview-create.md) or [retrieved an access review](accessreview-get.md), to have the value of `controlId` to include in the request, and</span></span>
 - <span data-ttu-id="c5a56-112">[recupera la lista de tipos de control de programa](programcontroltype-list.md), para que el valor de `controlTypeId` para incluir en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c5a56-112">[retrieved the list of program control types](programcontroltype-list.md), to have the value of `controlTypeId` to include in the request.</span></span>


## <a name="permissions"></a><span data-ttu-id="c5a56-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="c5a56-113">Permissions</span></span>
<span data-ttu-id="c5a56-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c5a56-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c5a56-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c5a56-116">Permission type</span></span>                        | <span data-ttu-id="c5a56-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c5a56-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="c5a56-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c5a56-118">Delegated (work or school account)</span></span>     | <span data-ttu-id="c5a56-119">`ProgramControl.ReadWrite.All`.</span><span class="sxs-lookup"><span data-stu-id="c5a56-119"></span></span>  <span data-ttu-id="c5a56-120">El usuario iniciado también debe estar en un rol de Active directory que le permita crear un programControl.</span><span class="sxs-lookup"><span data-stu-id="c5a56-120">The signed in user must also be in a directory role which permits them to create a programControl.</span></span> |
|<span data-ttu-id="c5a56-121">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c5a56-121">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c5a56-122">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c5a56-122">Not supported.</span></span> |
|<span data-ttu-id="c5a56-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c5a56-123">Application</span></span>                            | <span data-ttu-id="c5a56-124">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c5a56-124">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c5a56-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c5a56-125">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /programControls
```
## <a name="request-headers"></a><span data-ttu-id="c5a56-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c5a56-126">Request headers</span></span>
| <span data-ttu-id="c5a56-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="c5a56-127">Name</span></span>         | <span data-ttu-id="c5a56-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5a56-128">Type</span></span>        | <span data-ttu-id="c5a56-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5a56-129">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="c5a56-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="c5a56-130">Authorization</span></span> | <span data-ttu-id="c5a56-131">string</span><span class="sxs-lookup"><span data-stu-id="c5a56-131">string</span></span> | <span data-ttu-id="c5a56-132">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="c5a56-132">Bearer \{token\}.</span></span> <span data-ttu-id="c5a56-133">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c5a56-133">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c5a56-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c5a56-134">Request body</span></span>
<span data-ttu-id="c5a56-135">En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto [programControl](../resources/programcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="c5a56-135">In the request body, supply a JSON representation of a [programControl](../resources/programcontrol.md) object.</span></span>

<span data-ttu-id="c5a56-136">La siguiente tabla muestran las propiedades que son necesarias cuando se crea un control de programa.</span><span class="sxs-lookup"><span data-stu-id="c5a56-136">The following table shows the properties that are required when you create a program control.</span></span>

| <span data-ttu-id="c5a56-137">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c5a56-137">Property</span></span>     | <span data-ttu-id="c5a56-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5a56-138">Type</span></span>        | <span data-ttu-id="c5a56-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5a56-139">Description</span></span> |
|:-------------|:------------|:------------|
| `programId`              |`String`                | <span data-ttu-id="c5a56-140">El programId del programa de este control se va a convertirse en una parte de.</span><span class="sxs-lookup"><span data-stu-id="c5a56-140">The programId of the program this control is going to become a part of.</span></span>                             |
| `controlId`              |`String`                | <span data-ttu-id="c5a56-141">ControlId del control, en particular, el identificador de una revisión de access.</span><span class="sxs-lookup"><span data-stu-id="c5a56-141">The controlId of the control, in particular the identifier of an access review.</span></span>                                                |
| `controlTypeId`          |`String`                | <span data-ttu-id="c5a56-142">El programControlType identifica el tipo de control de programa: por ejemplo, se revisa un control de vinculación para acceso de invitado.</span><span class="sxs-lookup"><span data-stu-id="c5a56-142">The programControlType identifies the type of program control - for example, a control linking to guest access reviews.</span></span> |

## <a name="response"></a><span data-ttu-id="c5a56-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c5a56-143">Response</span></span>
<span data-ttu-id="c5a56-144">Si tiene éxito, este método devuelve una `201, Created` código de respuesta y un objeto [programControl](../resources/programcontrol.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c5a56-144">If successful, this method returns a `201, Created` response code and a [programControl](../resources/programcontrol.md) object in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="c5a56-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c5a56-145">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c5a56-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c5a56-146">Request</span></span>
<span data-ttu-id="c5a56-147">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [programControl](../resources/programcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="c5a56-147">In the request body, supply a JSON representation of the [programControl](../resources/programcontrol.md) object.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_programControl_from_programControls"
}-->
```http
POST https://graph.microsoft.com/beta/programControls
Content-type: application/json

{
    "controlId": "7e59d237-2fb0-4e5d-b7bb-d4f9f9129213",
    "controlTypeId": "6e4f3d20-c5c3-407f-9695-8460952bcc68",
    "programId": "7e59d237-2fb0-4e5d-b7bb-d4f9f9129213"
}
```

##### <a name="response"></a><span data-ttu-id="c5a56-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c5a56-148">Response</span></span>
><span data-ttu-id="c5a56-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c5a56-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.programControl"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "id": "63b2302c-7e62-43b7-aefb-063ba5bdb853",
  "controlId": "7e59d237-2fb0-4e5d-b7bb-d4f9f9129213",
  "programId": "7e59d237-2fb0-4e5d-b7bb-d4f9f9129213",
  "controlTypeId": "6e4f3d20-c5c3-407f-9695-8460952bcc68",
  "displayName": "test",
  "status": "Active",
  "createdDateTime": "2018-05-18T20:26:05.2976279Z"
}
```

## <a name="see-also"></a><span data-ttu-id="c5a56-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5a56-151">See also</span></span>

| <span data-ttu-id="c5a56-152">Método</span><span class="sxs-lookup"><span data-stu-id="c5a56-152">Method</span></span>           | <span data-ttu-id="c5a56-153">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5a56-153">Return Type</span></span>    |<span data-ttu-id="c5a56-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5a56-154">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="c5a56-155">Lista programControlTypes</span><span class="sxs-lookup"><span data-stu-id="c5a56-155">List programControlTypes</span></span>](../api/programcontroltype-list.md) | <span data-ttu-id="c5a56-156">colección de [programControlType](../resources/programcontroltype.md)</span><span class="sxs-lookup"><span data-stu-id="c5a56-156">[programControlType](../resources/programcontroltype.md) collection</span></span>| <span data-ttu-id="c5a56-157">Lista de tipos de control de programa.</span><span class="sxs-lookup"><span data-stu-id="c5a56-157">List program control types.</span></span> |


<!-- {
  "type": "#page.annotation",
  "description": "Create programControl",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
