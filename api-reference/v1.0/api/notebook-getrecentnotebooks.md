---
title: 'notebook: getRecentNotebooks'
description: Obtener una lista de instancias de recentNotebook a las que ha accedido el usuario que inició sesión.
author: jewan-microsoft
localization_priority: Normal
ms.prod: onenote
ms.openlocfilehash: 31f95d8e94ef22c6b0cbea1cbb5ff8b98c58d187
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27931674"
---
# <a name="notebook-getrecentnotebooks"></a><span data-ttu-id="4789b-103">notebook: getRecentNotebooks</span><span class="sxs-lookup"><span data-stu-id="4789b-103">notebook: getRecentNotebooks</span></span>

<span data-ttu-id="4789b-104">Obtener una lista de instancias de [recentNotebook](../resources/recentnotebook.md) a las que ha accedido el usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="4789b-104">Get a list of [recentNotebook](../resources/recentnotebook.md) instances that have been accessed by the signed-in user.</span></span>

## <a name="permissions"></a><span data-ttu-id="4789b-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="4789b-105">Permissions</span></span>
<span data-ttu-id="4789b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4789b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4789b-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4789b-108">Permission type</span></span>      | <span data-ttu-id="4789b-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4789b-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4789b-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4789b-110">Delegated (work or school account)</span></span> | <span data-ttu-id="4789b-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4789b-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All,</span></span>|
|<span data-ttu-id="4789b-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4789b-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4789b-113">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4789b-113">Notes.Create, Notes.Read, Notes.ReadWrite</span></span> |
|<span data-ttu-id="4789b-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4789b-114">Application</span></span> | <span data-ttu-id="4789b-115">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4789b-115">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4789b-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4789b-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/notebooks/getRecentNotebooks(includePersonalNotebooks=includePersonalNotebooks-value)
GET /users/{id | userPrincipalName}/onenote/notebooks/getRecentNotebooks(includePersonalNotebooks=includePersonalNotebooks-value)
```

<span data-ttu-id="4789b-117">El `<id | userPrincipalName>` del usuario debe coincidir con el usuario codificado en el token de autorización que se usa para realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4789b-117">The `<id | userPrincipalName>` for the user must match the user encoded in the authorization token used to make the request.</span></span>

## <a name="function-parameters"></a><span data-ttu-id="4789b-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="4789b-118">Function parameters</span></span>

| <span data-ttu-id="4789b-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4789b-119">Parameter</span></span>    | <span data-ttu-id="4789b-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="4789b-120">Type</span></span>   |<span data-ttu-id="4789b-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="4789b-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4789b-122">includePersonalNotebooks</span><span class="sxs-lookup"><span data-stu-id="4789b-122">includePersonalNotebooks</span></span>|<span data-ttu-id="4789b-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="4789b-123">Boolean</span></span>|<span data-ttu-id="4789b-124">Incluir los blocs de notas que pertenecen al usuario.</span><span class="sxs-lookup"><span data-stu-id="4789b-124">Include notebooks owned by the user.</span></span> <span data-ttu-id="4789b-125">Se establece en `true` para incluir los blocs de notas que pertenecen al usuario; en caso contrario, se establece en `false`.</span><span class="sxs-lookup"><span data-stu-id="4789b-125">Set to `true` to include notebooks owned by the user; otherwise, set to `false`.</span></span> <span data-ttu-id="4789b-126">Si no incluye el parámetro `includePersonalNotebooks`, la solicitud devolverá una respuesta de error `400`.</span><span class="sxs-lookup"><span data-stu-id="4789b-126">If you don't include the `includePersonalNotebooks` parameter, your request will return a `400` error response.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="4789b-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4789b-127">Request headers</span></span>
| <span data-ttu-id="4789b-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="4789b-128">Name</span></span>       | <span data-ttu-id="4789b-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="4789b-129">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="4789b-130">Autorización</span><span class="sxs-lookup"><span data-stu-id="4789b-130">Authorization</span></span>  | <span data-ttu-id="4789b-131">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="4789b-131">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="4789b-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4789b-132">Request body</span></span>
<span data-ttu-id="4789b-133">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4789b-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4789b-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4789b-134">Response</span></span>
<span data-ttu-id="4789b-135">Una respuesta correcta devuelve un valor `200 OK` que contiene una colección JSON de **recentNotebooks**.</span><span class="sxs-lookup"><span data-stu-id="4789b-135">A successful response returns a `200 OK` that contains a JSON collection of **recentNotebooks**.</span></span>

## <a name="example"></a><span data-ttu-id="4789b-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4789b-136">Example</span></span>
<span data-ttu-id="4789b-137">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="4789b-137">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="4789b-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4789b-138">Request</span></span>
<span data-ttu-id="4789b-139">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4789b-139">The following example shows the request.</span></span>
<!-- { "blockType": "request", "name": "recent_notebooks", "scopes": "notes.read" } -->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/notebooks/getRecentNotebooks(includePersonalNotebooks=true)
```

#### <a name="response"></a><span data-ttu-id="4789b-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4789b-140">Response</span></span>
<span data-ttu-id="4789b-141">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4789b-141">The following example shows the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.recentNotebook)",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-Length: 1110

{
  "value":[
    {
      "displayName":"Personal Notebook","lastAccessedTime":"timestamp","links":{
        "oneNoteClientUrl":{
          "href":"onenote:href-value"
        },"oneNoteWebUrl":{
          "href":"href-value"
        }
      },"sourceService":"OneDrive"
    },{
      "displayName":"Team Shared Notebook","lastAccessedTime":"timestamp","links":{
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
