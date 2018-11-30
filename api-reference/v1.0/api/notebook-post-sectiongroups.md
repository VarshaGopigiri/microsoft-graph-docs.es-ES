---
title: Crear sectionGroup
description: Crea un grupo de sección nuevo en el bloc de notas especificado.
ms.openlocfilehash: 8209f9aa66c90b88e2ea1a63cca24542edd57baa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029030"
---
# <a name="create-sectiongroup"></a><span data-ttu-id="76917-103">Crear sectionGroup</span><span class="sxs-lookup"><span data-stu-id="76917-103">Create sectionGroup</span></span>

<span data-ttu-id="76917-104">Crea un [grupo de sección](../resources/sectiongroup.md) nuevo en el bloc de notas especificado.</span><span class="sxs-lookup"><span data-stu-id="76917-104">Create a new [section group](../resources/sectiongroup.md) in the specified notebook.</span></span>
## <a name="permissions"></a><span data-ttu-id="76917-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="76917-105">Permissions</span></span>
<span data-ttu-id="76917-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="76917-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="76917-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="76917-108">Permission type</span></span>      | <span data-ttu-id="76917-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="76917-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="76917-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="76917-110">Delegated (work or school account)</span></span> | <span data-ttu-id="76917-111">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="76917-111">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="76917-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="76917-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="76917-113">Notes.Create, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="76917-113">Notes.Create, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="76917-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="76917-114">Application</span></span> | <span data-ttu-id="76917-115">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="76917-115">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="76917-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="76917-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/notebooks/{id}/sectionGroups
POST /users/{id | userPrincipalName}/onenote/notebooks/{id}/sectionGroups
POST /groups/{id}/onenote/notebooks/{id}/sectionGroups
POST /sites/{id}/onenote/notebooks/{id}/sectionGroups
```
## <a name="request-headers"></a><span data-ttu-id="76917-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="76917-117">Request headers</span></span>
| <span data-ttu-id="76917-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="76917-118">Name</span></span>       | <span data-ttu-id="76917-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="76917-119">Type</span></span> | <span data-ttu-id="76917-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="76917-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="76917-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="76917-121">Authorization</span></span>  | <span data-ttu-id="76917-122">string</span><span class="sxs-lookup"><span data-stu-id="76917-122">string</span></span>  | <span data-ttu-id="76917-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="76917-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="76917-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="76917-125">Content-Type</span></span> | <span data-ttu-id="76917-126">string</span><span class="sxs-lookup"><span data-stu-id="76917-126">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="76917-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="76917-127">Request body</span></span>
<span data-ttu-id="76917-128">En el cuerpo de la solicitud, asigne un nombre al grupo de sección.</span><span class="sxs-lookup"><span data-stu-id="76917-128">In the request body, supply a name for the section group.</span></span>

<span data-ttu-id="76917-p103">En el mismo nivel de jerarquía, los nombres de grupo de sección deben ser únicos. El nombre no puede contener más de 50 caracteres ni los caracteres siguientes: ?\*\/:<>|&#''%~</span><span class="sxs-lookup"><span data-stu-id="76917-p103">Within the same hierarchy level, section group names must be unique. The name cannot contain more than 50 characters or contain the following characters:  ?\*\/:<>|&#''%~</span></span>

## <a name="response"></a><span data-ttu-id="76917-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="76917-131">Response</span></span>

<span data-ttu-id="76917-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [sectionGroup](../resources/sectiongroup.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="76917-132">If successful, this method returns `201 Created` response code and a [sectionGroup](../resources/sectiongroup.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="76917-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="76917-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="76917-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="76917-134">Request</span></span>
<span data-ttu-id="76917-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="76917-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_sectiongroup_from_notebook"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/notebooks/{id}/sectionGroups
Content-type: application/json
Content-length: 30

{
  "displayName": "Section group name"
}
```

##### <a name="response"></a><span data-ttu-id="76917-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="76917-136">Response</span></span>
<span data-ttu-id="76917-p104">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="76917-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.sectionGroup"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 305

{
  "sectionsUrl": "sectionsUrl-value",
  "sectionGroupsUrl": "sectionGroupsUrl-value",
  "displayName": "name-value",
  "createdBy": {
    "user": {
      "id": "id-value",
      "displayName": "displayName-value"
    }
  },
  "lastModifiedBy": {
    "user": {
      "id": "id-value",
      "displayName": "displayName-value"
    }
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create SectionGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
