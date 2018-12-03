---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Crear una lista de SharePoint
ms.openlocfilehash: a1e247722e9e8874a78a1951619e08bff9bd36e8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090527"
---
# <a name="create-a-new-list"></a><span data-ttu-id="6edbf-102">Crear una lista</span><span class="sxs-lookup"><span data-stu-id="6edbf-102">Create a new list</span></span>

> <span data-ttu-id="6edbf-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6edbf-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6edbf-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6edbf-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6edbf-105">Cree una [list][] en un [site][].</span><span class="sxs-lookup"><span data-stu-id="6edbf-105">Create a new [list][] in a [site][].</span></span>

## <a name="permissions"></a><span data-ttu-id="6edbf-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="6edbf-106">Permissions</span></span>

<span data-ttu-id="6edbf-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6edbf-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|            <span data-ttu-id="6edbf-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6edbf-109">Permission type</span></span>             | <span data-ttu-id="6edbf-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6edbf-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="6edbf-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6edbf-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="6edbf-112">Sites.Manage.All</span><span class="sxs-lookup"><span data-stu-id="6edbf-112">Sites.Manage.All</span></span>                            |
| <span data-ttu-id="6edbf-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6edbf-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6edbf-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6edbf-114">Not supported.</span></span>                              |
| <span data-ttu-id="6edbf-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6edbf-115">Application</span></span>                            | <span data-ttu-id="6edbf-116">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6edbf-116">Sites.ReadWrite.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="6edbf-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6edbf-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST https://graph.microsoft.com/beta/sites/{site-id}/lists
```

## <a name="request-body"></a><span data-ttu-id="6edbf-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6edbf-118">Request body</span></span>

<span data-ttu-id="6edbf-119">En el cuerpo de la solicitud, proporcione una representación JSON del recurso [list][] que quiere crear.</span><span class="sxs-lookup"><span data-stu-id="6edbf-119">In the request body, supply a JSON representation of the [list][] resource to create.</span></span>

## <a name="example"></a><span data-ttu-id="6edbf-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6edbf-120">Example</span></span>

<span data-ttu-id="6edbf-121">Aquí se muestra un ejemplo de cómo crear una lista genérica.</span><span class="sxs-lookup"><span data-stu-id="6edbf-121">Here is an example of how to create a new generic list.</span></span>

<!-- { "blockType": "request", "name": "create-list", "scopes": "sites.readwrite.all" } -->

```http
POST /sites/{site-id}/lists
Content-Type: application/json

{
  "name": "Books",
  "columns": [
    {
      "name": "Author",
      "text": { }
    },
    {
      "name": "PageCount",
      "number": { }
    }
  ],
  "list": {
    "template": "genericList"
  }
}
```

<span data-ttu-id="6edbf-122">**Nota**: Las columnas personalizadas son opcionales.</span><span class="sxs-lookup"><span data-stu-id="6edbf-122">**Note:** Custom columns are optional.</span></span>

<span data-ttu-id="6edbf-123">Además de las columnas especificadas aquí, se crean listas con columnas definidas en la **plantilla** de referencia.</span><span class="sxs-lookup"><span data-stu-id="6edbf-123">In addition to any columns specified here, new lists are created with columns defined in the referenced **template**.</span></span>
<span data-ttu-id="6edbf-124">Si la faceta **list** o la **plantilla** están sin especificar, el valor predeterminado de la lista es la plantilla `genericList`, que incluye una columna _Título_.</span><span class="sxs-lookup"><span data-stu-id="6edbf-124">If the **list** facet or **template** is unspecified, the list defaults to the `genericList` template, which includes a _Title_ column.</span></span>

## <a name="response"></a><span data-ttu-id="6edbf-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6edbf-125">Response</span></span>

<span data-ttu-id="6edbf-126">Si se realiza correctamente, este método devuelve un valor [list][] en el cuerpo de la respuesta de la lista creada.</span><span class="sxs-lookup"><span data-stu-id="6edbf-126">If successful, this method returns a [list][] in the response body for the created list.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.list", "truncated": true } -->

```json
HTTP/1.1 201 Created
Content-type: application/json

{
  "id": "22e03ef3-6ef4-424d-a1d3-92a337807c30",
  "createdDateTime": "2017-04-30T01:21:00Z",
  "createdBy": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "8606e4d5-d582-4f5f-aeba-7d7c18b20cfd"
    }
  },
  "lastModifiedDateTime": "2016-08-30T08:26:00Z",
  "lastModifiedBy": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "8606e4d5-d582-4f5f-aeba-7d7c18b20cfd"
    }
  }
}
```

<span data-ttu-id="6edbf-127">**Nota:** El objeto Response se trunca para obtener una mayor claridad.</span><span class="sxs-lookup"><span data-stu-id="6edbf-127">**Note:** The response object is truncated for clarity.</span></span>
<span data-ttu-id="6edbf-128">Se devolverán las propiedades predeterminadas de la llamada actual.</span><span class="sxs-lookup"><span data-stu-id="6edbf-128">Default properties will be returned from the actual call.</span></span>

[list]: ../resources/list.md
[site]: ../resources/site.md

<!-- {
  "type": "#page.annotation",
  "description": "Create a new SharePoint list.",
  "keywords": "",
  "section": "documentation",
  "tocPath": "List/Create"
} -->