---
title: Programas de lista
description: Lista todos los objetos de programa, en Azure AD tener acceso a la característica de revisiones.
ms.openlocfilehash: fd934ec4dcfe4feb6167a6cf397be3669099c123
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084435"
---
# <a name="list-programs"></a><span data-ttu-id="001e0-103">Programas de lista</span><span class="sxs-lookup"><span data-stu-id="001e0-103">List programs</span></span>

> <span data-ttu-id="001e0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="001e0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="001e0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="001e0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="001e0-106">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, incluya a todos los objetos de [programa](../resources/program.md) .</span><span class="sxs-lookup"><span data-stu-id="001e0-106">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, list all the [program](../resources/program.md) objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="001e0-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="001e0-107">Permissions</span></span>
<span data-ttu-id="001e0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="001e0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="001e0-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="001e0-110">Permission type</span></span>                        | <span data-ttu-id="001e0-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="001e0-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="001e0-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="001e0-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="001e0-113">`ProgramControl.Read.All`, `ProgramControl.ReadWrite.All`.</span><span class="sxs-lookup"><span data-stu-id="001e0-113"></span></span>  <span data-ttu-id="001e0-114">También debe ser el usuario iniciado en un rol de Active directory que le permita leer un programa.</span><span class="sxs-lookup"><span data-stu-id="001e0-114">The signed in user must also be in a directory role which permits them to read a program.</span></span> |
|<span data-ttu-id="001e0-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="001e0-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="001e0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="001e0-116">Not supported.</span></span> |
|<span data-ttu-id="001e0-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="001e0-117">Application</span></span>                            | <span data-ttu-id="001e0-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="001e0-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="001e0-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="001e0-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /programs
```
## <a name="request-headers"></a><span data-ttu-id="001e0-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="001e0-120">Request headers</span></span>
| <span data-ttu-id="001e0-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="001e0-121">Name</span></span>         | <span data-ttu-id="001e0-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="001e0-122">Type</span></span>        | <span data-ttu-id="001e0-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="001e0-123">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="001e0-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="001e0-124">Authorization</span></span> | <span data-ttu-id="001e0-125">string</span><span class="sxs-lookup"><span data-stu-id="001e0-125">string</span></span> | <span data-ttu-id="001e0-126">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="001e0-126">Bearer \{token\}.</span></span> <span data-ttu-id="001e0-127">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="001e0-127">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="001e0-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="001e0-128">Request body</span></span>
<span data-ttu-id="001e0-129">No se debe suministrar ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="001e0-129">No request body should be supplied.</span></span>

## <a name="response"></a><span data-ttu-id="001e0-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="001e0-130">Response</span></span>
<span data-ttu-id="001e0-131">Si tiene éxito, este método devuelve una `200, OK` código de respuesta y una matriz de objetos de [programa](../resources/program.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="001e0-131">If successful, this method returns a `200, OK` response code and an array of [program](../resources/program.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="001e0-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="001e0-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="001e0-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="001e0-133">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_program"
}-->
```http
GET https://graph.microsoft.com/beta/programs
```

##### <a name="response"></a><span data-ttu-id="001e0-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="001e0-134">Response</span></span>
><span data-ttu-id="001e0-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="001e0-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.program",
    "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
        {
            "id": "7e59d237-2fb0-4e5d-b7bb-d4f9f9129213",
            "displayName": "testprogram3",
            "description": "test description"
        },
        {
            "id": "b4afdd74-b6cf-4239-9b08-dde9a91d18d2",
            "displayName": "Default Program",
            "description": "Built-in program to start managing access reviews"
        }
    ]
}

```

## <a name="see-also"></a><span data-ttu-id="001e0-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="001e0-137">See also</span></span>

| <span data-ttu-id="001e0-138">Método</span><span class="sxs-lookup"><span data-stu-id="001e0-138">Method</span></span>           | <span data-ttu-id="001e0-139">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="001e0-139">Return Type</span></span>    |<span data-ttu-id="001e0-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="001e0-140">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="001e0-141">ProgramControls de lista de un programa</span><span class="sxs-lookup"><span data-stu-id="001e0-141">List programControls of a program</span></span>](program-listcontrols.md) |     <span data-ttu-id="001e0-142">colección de [programControl](../resources/programcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="001e0-142">[programControl](../resources/programcontrol.md) collection</span></span>|    <span data-ttu-id="001e0-143">Obtener una colección de los controles de un programa.</span><span class="sxs-lookup"><span data-stu-id="001e0-143">Get a collection of the controls of a program.</span></span>|


<!-- {
  "type": "#page.annotation",
  "description": "List programs",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
