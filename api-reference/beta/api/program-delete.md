---
title: Eliminar programa
description: En AD Azure access revisiones característica, eliminar un objeto de programa.
ms.openlocfilehash: c09dcc36bfc4fbf279e7b6c49ea24bba9153c071
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088688"
---
# <a name="delete-program"></a><span data-ttu-id="53fc9-103">Eliminar programa</span><span class="sxs-lookup"><span data-stu-id="53fc9-103">Delete program</span></span>

> <span data-ttu-id="53fc9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="53fc9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="53fc9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="53fc9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="53fc9-106">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, eliminar un objeto de [programa](../resources/program.md) .</span><span class="sxs-lookup"><span data-stu-id="53fc9-106">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, delete a [program](../resources/program.md) object.</span></span>

<span data-ttu-id="53fc9-107">No elimine un programa que todavía tiene `programControl` vinculados a ella, las revisiones de access deben primero eliminarse o desvincula desde el programa y vinculadas a otro programa.</span><span class="sxs-lookup"><span data-stu-id="53fc9-107">Do not delete a program which still has `programControl` linked to it, those access reviews should first be deleted or unlinked from the program and linked to a different program.</span></span>  <span data-ttu-id="53fc9-108">Además, tenga en cuenta que no se puede eliminar el programa predeterminado integrado.</span><span class="sxs-lookup"><span data-stu-id="53fc9-108">Also, please note that the built-in default program cannot be deleted.</span></span>


## <a name="permissions"></a><span data-ttu-id="53fc9-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="53fc9-109">Permissions</span></span>
<span data-ttu-id="53fc9-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="53fc9-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="53fc9-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="53fc9-112">Permission type</span></span>                        | <span data-ttu-id="53fc9-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="53fc9-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="53fc9-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="53fc9-114">Delegated (work or school account)</span></span>     | <span data-ttu-id="53fc9-115">`ProgramControl.ReadWrite.All`.</span><span class="sxs-lookup"><span data-stu-id="53fc9-115"></span></span>  <span data-ttu-id="53fc9-116">También debe ser el usuario iniciado en un rol de Active directory que le permita crear un programa.</span><span class="sxs-lookup"><span data-stu-id="53fc9-116">The signed in user must also be in a directory role which permits them to create a program.</span></span> |
|<span data-ttu-id="53fc9-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="53fc9-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="53fc9-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="53fc9-118">Not supported.</span></span> |
|<span data-ttu-id="53fc9-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="53fc9-119">Application</span></span>                            | <span data-ttu-id="53fc9-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="53fc9-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="53fc9-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="53fc9-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /programs('<id>')
```
## <a name="request-headers"></a><span data-ttu-id="53fc9-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="53fc9-122">Request headers</span></span>
| <span data-ttu-id="53fc9-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="53fc9-123">Name</span></span>         | <span data-ttu-id="53fc9-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="53fc9-124">Type</span></span>        | <span data-ttu-id="53fc9-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="53fc9-125">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="53fc9-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="53fc9-126">Authorization</span></span> | <span data-ttu-id="53fc9-127">string</span><span class="sxs-lookup"><span data-stu-id="53fc9-127">string</span></span> | <span data-ttu-id="53fc9-128">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="53fc9-128">Bearer \{token\}.</span></span> <span data-ttu-id="53fc9-129">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="53fc9-129">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="53fc9-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="53fc9-130">Request body</span></span>
<span data-ttu-id="53fc9-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="53fc9-131">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="53fc9-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53fc9-132">Response</span></span>
<span data-ttu-id="53fc9-p106">Si se ejecuta correctamente, este método devuelve un código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="53fc9-p106">If successful, this method returns a `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="53fc9-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="53fc9-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="53fc9-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="53fc9-136">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_program"
}-->
```http
DELETE https://graph.microsoft.com/beta/programs('7e59d237-2fb0-4e5d-b7bb-d4f9f9129213')
```
##### <a name="response"></a><span data-ttu-id="53fc9-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53fc9-137">Response</span></span>
><span data-ttu-id="53fc9-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="53fc9-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-25 00:00:01 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete program",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
