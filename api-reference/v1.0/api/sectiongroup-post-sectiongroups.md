---
title: Crear sectionGroup
description: Crea un grupo de sección en el grupo de sección especificado.
localization_priority: Normal
author: jewan-microsoft
ms.prod: onenote
ms.openlocfilehash: a05e61934c8043c0c6a94c6e0785c0e93e4a3e19
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987114"
---
# <a name="create-sectiongroup"></a><span data-ttu-id="01b88-103">Crear sectionGroup</span><span class="sxs-lookup"><span data-stu-id="01b88-103">Create sectionGroup</span></span>

<span data-ttu-id="01b88-104">Crea un [grupo de sección](../resources/sectiongroup.md) en el grupo de sección especificado.</span><span class="sxs-lookup"><span data-stu-id="01b88-104">Create a new [section group](../resources/sectiongroup.md) in the specified section group.</span></span>
## <a name="permissions"></a><span data-ttu-id="01b88-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="01b88-105">Permissions</span></span>
<span data-ttu-id="01b88-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="01b88-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="01b88-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="01b88-108">Permission type</span></span>      | <span data-ttu-id="01b88-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="01b88-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="01b88-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="01b88-110">Delegated (work or school account)</span></span> | <span data-ttu-id="01b88-111">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="01b88-111">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="01b88-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="01b88-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="01b88-113">Notes.Create, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="01b88-113">Notes.Create, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="01b88-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="01b88-114">Application</span></span> | <span data-ttu-id="01b88-115">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="01b88-115">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="01b88-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="01b88-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/sectionGroups/{id}/sectionGroups
POST /users/{id | userPrincipalName}/onenote/sectionGroups/{id}/sectionGroups
POST /groups/{id}/onenote/sectionGroups/{id}/sectionGroups
POST /sites/{id}/onenote/sectionGroups/{id}/sectionGroups
```
## <a name="request-headers"></a><span data-ttu-id="01b88-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="01b88-117">Request headers</span></span>
| <span data-ttu-id="01b88-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="01b88-118">Name</span></span>       | <span data-ttu-id="01b88-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="01b88-119">Type</span></span> | <span data-ttu-id="01b88-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="01b88-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="01b88-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="01b88-121">Authorization</span></span>  | <span data-ttu-id="01b88-122">string</span><span class="sxs-lookup"><span data-stu-id="01b88-122">string</span></span>  | <span data-ttu-id="01b88-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="01b88-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="01b88-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="01b88-125">Content-Type</span></span> | <span data-ttu-id="01b88-126">string</span><span class="sxs-lookup"><span data-stu-id="01b88-126">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="01b88-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="01b88-127">Request body</span></span>
<span data-ttu-id="01b88-128">En el cuerpo de la solicitud, asigne un nombre al grupo de sección.</span><span class="sxs-lookup"><span data-stu-id="01b88-128">In the request body, supply a name for the section group.</span></span>

<span data-ttu-id="01b88-p103">En el mismo nivel de jerarquía, los nombres de grupo de sección deben ser únicos. El nombre no puede contener más de 50 caracteres ni los caracteres siguientes: ?\*\/:<>|&#''%~</span><span class="sxs-lookup"><span data-stu-id="01b88-p103">Within the same hierarchy level, section group names must be unique. The name cannot contain more than 50 characters or contain the following characters:  ?\*\/:<>|&#''%~</span></span>

## <a name="response"></a><span data-ttu-id="01b88-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01b88-131">Response</span></span>

<span data-ttu-id="01b88-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [sectionGroup](../resources/sectiongroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01b88-132">If successful, this method returns a `201 Created` response code and a [sectionGroup](../resources/sectiongroup.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="01b88-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="01b88-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="01b88-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="01b88-134">Request</span></span>
<span data-ttu-id="01b88-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="01b88-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_sectiongroup_from_sectiongroup"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/sectionGroups/{id}/sectionGroups
Content-type: application/json
Content-length: 30

{
  "displayName": "Section group name"
}
```
##### <a name="response"></a><span data-ttu-id="01b88-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01b88-136">Response</span></span>
<span data-ttu-id="01b88-p104">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="01b88-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
