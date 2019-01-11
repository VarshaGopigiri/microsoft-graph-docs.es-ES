---
title: Lista programControlTypes
description: Lista todos los objetos de programControlType, en Azure AD tener acceso a la característica de revisiones.
localization_priority: Normal
ms.openlocfilehash: ae5a2298d3c0f542f7d8fd766f412b8cf5648730
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860889"
---
# <a name="list-programcontroltypes"></a><span data-ttu-id="2a0aa-103">Lista programControlTypes</span><span class="sxs-lookup"><span data-stu-id="2a0aa-103">List programControlTypes</span></span>

> <span data-ttu-id="2a0aa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2a0aa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2a0aa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2a0aa-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2a0aa-106">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, incluya a todos los objetos de [programControlType](../resources/programcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="2a0aa-106">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, list all the [programControlType](../resources/programcontroltype.md) objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="2a0aa-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="2a0aa-107">Permissions</span></span>
<span data-ttu-id="2a0aa-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2a0aa-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2a0aa-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2a0aa-110">Permission type</span></span>                        | <span data-ttu-id="2a0aa-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2a0aa-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="2a0aa-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2a0aa-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="2a0aa-113">`ProgramControl.Read.All`, `ProgramControl.ReadWrite.All`.</span><span class="sxs-lookup"><span data-stu-id="2a0aa-113"></span></span>  <span data-ttu-id="2a0aa-114">También debe ser el usuario iniciado en un rol de Active directory que le permita leer un programa.</span><span class="sxs-lookup"><span data-stu-id="2a0aa-114">The signed in user must also be in a directory role which permits them to read a program.</span></span> |
|<span data-ttu-id="2a0aa-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2a0aa-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2a0aa-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2a0aa-116">Not supported.</span></span> |
|<span data-ttu-id="2a0aa-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2a0aa-117">Application</span></span>                            | <span data-ttu-id="2a0aa-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2a0aa-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="2a0aa-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2a0aa-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /programControlTypes
```
## <a name="request-headers"></a><span data-ttu-id="2a0aa-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2a0aa-120">Request headers</span></span>
| <span data-ttu-id="2a0aa-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="2a0aa-121">Name</span></span>         | <span data-ttu-id="2a0aa-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="2a0aa-122">Type</span></span>        | <span data-ttu-id="2a0aa-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a0aa-123">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="2a0aa-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="2a0aa-124">Authorization</span></span> | <span data-ttu-id="2a0aa-125">string</span><span class="sxs-lookup"><span data-stu-id="2a0aa-125">string</span></span> | <span data-ttu-id="2a0aa-126">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="2a0aa-126">Bearer \{token\}.</span></span> <span data-ttu-id="2a0aa-127">Necesario.</span><span class="sxs-lookup"><span data-stu-id="2a0aa-127">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2a0aa-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2a0aa-128">Request body</span></span>
<span data-ttu-id="2a0aa-129">No se debe suministrar ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2a0aa-129">No request body should be supplied.</span></span>

## <a name="response"></a><span data-ttu-id="2a0aa-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2a0aa-130">Response</span></span>
<span data-ttu-id="2a0aa-131">Si tiene éxito, este método devuelve una `200, OK` código de respuesta y una matriz de objetos de [programControlType](../resources/programcontroltype.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2a0aa-131">If successful, this method returns a `200, OK` response code and an array of [programControlType](../resources/programcontroltype.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2a0aa-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2a0aa-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2a0aa-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2a0aa-133">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_programcontroltype"
}-->
```http
GET https://graph.microsoft.com/beta/programControlTypes
```

##### <a name="response"></a><span data-ttu-id="2a0aa-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2a0aa-134">Response</span></span>
><span data-ttu-id="2a0aa-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2a0aa-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="2a0aa-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a0aa-137">See also</span></span>

| <span data-ttu-id="2a0aa-138">Método</span><span class="sxs-lookup"><span data-stu-id="2a0aa-138">Method</span></span>           | <span data-ttu-id="2a0aa-139">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a0aa-139">Return Type</span></span>    |<span data-ttu-id="2a0aa-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a0aa-140">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="2a0aa-141">ProgramControls de lista de un programa</span><span class="sxs-lookup"><span data-stu-id="2a0aa-141">List programControls of a program</span></span>](program-listcontrols.md) |     <span data-ttu-id="2a0aa-142">colección de [programControl](../resources/programcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="2a0aa-142">[programControl](../resources/programcontrol.md) collection</span></span>|    <span data-ttu-id="2a0aa-143">Obtener una colección de los controles de un programa.</span><span class="sxs-lookup"><span data-stu-id="2a0aa-143">Get a collection of the controls of a program.</span></span>|


<!-- {
  "type": "#page.annotation",
  "description": "List program control types",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
