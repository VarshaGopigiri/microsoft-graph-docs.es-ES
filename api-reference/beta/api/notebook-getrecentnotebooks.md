---
title: 'notebook: getRecentNotebooks'
description: Obtener una lista de instancias de recentNotebook a las que ha accedido el usuario que inició sesión.
author: Jewan-microsoft
ms.openlocfilehash: 43141d7734a3427a3325a852d8185ebbee5d752c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27350501"
---
# <a name="notebook-getrecentnotebooks"></a><span data-ttu-id="0166c-103">notebook: getRecentNotebooks</span><span class="sxs-lookup"><span data-stu-id="0166c-103">notebook: getRecentNotebooks</span></span>

> <span data-ttu-id="0166c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0166c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0166c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0166c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0166c-106">Obtener una lista de instancias de [recentNotebook](../resources/recentnotebook.md) a las que ha accedido el usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="0166c-106">Get a list of [recentNotebook](../resources/recentnotebook.md) instances that have been accessed by the signed-in user.</span></span>

## <a name="permissions"></a><span data-ttu-id="0166c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="0166c-107">Permissions</span></span>
<span data-ttu-id="0166c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0166c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0166c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0166c-110">Permission type</span></span>      | <span data-ttu-id="0166c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0166c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0166c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0166c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="0166c-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0166c-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All,</span></span>|
|<span data-ttu-id="0166c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0166c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0166c-115">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0166c-115">Notes.Create, Notes.Read, Notes.ReadWrite</span></span> |
|<span data-ttu-id="0166c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0166c-116">Application</span></span> | <span data-ttu-id="0166c-117">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0166c-117">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="0166c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0166c-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/notebooks/getRecentNotebooks(includePersonalNotebooks=includePersonalNotebooks-value)
GET /users/<id | userPrincipalName>/onenote/notebooks/getRecentNotebooks(includePersonalNotebooks=includePersonalNotebooks-value)
```

<span data-ttu-id="0166c-119">El `<id | userPrincipalName>` del usuario debe coincidir con el usuario codificado en el token de autorización que se usa para realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0166c-119">The `<id | userPrincipalName>` for the user must match the user encoded in the authorization token used to make the request.</span></span>

## <a name="function-parameters"></a><span data-ttu-id="0166c-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="0166c-120">Function parameters</span></span>

| <span data-ttu-id="0166c-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0166c-121">Parameter</span></span>    | <span data-ttu-id="0166c-122">Type</span><span class="sxs-lookup"><span data-stu-id="0166c-122">Type</span></span>   |<span data-ttu-id="0166c-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="0166c-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0166c-124">includePersonalNotebooks</span><span class="sxs-lookup"><span data-stu-id="0166c-124">includePersonalNotebooks</span></span>|<span data-ttu-id="0166c-125">Boolean</span><span class="sxs-lookup"><span data-stu-id="0166c-125">Boolean</span></span>|<span data-ttu-id="0166c-126">Incluir los blocs de notas que pertenecen al usuario.</span><span class="sxs-lookup"><span data-stu-id="0166c-126">Include notebooks owned by the user.</span></span> <span data-ttu-id="0166c-127">Se establece en `true` para incluir los blocs de notas que pertenecen al usuario; en caso contrario, se establece en `false`.</span><span class="sxs-lookup"><span data-stu-id="0166c-127">Set to `true` to include notebooks owned by the user; otherwise, set to `false`.</span></span> <span data-ttu-id="0166c-128">Si no incluye el parámetro `includePersonalNotebooks`, la solicitud devolverá una respuesta de error `400`.</span><span class="sxs-lookup"><span data-stu-id="0166c-128">If you don't include the `includePersonalNotebooks` parameter, your request will return a `400` error response.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="0166c-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0166c-129">Request headers</span></span>
| <span data-ttu-id="0166c-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="0166c-130">Name</span></span>       | <span data-ttu-id="0166c-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="0166c-131">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="0166c-132">Autorización</span><span class="sxs-lookup"><span data-stu-id="0166c-132">Authorization</span></span>  | <span data-ttu-id="0166c-133">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="0166c-133">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="0166c-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0166c-134">Request body</span></span>
<span data-ttu-id="0166c-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0166c-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0166c-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0166c-136">Response</span></span>
<span data-ttu-id="0166c-137">Una respuesta correcta devuelve un valor `200 OK` que contiene una colección JSON de **recentNotebooks**.</span><span class="sxs-lookup"><span data-stu-id="0166c-137">A successful response returns a `200 OK` that contains a JSON collection of **recentNotebooks**.</span></span>

## <a name="example"></a><span data-ttu-id="0166c-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0166c-138">Example</span></span>
<span data-ttu-id="0166c-139">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="0166c-139">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="0166c-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0166c-140">Request</span></span>
<span data-ttu-id="0166c-141">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0166c-141">The following example shows the request.</span></span>
<!-- { "blockType": "request", "name": "recent_notebooks", "scopes": "notes.read" } -->
```http
GET https://graph.microsoft.com/v1.0/onenote/notebooks/getrecentnotebooks(includePersonalNotebooks=true)
```

##### <a name="response"></a><span data-ttu-id="0166c-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0166c-142">Response</span></span>
<span data-ttu-id="0166c-143">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0166c-143">The following example shows the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.notebook",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-Length: 1110

{
  "value":[
    {
      "name":"Personal Notebook","lastAccessedTime":"timestamp","links":{
        "oneNoteClientUrl":{
          "href":"onenote:href-value"
        },"oneNoteWebUrl":{
          "href":"href-value"
        }
      },"sourceService":"OneDrive"
    },{
      "name":"Team Shared Notebook","lastAccessedTime":"timestamp","links":{
        "oneNoteClientUrl":{
          "href":"onenote:href-value"
        },"oneNoteWebUrl":{
          "href":"href-value"
        }
      },"sourceService":"OneDriveForBusiness"
    }
  ]
}
```
