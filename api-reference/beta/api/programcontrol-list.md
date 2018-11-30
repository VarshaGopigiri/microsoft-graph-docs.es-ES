---
title: Lista programControls
description: En la característica de revisiones de access Azure AD, incluya todos los objetos de programControl, a través de todos los programas en el inquilino.
ms.openlocfilehash: 7e1dcb197a546e3aa823b731a9e7954803b36c2a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084136"
---
# <a name="list-programcontrols"></a><span data-ttu-id="a3faa-103">Lista programControls</span><span class="sxs-lookup"><span data-stu-id="a3faa-103">List programControls</span></span>

> <span data-ttu-id="a3faa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a3faa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a3faa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a3faa-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a3faa-106">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, incluya todos los objetos de [programControl](../resources/programcontrol.md) , a través de todos los programas en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="a3faa-106">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, list all the [programControl](../resources/programcontrol.md) objects, across all programs in the tenant.</span></span>
## <a name="permissions"></a><span data-ttu-id="a3faa-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a3faa-107">Permissions</span></span>
<span data-ttu-id="a3faa-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a3faa-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a3faa-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a3faa-110">Permission type</span></span>                        | <span data-ttu-id="a3faa-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a3faa-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="a3faa-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a3faa-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="a3faa-113">`ProgramControl.Read.All`, `ProgramControl.ReadWrite.All`.</span><span class="sxs-lookup"><span data-stu-id="a3faa-113"></span></span>  <span data-ttu-id="a3faa-114">También debe ser el usuario iniciado en un rol de Active directory que le permita leer un programa.</span><span class="sxs-lookup"><span data-stu-id="a3faa-114">The signed in user must also be in a directory role which permits them to read a program.</span></span> |
|<span data-ttu-id="a3faa-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a3faa-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a3faa-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a3faa-116">Not supported.</span></span> |
|<span data-ttu-id="a3faa-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a3faa-117">Application</span></span>                            | <span data-ttu-id="a3faa-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a3faa-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a3faa-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a3faa-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /programControls
```
## <a name="request-headers"></a><span data-ttu-id="a3faa-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a3faa-120">Request headers</span></span>
| <span data-ttu-id="a3faa-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="a3faa-121">Name</span></span>         | <span data-ttu-id="a3faa-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="a3faa-122">Type</span></span>        | <span data-ttu-id="a3faa-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3faa-123">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="a3faa-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="a3faa-124">Authorization</span></span> | <span data-ttu-id="a3faa-125">string</span><span class="sxs-lookup"><span data-stu-id="a3faa-125">string</span></span> | <span data-ttu-id="a3faa-126">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="a3faa-126">Bearer \{token\}.</span></span> <span data-ttu-id="a3faa-127">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a3faa-127">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a3faa-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a3faa-128">Request body</span></span>
<span data-ttu-id="a3faa-129">No se debe suministrar ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a3faa-129">No request body should be supplied.</span></span>

## <a name="response"></a><span data-ttu-id="a3faa-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a3faa-130">Response</span></span>
<span data-ttu-id="a3faa-131">Si tiene éxito, este método devuelve una `200, OK` código de respuesta y una matriz de objetos de [programControl](../resources/programcontrol.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a3faa-131">If successful, this method returns a `200, OK` response code and an array of [programControl](../resources/programcontrol.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a3faa-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a3faa-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a3faa-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a3faa-133">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_programControl"
}-->
```http
GET https://graph.microsoft.com/beta/programControls
```

##### <a name="response"></a><span data-ttu-id="a3faa-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a3faa-134">Response</span></span>
><span data-ttu-id="a3faa-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a3faa-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.programControl",
    "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{

    "value": [
        {
            "id": "f6abf8ef-a05e-4788-adc9-5af909c400af",
            "controlId": "bc81d51d-be53-4606-a8c2-f90a2beb5f40",
            "programId": "673a7379-9c38-4f01-bd9d-4fda7260b807",
            "controlTypeId": "6e4f3d20-c5c3-407f-9695-8460952bcc68",
            "displayName": "guest user review",
            "status": "Completed",
            "createdDateTime": "2017-09-20T20:18:05.1318394Z"
        }
    ]
}

```

## <a name="see-also"></a><span data-ttu-id="a3faa-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3faa-137">See also</span></span>

| <span data-ttu-id="a3faa-138">Método</span><span class="sxs-lookup"><span data-stu-id="a3faa-138">Method</span></span>           | <span data-ttu-id="a3faa-139">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3faa-139">Return Type</span></span>    |<span data-ttu-id="a3faa-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3faa-140">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="a3faa-141">ProgramControls de lista de un programa</span><span class="sxs-lookup"><span data-stu-id="a3faa-141">List programControls of a program</span></span>](program-listcontrols.md) |     <span data-ttu-id="a3faa-142">colección de [programControl](../resources/programcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="a3faa-142">[programControl](../resources/programcontrol.md) collection</span></span>|    <span data-ttu-id="a3faa-143">Obtener una colección de los controles de un programa.</span><span class="sxs-lookup"><span data-stu-id="a3faa-143">Get a collection of the controls of a program.</span></span>|


<!-- {
  "type": "#page.annotation",
  "description": "List programControls",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
