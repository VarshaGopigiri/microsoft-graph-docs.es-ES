---
title: Crear bloc de notas
description: Crea un bloc de notas de OneNote.
author: Jewan-microsoft
ms.openlocfilehash: e9290ed51f2ebf30cccaa8ecc82ab95767c9ed5c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27341604"
---
# <a name="create-notebook"></a><span data-ttu-id="5985c-103">Crear bloc de notas</span><span class="sxs-lookup"><span data-stu-id="5985c-103">Create notebook</span></span>

> <span data-ttu-id="5985c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5985c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5985c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5985c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5985c-106">Crea un [bloc de notas](../resources/notebook.md) de OneNote.</span><span class="sxs-lookup"><span data-stu-id="5985c-106">Create a new OneNote [notebook](../resources/notebook.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="5985c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5985c-107">Permissions</span></span>
<span data-ttu-id="5985c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5985c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5985c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5985c-110">Permission type</span></span>      | <span data-ttu-id="5985c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5985c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5985c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5985c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5985c-113">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5985c-113">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="5985c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5985c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5985c-115">Notes.Create, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5985c-115">Notes.Create, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="5985c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5985c-116">Application</span></span> | <span data-ttu-id="5985c-117">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5985c-117">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="5985c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5985c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/notebooks
POST /users/{id | userPrincipalName}/onenote/notebooks
POST /groups/{id}/onenote/notebooks
POST /sites/{id}/onenote/notebooks
```
## <a name="request-headers"></a><span data-ttu-id="5985c-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5985c-119">Request headers</span></span>
| <span data-ttu-id="5985c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="5985c-120">Name</span></span>       | <span data-ttu-id="5985c-121">Type</span><span class="sxs-lookup"><span data-stu-id="5985c-121">Type</span></span> | <span data-ttu-id="5985c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="5985c-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="5985c-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="5985c-123">Authorization</span></span>  | <span data-ttu-id="5985c-124">string</span><span class="sxs-lookup"><span data-stu-id="5985c-124">string</span></span>  | <span data-ttu-id="5985c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5985c-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="5985c-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="5985c-127">Content-Type</span></span> | <span data-ttu-id="5985c-128">string</span><span class="sxs-lookup"><span data-stu-id="5985c-128">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="5985c-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5985c-129">Request body</span></span>
<span data-ttu-id="5985c-130">En el cuerpo de la solicitud, asigne un nombre al bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="5985c-130">In the request body, supply a name for the notebook.</span></span> 

<span data-ttu-id="5985c-p104">Los nombres del bloc de notas deben ser únicos. El nombre no puede contener más de 128 caracteres ni los caracteres siguientes: ?\*\/:<>|'"</span><span class="sxs-lookup"><span data-stu-id="5985c-p104">Notebook names must be unique. The name cannot contain more than 128 characters or contain the following characters:  ?\*\/:<>|'"</span></span>

## <a name="response"></a><span data-ttu-id="5985c-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5985c-133">Response</span></span>

<span data-ttu-id="5985c-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el nuevo objeto [notebook](../resources/notebook.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5985c-134">If successful, this method returns a `201 Created` response code and the new [notebook](../resources/notebook.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5985c-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5985c-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5985c-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5985c-136">Request</span></span>
<span data-ttu-id="5985c-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5985c-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_notebook_from_onenote"
}-->
```http
POST https://graph.microsoft.com/beta/me/onenote/notebooks
Content-type: application/json
Content-length: 30

{
  "displayName": "Notebook name"
}
```

##### <a name="response"></a><span data-ttu-id="5985c-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5985c-138">Response</span></span>
<span data-ttu-id="5985c-p105">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5985c-p105">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "id": "8fcb5dbc-d5aa-4681-8e31-b001d5168d79",
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