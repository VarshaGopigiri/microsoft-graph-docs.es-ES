---
title: Programas de lista
description: Lista todos los objetos de programa, en Azure AD tener acceso a la característica de revisiones.
localization_priority: Normal
ms.openlocfilehash: 9ea71e5377b7dcfe7ca6de7cfaf221e2c6dfcd98
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876296"
---
# <a name="list-programs"></a><span data-ttu-id="b384e-103">Programas de lista</span><span class="sxs-lookup"><span data-stu-id="b384e-103">List programs</span></span>

> <span data-ttu-id="b384e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b384e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b384e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b384e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b384e-106">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, incluya a todos los objetos de [programa](../resources/program.md) .</span><span class="sxs-lookup"><span data-stu-id="b384e-106">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, list all the [program](../resources/program.md) objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="b384e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b384e-107">Permissions</span></span>
<span data-ttu-id="b384e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b384e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b384e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b384e-110">Permission type</span></span>                        | <span data-ttu-id="b384e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b384e-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="b384e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b384e-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="b384e-113">`ProgramControl.Read.All`, `ProgramControl.ReadWrite.All`.</span><span class="sxs-lookup"><span data-stu-id="b384e-113"></span></span>  <span data-ttu-id="b384e-114">También debe ser el usuario iniciado en un rol de Active directory que le permita leer un programa.</span><span class="sxs-lookup"><span data-stu-id="b384e-114">The signed in user must also be in a directory role which permits them to read a program.</span></span> |
|<span data-ttu-id="b384e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b384e-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b384e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b384e-116">Not supported.</span></span> |
|<span data-ttu-id="b384e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b384e-117">Application</span></span>                            | <span data-ttu-id="b384e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b384e-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b384e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b384e-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /programs
```
## <a name="request-headers"></a><span data-ttu-id="b384e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b384e-120">Request headers</span></span>
| <span data-ttu-id="b384e-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="b384e-121">Name</span></span>         | <span data-ttu-id="b384e-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="b384e-122">Type</span></span>        | <span data-ttu-id="b384e-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="b384e-123">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="b384e-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="b384e-124">Authorization</span></span> | <span data-ttu-id="b384e-125">string</span><span class="sxs-lookup"><span data-stu-id="b384e-125">string</span></span> | <span data-ttu-id="b384e-126">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="b384e-126">Bearer \{token\}.</span></span> <span data-ttu-id="b384e-127">Necesario.</span><span class="sxs-lookup"><span data-stu-id="b384e-127">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b384e-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b384e-128">Request body</span></span>
<span data-ttu-id="b384e-129">No se debe suministrar ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b384e-129">No request body should be supplied.</span></span>

## <a name="response"></a><span data-ttu-id="b384e-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b384e-130">Response</span></span>
<span data-ttu-id="b384e-131">Si tiene éxito, este método devuelve una `200, OK` código de respuesta y una matriz de objetos de [programa](../resources/program.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b384e-131">If successful, this method returns a `200, OK` response code and an array of [program](../resources/program.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b384e-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b384e-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b384e-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b384e-133">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_program"
}-->
```http
GET https://graph.microsoft.com/beta/programs
```

##### <a name="response"></a><span data-ttu-id="b384e-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b384e-134">Response</span></span>
><span data-ttu-id="b384e-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b384e-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="b384e-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="b384e-137">See also</span></span>

| <span data-ttu-id="b384e-138">Método</span><span class="sxs-lookup"><span data-stu-id="b384e-138">Method</span></span>           | <span data-ttu-id="b384e-139">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b384e-139">Return Type</span></span>    |<span data-ttu-id="b384e-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="b384e-140">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="b384e-141">ProgramControls de lista de un programa</span><span class="sxs-lookup"><span data-stu-id="b384e-141">List programControls of a program</span></span>](program-listcontrols.md) |     <span data-ttu-id="b384e-142">colección de [programControl](../resources/programcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="b384e-142">[programControl](../resources/programcontrol.md) collection</span></span>|    <span data-ttu-id="b384e-143">Obtener una colección de los controles de un programa.</span><span class="sxs-lookup"><span data-stu-id="b384e-143">Get a collection of the controls of a program.</span></span>|


<!-- {
  "type": "#page.annotation",
  "description": "List programs",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
