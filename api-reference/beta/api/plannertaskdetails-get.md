---
title: Get plannerTaskDetails
description: Recuperar las propiedades y las relaciones del objeto **plannertaskdetails**.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 813f6ae2cdeac0e3b3797e7abdfc435d5bbb4a71
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27975632"
---
# <a name="get-plannertaskdetails"></a><span data-ttu-id="5f151-103">Get plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="5f151-103">Get plannerTaskDetails</span></span>

> <span data-ttu-id="5f151-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5f151-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5f151-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5f151-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5f151-106">Recuperar las propiedades y las relaciones del objeto **plannertaskdetails**.</span><span class="sxs-lookup"><span data-stu-id="5f151-106">Retrieve the properties and relationships of **plannertaskdetails** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="5f151-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5f151-107">Permissions</span></span>
<span data-ttu-id="5f151-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5f151-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5f151-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5f151-110">Permission type</span></span>      | <span data-ttu-id="5f151-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5f151-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5f151-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5f151-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5f151-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5f151-113">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="5f151-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5f151-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5f151-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5f151-115">Not supported.</span></span>    |
|<span data-ttu-id="5f151-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5f151-116">Application</span></span> | <span data-ttu-id="5f151-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5f151-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="5f151-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5f151-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /planner/tasks/<id>/details
```

## <a name="request-headers"></a><span data-ttu-id="5f151-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5f151-119">Request headers</span></span>
| <span data-ttu-id="5f151-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="5f151-120">Name</span></span>      |<span data-ttu-id="5f151-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f151-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="5f151-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="5f151-122">Authorization</span></span>  | <span data-ttu-id="5f151-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5f151-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="5f151-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5f151-125">Request body</span></span>
<span data-ttu-id="5f151-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5f151-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5f151-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f151-127">Response</span></span>

<span data-ttu-id="5f151-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerTaskDetails](../resources/plannertaskdetails.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f151-128">If successful, this method returns a `200 OK` response code and [plannerTaskDetails](../resources/plannertaskdetails.md) object in the response body.</span></span>

<span data-ttu-id="5f151-p104">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="5f151-p104">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="5f151-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5f151-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5f151-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5f151-133">Request</span></span>
<span data-ttu-id="5f151-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5f151-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_plannertaskdetails"
}-->
```http
GET https://graph.microsoft.com/beta/planner/tasks/gcrYAaAkgU2EQUvpkNNXLGQAGTtu/details
```
##### <a name="response"></a><span data-ttu-id="5f151-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f151-135">Response</span></span>
<span data-ttu-id="5f151-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5f151-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerTaskDetails"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1036

{
  "description": "Task details properties:\nchecklist:Sub items\nreferences:Related links",
  "previewType": "automatic",
  "references": {
    "https%3A//developer%2Emicrosoft%2Ecom/en-us/graph/graph-explorer": {
      "@odata.type": "#microsoft.graph.plannerExternalReference",
      "alias": "Graph Explorer",
      "type": "Other",
      "previewPriority": "0009005706180391122",
      "lastModifiedBy": {
        "user": {
          "id": "fbab97d0-4932-4511-b675-204639209557"
        }
      },
      "lastModifiedDateTime": "2017-04-24T22:52:29.814Z"
    }
  },
  "checklist": {
    "d280ed1a-9f6b-4f9c-a962-fb4d00dc50ff": {
      "@odata.type": "#microsoft.graph.plannerChecklistItem",
      "isChecked": false,
      "title": "Try reading task details",
      "orderHint": "8587094707721254251P]",
      "lastModifiedBy": {
        "user": {
          "id": "e396de0e-4812-4fcb-9f9e-0358744df343"
        }
      },
      "lastModifiedDateTime": "2017-04-14T02:16:14.866Z"
    }
  },
  "id": "gcrYAaAkgU2EQUvpkNNXLGQAGTtu"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get plannerTaskDetails",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
