---
title: Crear bloc de notas
description: Crea un bloc de notas de OneNote.
ms.openlocfilehash: 38e92f402b5372292cdd30ed60cae81c1e0d46cc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031627"
---
# <a name="create-notebook"></a><span data-ttu-id="1d3ec-103">Crear bloc de notas</span><span class="sxs-lookup"><span data-stu-id="1d3ec-103">Create notebook</span></span>

<span data-ttu-id="1d3ec-104">Crea un [bloc de notas](../resources/notebook.md) de OneNote.</span><span class="sxs-lookup"><span data-stu-id="1d3ec-104">Create a new OneNote [notebook](../resources/notebook.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="1d3ec-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="1d3ec-105">Permissions</span></span>
<span data-ttu-id="1d3ec-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1d3ec-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1d3ec-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1d3ec-108">Permission type</span></span>      | <span data-ttu-id="1d3ec-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1d3ec-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1d3ec-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1d3ec-110">Delegated (work or school account)</span></span> | <span data-ttu-id="1d3ec-111">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1d3ec-111">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="1d3ec-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1d3ec-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1d3ec-113">Notes.Create, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1d3ec-113">Notes.Create, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="1d3ec-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1d3ec-114">Application</span></span> | <span data-ttu-id="1d3ec-115">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1d3ec-115">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="1d3ec-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1d3ec-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/notebooks
POST /users/{id | userPrincipalName}/onenote/notebooks
POST /groups/{id}/onenote/notebooks
POST /sites/{id}/onenote/notebooks
```
## <a name="request-headers"></a><span data-ttu-id="1d3ec-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1d3ec-117">Request headers</span></span>
| <span data-ttu-id="1d3ec-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="1d3ec-118">Name</span></span>       | <span data-ttu-id="1d3ec-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d3ec-119">Type</span></span> | <span data-ttu-id="1d3ec-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d3ec-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="1d3ec-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="1d3ec-121">Authorization</span></span>  | <span data-ttu-id="1d3ec-122">string</span><span class="sxs-lookup"><span data-stu-id="1d3ec-122">string</span></span>  | <span data-ttu-id="1d3ec-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1d3ec-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1d3ec-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1d3ec-125">Content-Type</span></span> | <span data-ttu-id="1d3ec-126">string</span><span class="sxs-lookup"><span data-stu-id="1d3ec-126">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="1d3ec-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1d3ec-127">Request body</span></span>
<span data-ttu-id="1d3ec-128">En el cuerpo de la solicitud, asigne un nombre al bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="1d3ec-128">In the request body, supply a name for the notebook.</span></span> 

<span data-ttu-id="1d3ec-p103">Los nombres del bloc de notas deben ser únicos. El nombre no puede contener más de 128 caracteres ni los caracteres siguientes: ?\*\/:<>|'"</span><span class="sxs-lookup"><span data-stu-id="1d3ec-p103">Notebook names must be unique. The name cannot contain more than 128 characters or contain the following characters:  ?\*\/:<>|'"</span></span>

## <a name="response"></a><span data-ttu-id="1d3ec-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d3ec-131">Response</span></span>

<span data-ttu-id="1d3ec-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el nuevo objeto [notebook](../resources/notebook.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d3ec-132">If successful, this method returns a `201 Created` response code and the new [notebook](../resources/notebook.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1d3ec-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1d3ec-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1d3ec-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1d3ec-134">Request</span></span>
<span data-ttu-id="1d3ec-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d3ec-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_notebook_from_onenote"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/notebooks
Content-type: application/json
Content-length: 30

{
  "displayName": "Notebook name"
}
```

##### <a name="response"></a><span data-ttu-id="1d3ec-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d3ec-136">Response</span></span>
<span data-ttu-id="1d3ec-p104">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1d3ec-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.notebook"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 284

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
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Notebook",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->