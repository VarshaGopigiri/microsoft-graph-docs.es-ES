---
title: 'notebook: getRecentNotebooks'
description: Obtener una lista de instancias de recentNotebook a las que ha accedido el usuario que inició sesión.
author: Jewan-microsoft
localization_priority: Normal
ms.openlocfilehash: 0487a7810602f709ea6386957fa1047a60111990
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887328"
---
# <a name="notebook-getrecentnotebooks"></a><span data-ttu-id="e4235-103">notebook: getRecentNotebooks</span><span class="sxs-lookup"><span data-stu-id="e4235-103">notebook: getRecentNotebooks</span></span>

> <span data-ttu-id="e4235-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e4235-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e4235-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e4235-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e4235-106">Obtener una lista de instancias de [recentNotebook](../resources/recentnotebook.md) a las que ha accedido el usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="e4235-106">Get a list of [recentNotebook](../resources/recentnotebook.md) instances that have been accessed by the signed-in user.</span></span>

## <a name="permissions"></a><span data-ttu-id="e4235-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e4235-107">Permissions</span></span>
<span data-ttu-id="e4235-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e4235-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e4235-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e4235-110">Permission type</span></span>      | <span data-ttu-id="e4235-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e4235-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e4235-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e4235-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e4235-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e4235-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All,</span></span>|
|<span data-ttu-id="e4235-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e4235-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e4235-115">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e4235-115">Notes.Create, Notes.Read, Notes.ReadWrite</span></span> |
|<span data-ttu-id="e4235-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e4235-116">Application</span></span> | <span data-ttu-id="e4235-117">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e4235-117">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e4235-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e4235-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/notebooks/getRecentNotebooks(includePersonalNotebooks=includePersonalNotebooks-value)
GET /users/<id | userPrincipalName>/onenote/notebooks/getRecentNotebooks(includePersonalNotebooks=includePersonalNotebooks-value)
```

<span data-ttu-id="e4235-119">El `<id | userPrincipalName>` del usuario debe coincidir con el usuario codificado en el token de autorización que se usa para realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e4235-119">The `<id | userPrincipalName>` for the user must match the user encoded in the authorization token used to make the request.</span></span>

## <a name="function-parameters"></a><span data-ttu-id="e4235-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="e4235-120">Function parameters</span></span>

| <span data-ttu-id="e4235-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e4235-121">Parameter</span></span>    | <span data-ttu-id="e4235-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4235-122">Type</span></span>   |<span data-ttu-id="e4235-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4235-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e4235-124">includePersonalNotebooks</span><span class="sxs-lookup"><span data-stu-id="e4235-124">includePersonalNotebooks</span></span>|<span data-ttu-id="e4235-125">Boolean</span><span class="sxs-lookup"><span data-stu-id="e4235-125">Boolean</span></span>|<span data-ttu-id="e4235-126">Incluir los blocs de notas que pertenecen al usuario.</span><span class="sxs-lookup"><span data-stu-id="e4235-126">Include notebooks owned by the user.</span></span> <span data-ttu-id="e4235-127">Se establece en `true` para incluir los blocs de notas que pertenecen al usuario; en caso contrario, se establece en `false`.</span><span class="sxs-lookup"><span data-stu-id="e4235-127">Set to `true` to include notebooks owned by the user; otherwise, set to `false`.</span></span> <span data-ttu-id="e4235-128">Si no incluye el parámetro `includePersonalNotebooks`, la solicitud devolverá una respuesta de error `400`.</span><span class="sxs-lookup"><span data-stu-id="e4235-128">If you don't include the `includePersonalNotebooks` parameter, your request will return a `400` error response.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="e4235-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e4235-129">Request headers</span></span>
| <span data-ttu-id="e4235-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="e4235-130">Name</span></span>       | <span data-ttu-id="e4235-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4235-131">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="e4235-132">Autorización</span><span class="sxs-lookup"><span data-stu-id="e4235-132">Authorization</span></span>  | <span data-ttu-id="e4235-133">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="e4235-133">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="e4235-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e4235-134">Request body</span></span>
<span data-ttu-id="e4235-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e4235-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e4235-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4235-136">Response</span></span>
<span data-ttu-id="e4235-137">Una respuesta correcta devuelve un valor `200 OK` que contiene una colección JSON de **recentNotebooks**.</span><span class="sxs-lookup"><span data-stu-id="e4235-137">A successful response returns a `200 OK` that contains a JSON collection of **recentNotebooks**.</span></span>

## <a name="example"></a><span data-ttu-id="e4235-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e4235-138">Example</span></span>
<span data-ttu-id="e4235-139">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="e4235-139">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="e4235-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e4235-140">Request</span></span>
<span data-ttu-id="e4235-141">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e4235-141">The following example shows the request.</span></span>
<!-- { "blockType": "request", "name": "recent_notebooks", "scopes": "notes.read" } -->
```http
GET https://graph.microsoft.com/v1.0/onenote/notebooks/getrecentnotebooks(includePersonalNotebooks=true)
```

##### <a name="response"></a><span data-ttu-id="e4235-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4235-142">Response</span></span>
<span data-ttu-id="e4235-143">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e4235-143">The following example shows the response.</span></span>

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
