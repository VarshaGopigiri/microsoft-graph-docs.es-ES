---
title: Enumerar blocs de notas
description: Recupera una lista de objetos notebook.
ms.openlocfilehash: 0f9bf502973be0d178db70e42f25a0716263e323
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085389"
---
# <a name="list-notebooks"></a><span data-ttu-id="361f4-103">Enumerar blocs de notas</span><span class="sxs-lookup"><span data-stu-id="361f4-103">List notebooks</span></span>

> <span data-ttu-id="361f4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="361f4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="361f4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="361f4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="361f4-106">Recupera una lista de objetos [notebook](../resources/notebook.md).</span><span class="sxs-lookup"><span data-stu-id="361f4-106">Retrieve a list of [notebook](../resources/notebook.md) objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="361f4-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="361f4-107">Permissions</span></span>
<span data-ttu-id="361f4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="361f4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="361f4-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="361f4-110">Permission type</span></span>      | <span data-ttu-id="361f4-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="361f4-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="361f4-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="361f4-112">Delegated (work or school account)</span></span> | <span data-ttu-id="361f4-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="361f4-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="361f4-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="361f4-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="361f4-115">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="361f4-115">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="361f4-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="361f4-116">Application</span></span> | <span data-ttu-id="361f4-117">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="361f4-117">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="361f4-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="361f4-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/notebooks
GET /users/{id | userPrincipalName}/onenote/notebooks
GET /groups/{id}/onenote/notebooks
GET /sites/{id}/onenote/notebooks
```
## <a name="optional-query-parameters"></a><span data-ttu-id="361f4-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="361f4-119">Optional query parameters</span></span>
<span data-ttu-id="361f4-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="361f4-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="361f4-121">El criterio de ordenación predeterminado es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="361f4-121">The default sort order is `name asc`.</span></span> 

<span data-ttu-id="361f4-122">`sections` y `sectionGroups` son valores de `expand` para los blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="361f4-122">Valid `expand` values for notebooks are `sections` and `sectionGroups`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="361f4-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="361f4-123">Request headers</span></span>
| <span data-ttu-id="361f4-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="361f4-124">Name</span></span>       | <span data-ttu-id="361f4-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="361f4-125">Type</span></span> | <span data-ttu-id="361f4-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="361f4-126">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="361f4-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="361f4-127">Authorization</span></span>  | <span data-ttu-id="361f4-128">string</span><span class="sxs-lookup"><span data-stu-id="361f4-128">string</span></span>  | <span data-ttu-id="361f4-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="361f4-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="361f4-131">Aceptar</span><span class="sxs-lookup"><span data-stu-id="361f4-131">Accept</span></span> | <span data-ttu-id="361f4-132">string</span><span class="sxs-lookup"><span data-stu-id="361f4-132">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="361f4-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="361f4-133">Request body</span></span>
<span data-ttu-id="361f4-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="361f4-134">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="361f4-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="361f4-135">Response</span></span>

<span data-ttu-id="361f4-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [notebook](../resources/notebook.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="361f4-136">If successful, this method returns a `200 OK` response code and collection of [notebook](../resources/notebook.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="361f4-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="361f4-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="361f4-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="361f4-138">Request</span></span>
<span data-ttu-id="361f4-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="361f4-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_notebooks"
}-->
```http
GET https://graph.microsoft.com/beta/me/onenote/notebooks
```
##### <a name="response"></a><span data-ttu-id="361f4-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="361f4-140">Response</span></span>
<span data-ttu-id="361f4-p104">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="361f4-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
      "id": "8fcb5dbc-d5aa-4681-8e31-b001d5168d79",
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