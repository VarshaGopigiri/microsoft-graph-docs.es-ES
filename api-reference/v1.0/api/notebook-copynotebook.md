---
title: 'bloc de notas: copyNotebook'
description: Copia un bloc de notas a la carpeta Blocs de notas de la biblioteca de documentos de destino. Se crea la carpeta si no existe.
localization_priority: Normal
author: jewan-microsoft
ms.prod: onenote
ms.openlocfilehash: aa684dcaa01f2a8c16be1c75a7b973ee8adb8eea
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972932"
---
# <a name="notebook-copynotebook"></a><span data-ttu-id="f9172-104">bloc de notas: copyNotebook</span><span class="sxs-lookup"><span data-stu-id="f9172-104">notebook: copyNotebook</span></span>
<span data-ttu-id="f9172-p102">Copia un bloc de notas a la carpeta Blocs de notas de la biblioteca de documentos de destino. Se crea la carpeta si no existe.</span><span class="sxs-lookup"><span data-stu-id="f9172-p102">Copies a notebook to the Notebooks folder in the destination Documents library. The folder is created if it doesn't exist.</span></span>

<span data-ttu-id="f9172-107">En el caso de las operaciones de copia, siga un patrón de llamada asincrónico:  Llame primero a la acción de copiar y, a continuación, sondee el extremo de la operación para obtener el resultado.</span><span class="sxs-lookup"><span data-stu-id="f9172-107">For Copy operations, you follow an asynchronous calling pattern:  First call the Copy action, and then poll the operation endpoint for the result.</span></span>

## <a name="permissions"></a><span data-ttu-id="f9172-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="f9172-108">Permissions</span></span>
<span data-ttu-id="f9172-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f9172-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f9172-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f9172-111">Permission type</span></span>      | <span data-ttu-id="f9172-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f9172-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f9172-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f9172-113">Delegated (work or school account)</span></span> | <span data-ttu-id="f9172-114">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f9172-114">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="f9172-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f9172-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f9172-116">Notes.Create, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f9172-116">Notes.Create, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="f9172-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f9172-117">Application</span></span> | <span data-ttu-id="f9172-118">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f9172-118">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f9172-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f9172-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/notebooks/{id}/copyNotebook
POST /users/{id | userPrincipalName}/onenote/notebooks/{id}/copyNotebook
POST /groups/{id}/onenote/notebooks/{id}/copyNotebook
```
## <a name="request-headers"></a><span data-ttu-id="f9172-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f9172-120">Request headers</span></span>
| <span data-ttu-id="f9172-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="f9172-121">Name</span></span>       | <span data-ttu-id="f9172-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="f9172-122">Type</span></span> | <span data-ttu-id="f9172-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9172-123">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="f9172-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="f9172-124">Authorization</span></span>  | <span data-ttu-id="f9172-125">string</span><span class="sxs-lookup"><span data-stu-id="f9172-125">string</span></span>  | <span data-ttu-id="f9172-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f9172-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f9172-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f9172-128">Content-Type</span></span> | <span data-ttu-id="f9172-129">string</span><span class="sxs-lookup"><span data-stu-id="f9172-129">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="f9172-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f9172-130">Request body</span></span>
<span data-ttu-id="f9172-p105">En el cuerpo de la solicitud, proporcione un objeto JSON que contenga los parámetros que necesita la operación. Puede enviarse un cuerpo vacío si no se necesita ninguno.</span><span class="sxs-lookup"><span data-stu-id="f9172-p105">In the request body, provide a JSON object that contains the parameters that your operation needs. It's okay to send an empty body if none are needed.</span></span>

| <span data-ttu-id="f9172-133">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f9172-133">Parameter</span></span>    | <span data-ttu-id="f9172-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="f9172-134">Type</span></span>   |<span data-ttu-id="f9172-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9172-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f9172-136">groupId</span><span class="sxs-lookup"><span data-stu-id="f9172-136">groupId</span></span>|<span data-ttu-id="f9172-137">String</span><span class="sxs-lookup"><span data-stu-id="f9172-137">String</span></span>|<span data-ttu-id="f9172-p106">El id. del grupo al que se debe copiar. Debe usarse solo cuando copie a un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="f9172-p106">The id of the group to copy to. Use only when copying to an Office 365 group.</span></span>|
|<span data-ttu-id="f9172-140">renameAs</span><span class="sxs-lookup"><span data-stu-id="f9172-140">renameAs</span></span>|<span data-ttu-id="f9172-141">String</span><span class="sxs-lookup"><span data-stu-id="f9172-141">String</span></span>|<span data-ttu-id="f9172-p107">El nombre de la copia. Tiene como valor predeterminado el nombre del elemento existente.</span><span class="sxs-lookup"><span data-stu-id="f9172-p107">The name of the copy. Defaults to the name of the existing item.</span></span> |

## <a name="response"></a><span data-ttu-id="f9172-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9172-144">Response</span></span>

<span data-ttu-id="f9172-p108">Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted` y un encabezado `Operation-Location`. Sondee el extremo de Operation-Location para [obtener el estado de la operación de copia](onenoteoperation-get.md).</span><span class="sxs-lookup"><span data-stu-id="f9172-p108">If successful, this method returns a `202 Accepted` response code and an `Operation-Location` header. Poll the Operation-Location endpoint to [get the status of the copy operation](onenoteoperation-get.md).</span></span>

## <a name="example"></a><span data-ttu-id="f9172-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9172-147">Example</span></span>
<span data-ttu-id="f9172-148">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="f9172-148">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="f9172-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f9172-149">Request</span></span>
<span data-ttu-id="f9172-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f9172-150">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "notebook_copynotebook"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/notebooks/{id}/copyNotebook
Content-type: application/json
Content-length: 108

{
  "groupId": "groupId-value",
  "renameAs": "renameAs-value"
}
```

##### <a name="response"></a><span data-ttu-id="f9172-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9172-151">Response</span></span>
<span data-ttu-id="f9172-152">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9172-152">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.onenoteOperation"
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "notebook: copyNotebook",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
