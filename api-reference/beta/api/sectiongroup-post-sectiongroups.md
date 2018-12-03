---
title: Crear sectionGroup
description: Crea un grupo de sección en el grupo de sección especificado.
ms.openlocfilehash: 62e88f65755006fb6cbb4755cd63ef02fbc19556
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086317"
---
# <a name="create-sectiongroup"></a><span data-ttu-id="7967b-103">Crear sectionGroup</span><span class="sxs-lookup"><span data-stu-id="7967b-103">Create sectionGroup</span></span>

> <span data-ttu-id="7967b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7967b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7967b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7967b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7967b-106">Crea un [grupo de sección](../resources/sectiongroup.md) en el grupo de sección especificado.</span><span class="sxs-lookup"><span data-stu-id="7967b-106">Create a new [section group](../resources/sectiongroup.md) in the specified section group.</span></span>
## <a name="permissions"></a><span data-ttu-id="7967b-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="7967b-107">Permissions</span></span>
<span data-ttu-id="7967b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7967b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7967b-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7967b-110">Permission type</span></span>      | <span data-ttu-id="7967b-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7967b-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7967b-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7967b-112">Delegated (work or school account)</span></span> | <span data-ttu-id="7967b-113">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7967b-113">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="7967b-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7967b-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7967b-115">Notes.Create, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7967b-115">Notes.Create, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="7967b-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7967b-116">Application</span></span> | <span data-ttu-id="7967b-117">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7967b-117">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="7967b-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7967b-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/sectionGroups/{id}/sectionGroups
POST /users/{id | userPrincipalName}/onenote/sectionGroups/{id}/sectionGroups
POST /groups/{id}/onenote/sectionGroups/{id}/sectionGroups
POST /sites/{id}/onenote/sectionGroups/{id}/sectionGroups
```
## <a name="request-headers"></a><span data-ttu-id="7967b-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7967b-119">Request headers</span></span>
| <span data-ttu-id="7967b-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="7967b-120">Name</span></span>       | <span data-ttu-id="7967b-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="7967b-121">Type</span></span> | <span data-ttu-id="7967b-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="7967b-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="7967b-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="7967b-123">Authorization</span></span>  | <span data-ttu-id="7967b-124">string</span><span class="sxs-lookup"><span data-stu-id="7967b-124">string</span></span>  | <span data-ttu-id="7967b-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7967b-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="7967b-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7967b-127">Content-Type</span></span> | <span data-ttu-id="7967b-128">string</span><span class="sxs-lookup"><span data-stu-id="7967b-128">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="7967b-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7967b-129">Request body</span></span>
<span data-ttu-id="7967b-130">En el cuerpo de la solicitud, asigne un nombre al grupo de sección.</span><span class="sxs-lookup"><span data-stu-id="7967b-130">In the request body, supply a name for the section group.</span></span>

<span data-ttu-id="7967b-p104">En el mismo nivel de jerarquía, los nombres de grupo de sección deben ser únicos. El nombre no puede contener más de 50 caracteres ni los caracteres siguientes: ?\*\/:<>|&#''%~</span><span class="sxs-lookup"><span data-stu-id="7967b-p104">Within the same hierarchy level, section group names must be unique. The name cannot contain more than 50 characters or contain the following characters:  ?\*\/:<>|&#''%~</span></span>

## <a name="response"></a><span data-ttu-id="7967b-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7967b-133">Response</span></span>

<span data-ttu-id="7967b-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [sectionGroup](../resources/sectiongroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7967b-134">If successful, this method returns a `201 Created` response code and a [sectionGroup](../resources/sectiongroup.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7967b-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7967b-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7967b-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7967b-136">Request</span></span>
<span data-ttu-id="7967b-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7967b-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_sectiongroup_from_sectiongroup"
}-->
```http
POST https://graph.microsoft.com/beta/me/onenote/sectionGroups/{id}/sectionGroups
Content-type: application/json
Content-length: 30

{
  "displayName": "Section group name"
}
```
##### <a name="response"></a><span data-ttu-id="7967b-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7967b-138">Response</span></span>
<span data-ttu-id="7967b-p105">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7967b-p105">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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