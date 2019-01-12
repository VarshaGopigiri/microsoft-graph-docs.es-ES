---
title: Enumerar blocs de notas
description: Recupera una lista de objetos notebook.
author: jewan-microsoft
localization_priority: Priority
ms.prod: onenote
ms.openlocfilehash: b66b059d92b1177a6c2b5df9a9d978eb87dec53e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27975487"
---
# <a name="list-notebooks"></a><span data-ttu-id="1796e-103">Enumerar blocs de notas</span><span class="sxs-lookup"><span data-stu-id="1796e-103">List notebooks</span></span>

<span data-ttu-id="1796e-104">Recupera una lista de objetos [notebook](../resources/notebook.md).</span><span class="sxs-lookup"><span data-stu-id="1796e-104">Retrieve a list of [notebook](../resources/notebook.md) objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="1796e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="1796e-105">Permissions</span></span>
<span data-ttu-id="1796e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1796e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1796e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1796e-108">Permission type</span></span>      | <span data-ttu-id="1796e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1796e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1796e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1796e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="1796e-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1796e-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="1796e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1796e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1796e-113">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1796e-113">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="1796e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1796e-114">Application</span></span> | <span data-ttu-id="1796e-115">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1796e-115">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="1796e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1796e-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/notebooks
GET /users/{id | userPrincipalName}/onenote/notebooks
GET /groups/{id}/onenote/notebooks
GET /sites/{id}/onenote/notebooks
```
## <a name="optional-query-parameters"></a><span data-ttu-id="1796e-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1796e-117">Optional query parameters</span></span>
<span data-ttu-id="1796e-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1796e-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="1796e-119">El criterio de ordenación predeterminado es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="1796e-119">The default sort order is `name asc`.</span></span> 

<span data-ttu-id="1796e-120">`sections` y `sectionGroups` son valores de `expand` para los blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="1796e-120">Valid `expand` values for notebooks are `sections` and `sectionGroups`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="1796e-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1796e-121">Request headers</span></span>
| <span data-ttu-id="1796e-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="1796e-122">Name</span></span>       | <span data-ttu-id="1796e-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="1796e-123">Type</span></span> | <span data-ttu-id="1796e-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="1796e-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="1796e-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="1796e-125">Authorization</span></span>  | <span data-ttu-id="1796e-126">string</span><span class="sxs-lookup"><span data-stu-id="1796e-126">string</span></span>  | <span data-ttu-id="1796e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1796e-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1796e-129">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1796e-129">Accept</span></span> | <span data-ttu-id="1796e-130">string</span><span class="sxs-lookup"><span data-stu-id="1796e-130">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="1796e-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1796e-131">Request body</span></span>
<span data-ttu-id="1796e-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1796e-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1796e-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1796e-133">Response</span></span>

<span data-ttu-id="1796e-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [notebook](../resources/notebook.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1796e-134">If successful, this method returns a `200 OK` response code and collection of [notebook](../resources/notebook.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="1796e-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1796e-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1796e-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1796e-136">Request</span></span>
<span data-ttu-id="1796e-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1796e-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_notebooks"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/notebooks
```
##### <a name="response"></a><span data-ttu-id="1796e-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1796e-138">Response</span></span>
<span data-ttu-id="1796e-p103">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1796e-p103">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.notebook",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 369

{
  "value": [
    {
      "isDefault": true,
      "userRole": {
      },
      "isShared": true,
      "sectionsUrl": "sectionsUrl-value",
      "sectionGroupsUrl": "sectionGroupsUrl-value",
      "links": {
        "oneNoteClientUrl": {
          "href": "href-value"
        },
        "oneNoteWebUrl": {
          "href": "href-value"
        }
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List notebooks",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
