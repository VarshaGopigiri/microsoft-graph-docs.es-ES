---
title: Lista businessFlowTemplates
description: Lista todos los objetos de businessFlowTemplate, en Azure AD tener acceso a la característica de revisiones.
ms.openlocfilehash: 9c6dc976244c60151cb2c230430ab6b4d0dc4b43
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083708"
---
# <a name="list-businessflowtemplates"></a><span data-ttu-id="dc731-103">Lista businessFlowTemplates</span><span class="sxs-lookup"><span data-stu-id="dc731-103">List businessFlowTemplates</span></span>

> <span data-ttu-id="dc731-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dc731-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dc731-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dc731-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="dc731-106">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, incluya a todos los objetos de [businessFlowTemplate](../resources/businessflowtemplate.md) .</span><span class="sxs-lookup"><span data-stu-id="dc731-106">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, list all the [businessFlowTemplate](../resources/businessflowtemplate.md) objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="dc731-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="dc731-107">Permissions</span></span>
<span data-ttu-id="dc731-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dc731-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dc731-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dc731-110">Permission type</span></span>                        | <span data-ttu-id="dc731-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dc731-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="dc731-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dc731-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="dc731-113">`AccessReview.Read.All`, `AccessReview.ReadWrite.All`.</span><span class="sxs-lookup"><span data-stu-id="dc731-113"></span></span>  <span data-ttu-id="dc731-114">También debe ser el usuario iniciado en un rol de Active directory que le permita leer una revisión de acceso.</span><span class="sxs-lookup"><span data-stu-id="dc731-114">The signed in user must also be in a directory role which permits them to read an access review.</span></span> |
|<span data-ttu-id="dc731-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dc731-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dc731-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dc731-116">Not supported.</span></span> |
|<span data-ttu-id="dc731-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dc731-117">Application</span></span>                            | <span data-ttu-id="dc731-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dc731-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="dc731-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dc731-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /businessFlowTemplates
```
## <a name="request-headers"></a><span data-ttu-id="dc731-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dc731-120">Request headers</span></span>
| <span data-ttu-id="dc731-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="dc731-121">Name</span></span>         | <span data-ttu-id="dc731-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc731-122">Type</span></span>        | <span data-ttu-id="dc731-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc731-123">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="dc731-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="dc731-124">Authorization</span></span> | <span data-ttu-id="dc731-125">string</span><span class="sxs-lookup"><span data-stu-id="dc731-125">string</span></span> | <span data-ttu-id="dc731-126">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="dc731-126">Bearer \{token\}.</span></span> <span data-ttu-id="dc731-127">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dc731-127">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="dc731-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dc731-128">Request body</span></span>
<span data-ttu-id="dc731-129">No se debe suministrar ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dc731-129">No request body should be supplied.</span></span>

## <a name="response"></a><span data-ttu-id="dc731-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dc731-130">Response</span></span>
<span data-ttu-id="dc731-131">Si tiene éxito, este método devuelve una `200, OK` código de respuesta y una matriz de objetos de [businessFlowTemplate](../resources/businessflowtemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dc731-131">If successful, this method returns a `200, OK` response code and an array of [businessFlowTemplate](../resources/businessflowtemplate.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dc731-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dc731-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="dc731-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dc731-133">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_businesFlowTemplate"
}-->
```http
GET https://graph.microsoft.com/beta/businesFlowTemplates
```

##### <a name="response"></a><span data-ttu-id="dc731-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dc731-134">Response</span></span>
><span data-ttu-id="dc731-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dc731-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.businessFlowTemplate",
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

## <a name="see-also"></a><span data-ttu-id="dc731-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc731-137">See also</span></span>

| <span data-ttu-id="dc731-138">Método</span><span class="sxs-lookup"><span data-stu-id="dc731-138">Method</span></span>           | <span data-ttu-id="dc731-139">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc731-139">Return Type</span></span>    |<span data-ttu-id="dc731-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc731-140">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="dc731-141">Crear accessReview</span><span class="sxs-lookup"><span data-stu-id="dc731-141">Create accessReview</span></span>](accessreview-create.md) |    [<span data-ttu-id="dc731-142">accessReview</span><span class="sxs-lookup"><span data-stu-id="dc731-142">accessReview</span></span>](../resources/accessreview.md) |  <span data-ttu-id="dc731-143">Crear un nuevo accessReview.</span><span class="sxs-lookup"><span data-stu-id="dc731-143">Create a new accessReview.</span></span> |




<!-- {
  "type": "#page.annotation",
  "description": "List business flow template",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
