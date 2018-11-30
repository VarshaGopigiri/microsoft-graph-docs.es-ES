---
title: Lista programControlTypes
description: Lista todos los objetos de programControlType, en Azure AD tener acceso a la característica de revisiones.
ms.openlocfilehash: 9e3b8efccd8d8be96ef1295dfba1a5c2e329c756
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091113"
---
# <a name="list-programcontroltypes"></a><span data-ttu-id="bf026-103">Lista programControlTypes</span><span class="sxs-lookup"><span data-stu-id="bf026-103">List programControlTypes</span></span>

> <span data-ttu-id="bf026-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bf026-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bf026-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bf026-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bf026-106">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, incluya a todos los objetos de [programControlType](../resources/programcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="bf026-106">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, list all the [programControlType](../resources/programcontroltype.md) objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="bf026-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="bf026-107">Permissions</span></span>
<span data-ttu-id="bf026-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bf026-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bf026-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bf026-110">Permission type</span></span>                        | <span data-ttu-id="bf026-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bf026-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="bf026-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bf026-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="bf026-113">`ProgramControl.Read.All`, `ProgramControl.ReadWrite.All`.</span><span class="sxs-lookup"><span data-stu-id="bf026-113"></span></span>  <span data-ttu-id="bf026-114">También debe ser el usuario iniciado en un rol de Active directory que le permita leer un programa.</span><span class="sxs-lookup"><span data-stu-id="bf026-114">The signed in user must also be in a directory role which permits them to read a program.</span></span> |
|<span data-ttu-id="bf026-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bf026-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bf026-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bf026-116">Not supported.</span></span> |
|<span data-ttu-id="bf026-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bf026-117">Application</span></span>                            | <span data-ttu-id="bf026-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bf026-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="bf026-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bf026-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /programControlTypes
```
## <a name="request-headers"></a><span data-ttu-id="bf026-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bf026-120">Request headers</span></span>
| <span data-ttu-id="bf026-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="bf026-121">Name</span></span>         | <span data-ttu-id="bf026-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="bf026-122">Type</span></span>        | <span data-ttu-id="bf026-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf026-123">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="bf026-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="bf026-124">Authorization</span></span> | <span data-ttu-id="bf026-125">string</span><span class="sxs-lookup"><span data-stu-id="bf026-125">string</span></span> | <span data-ttu-id="bf026-126">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="bf026-126">Bearer \{token\}.</span></span> <span data-ttu-id="bf026-127">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bf026-127">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bf026-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bf026-128">Request body</span></span>
<span data-ttu-id="bf026-129">No se debe suministrar ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf026-129">No request body should be supplied.</span></span>

## <a name="response"></a><span data-ttu-id="bf026-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf026-130">Response</span></span>
<span data-ttu-id="bf026-131">Si tiene éxito, este método devuelve una `200, OK` código de respuesta y una matriz de objetos de [programControlType](../resources/programcontroltype.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf026-131">If successful, this method returns a `200, OK` response code and an array of [programControlType](../resources/programcontroltype.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bf026-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bf026-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bf026-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bf026-133">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_programcontroltype"
}-->
```http
GET https://graph.microsoft.com/beta/programControlTypes
```

##### <a name="response"></a><span data-ttu-id="bf026-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf026-134">Response</span></span>
><span data-ttu-id="bf026-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bf026-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.programControlType",
    "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value":[
        {
            "id": "842169fe-e1b7-4ce9-98b6-6a9db02eec6b",
            "displayName": "Access Reviews for External Users' access to groups"
        },
        {
            "id": "7fbc909b-efe1-4c72-8ae6-99cb30b882de",
            "displayName": "Access Reviews for External Users' access to applications"
        },
        {
            "id": "50839a84-e23c-44a7-a8cc-16e162afc656",
            "displayName": "Access Reviews for All Users' assignment to applications"
        },
        {
            "id": "6e4f3d20-c5c3-407f-9695-8460952bcc68",
            "displayName": "Access Reviews for Office 365 Groups' membership"
        }
    ]
}

```

## <a name="see-also"></a><span data-ttu-id="bf026-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf026-137">See also</span></span>

| <span data-ttu-id="bf026-138">Método</span><span class="sxs-lookup"><span data-stu-id="bf026-138">Method</span></span>           | <span data-ttu-id="bf026-139">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf026-139">Return Type</span></span>    |<span data-ttu-id="bf026-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf026-140">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="bf026-141">ProgramControls de lista de un programa</span><span class="sxs-lookup"><span data-stu-id="bf026-141">List programControls of a program</span></span>](program-listcontrols.md) |     <span data-ttu-id="bf026-142">colección de [programControl](../resources/programcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="bf026-142">[programControl](../resources/programcontrol.md) collection</span></span>|    <span data-ttu-id="bf026-143">Obtener una colección de los controles de un programa.</span><span class="sxs-lookup"><span data-stu-id="bf026-143">Get a collection of the controls of a program.</span></span>|


<!-- {
  "type": "#page.annotation",
  "description": "List program control types",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
