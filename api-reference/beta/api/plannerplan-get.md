---
title: Obtener plannerPlan
description: Recuperar las propiedades y las relaciones del objeto **plannerplan**.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: c0829abece86627c04d05ba4f56bf71d619fd5ae
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27955593"
---
# <a name="get-plannerplan"></a><span data-ttu-id="fc65d-103">Obtener plannerPlan</span><span class="sxs-lookup"><span data-stu-id="fc65d-103">Get plannerPlan</span></span>

> <span data-ttu-id="fc65d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fc65d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fc65d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fc65d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fc65d-106">Recuperar las propiedades y las relaciones del objeto **plannerplan**.</span><span class="sxs-lookup"><span data-stu-id="fc65d-106">Retrieve the properties and relationships of **plannerplan** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="fc65d-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="fc65d-107">Permissions</span></span>
<span data-ttu-id="fc65d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fc65d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fc65d-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fc65d-110">Permission type</span></span>      | <span data-ttu-id="fc65d-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fc65d-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fc65d-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fc65d-112">Delegated (work or school account)</span></span> | <span data-ttu-id="fc65d-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fc65d-113">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="fc65d-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fc65d-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fc65d-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fc65d-115">Not supported.</span></span>    |
|<span data-ttu-id="fc65d-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fc65d-116">Application</span></span> | <span data-ttu-id="fc65d-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fc65d-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="fc65d-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fc65d-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /planner/plans/<id>
```
## <a name="request-headers"></a><span data-ttu-id="fc65d-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fc65d-119">Request headers</span></span>
| <span data-ttu-id="fc65d-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="fc65d-120">Name</span></span>      |<span data-ttu-id="fc65d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc65d-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="fc65d-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="fc65d-122">Authorization</span></span>  | <span data-ttu-id="fc65d-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fc65d-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="fc65d-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fc65d-125">Request body</span></span>
<span data-ttu-id="fc65d-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fc65d-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fc65d-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc65d-127">Response</span></span>

<span data-ttu-id="fc65d-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerPlan](../resources/plannerplan.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fc65d-128">If successful, this method returns a `200 OK` response code and [plannerPlan](../resources/plannerplan.md) object in the response body.</span></span>

<span data-ttu-id="fc65d-p104">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="fc65d-p104">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="fc65d-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fc65d-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fc65d-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fc65d-133">Request</span></span>
<span data-ttu-id="fc65d-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fc65d-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_plannerplan"
}-->
```http
GET https://graph.microsoft.com/beta/planner/plans/<id>
```
##### <a name="response"></a><span data-ttu-id="fc65d-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc65d-135">Response</span></span>
<span data-ttu-id="fc65d-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fc65d-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerPlan"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 357

{
  "createdBy": {
    "application": {
      "id": "95e27074-6c4a-447a-aa24-9d718a0b86fa"
    },
    "user": {
      "id": "ebf3b108-5234-4e22-b93d-656d7dae5874"
    }
  },
  "createdDateTime": "2015-03-30T18:36:49.2407981Z",
  "owner": "ebf3b108-5234-4e22-b93d-656d7dae5874",
  "title": "title-value",
  "id": "xqQg5FS2LkCp935s-FIFm2QAFkHM"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get plannerPlan",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
