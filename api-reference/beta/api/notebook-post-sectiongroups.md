---
title: Crear sectionGroup
description: Crea un grupo de sección nuevo en el bloc de notas especificado.
author: Jewan-microsoft
ms.openlocfilehash: 7bdf81023cea5738ac434add597124151740a6e0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27360252"
---
# <a name="create-sectiongroup"></a><span data-ttu-id="06564-103">Crear sectionGroup</span><span class="sxs-lookup"><span data-stu-id="06564-103">Create sectionGroup</span></span>

> <span data-ttu-id="06564-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="06564-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="06564-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="06564-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="06564-106">Crea un [grupo de sección](../resources/sectiongroup.md) nuevo en el bloc de notas especificado.</span><span class="sxs-lookup"><span data-stu-id="06564-106">Create a new [section group](../resources/sectiongroup.md) in the specified notebook.</span></span>
## <a name="permissions"></a><span data-ttu-id="06564-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="06564-107">Permissions</span></span>
<span data-ttu-id="06564-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="06564-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="06564-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="06564-110">Permission type</span></span>      | <span data-ttu-id="06564-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="06564-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="06564-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="06564-112">Delegated (work or school account)</span></span> | <span data-ttu-id="06564-113">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="06564-113">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="06564-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="06564-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="06564-115">Notes.Create, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="06564-115">Notes.Create, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="06564-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="06564-116">Application</span></span> | <span data-ttu-id="06564-117">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="06564-117">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="06564-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="06564-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/notebooks/{id}/sectionGroups
POST /users/{id | userPrincipalName}/onenote/notebooks/{id}/sectionGroups
POST /groups/{id}/onenote/notebooks/{id}/sectionGroups
POST /sites/{id}/onenote/notebooks/{id}/sectionGroups
```
## <a name="request-headers"></a><span data-ttu-id="06564-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="06564-119">Request headers</span></span>
| <span data-ttu-id="06564-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="06564-120">Name</span></span>       | <span data-ttu-id="06564-121">Type</span><span class="sxs-lookup"><span data-stu-id="06564-121">Type</span></span> | <span data-ttu-id="06564-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="06564-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="06564-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="06564-123">Authorization</span></span>  | <span data-ttu-id="06564-124">string</span><span class="sxs-lookup"><span data-stu-id="06564-124">string</span></span>  | <span data-ttu-id="06564-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="06564-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="06564-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="06564-127">Content-Type</span></span> | <span data-ttu-id="06564-128">string</span><span class="sxs-lookup"><span data-stu-id="06564-128">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="06564-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="06564-129">Request body</span></span>
<span data-ttu-id="06564-130">En el cuerpo de la solicitud, asigne un nombre al grupo de sección.</span><span class="sxs-lookup"><span data-stu-id="06564-130">In the request body, supply a name for the section group.</span></span>

<span data-ttu-id="06564-p104">En el mismo nivel de jerarquía, los nombres de grupo de sección deben ser únicos. El nombre no puede contener más de 50 caracteres ni los caracteres siguientes: ?\*\/:<>|&#''%~</span><span class="sxs-lookup"><span data-stu-id="06564-p104">Within the same hierarchy level, section group names must be unique. The name cannot contain more than 50 characters or contain the following characters:  ?\*\/:<>|&#''%~</span></span>

## <a name="response"></a><span data-ttu-id="06564-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="06564-133">Response</span></span>

<span data-ttu-id="06564-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [sectionGroup](../resources/sectiongroup.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="06564-134">If successful, this method returns `201 Created` response code and a [sectionGroup](../resources/sectiongroup.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="06564-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="06564-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="06564-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="06564-136">Request</span></span>
<span data-ttu-id="06564-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="06564-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_sectiongroup_from_notebook"
}-->
```http
POST https://graph.microsoft.com/beta/me/onenote/notebooks/{id}/sectionGroups
Content-type: application/json
Content-length: 30

{
  "displayName": "Section group name"
}
```

##### <a name="response"></a><span data-ttu-id="06564-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="06564-138">Response</span></span>
<span data-ttu-id="06564-p105">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="06564-p105">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.sectiongroup"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 305

{
  "sectionsUrl": "sectionsUrl-value",
  "sectionGroupsUrl": "sectionGroupsUrl-value",
  "displayName": "name-value",
  "id": "8fcb5dbc-d5aa-4681-8e31-b001d5168d79",
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
