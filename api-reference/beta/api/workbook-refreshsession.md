---
title: Actualizar sesión
description: 'Use esta API para actualizar una sesión existente del libro. '
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 288f0b4b41841a6393af837f1b6e5c048dfae77e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977454"
---
# <a name="refresh-session"></a><span data-ttu-id="06e8b-103">Actualizar sesión</span><span class="sxs-lookup"><span data-stu-id="06e8b-103">Refresh Session</span></span>

<span data-ttu-id="06e8b-104">Use esta API para actualizar una sesión existente del libro.</span><span class="sxs-lookup"><span data-stu-id="06e8b-104">Use this API to refresh an existing workbook session.</span></span> 

## <a name="permissions"></a><span data-ttu-id="06e8b-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="06e8b-105">Permissions</span></span>
<span data-ttu-id="06e8b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="06e8b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="06e8b-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="06e8b-108">Permission type</span></span>      | <span data-ttu-id="06e8b-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="06e8b-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="06e8b-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="06e8b-110">Delegated (work or school account)</span></span> | <span data-ttu-id="06e8b-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="06e8b-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="06e8b-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="06e8b-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="06e8b-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="06e8b-113">Not supported.</span></span>    |
|<span data-ttu-id="06e8b-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="06e8b-114">Application</span></span> | <span data-ttu-id="06e8b-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="06e8b-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="06e8b-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="06e8b-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/refreshSession
workbook-session-id: {session-id}
```
## <a name="request-headers"></a><span data-ttu-id="06e8b-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="06e8b-117">Request headers</span></span>
| <span data-ttu-id="06e8b-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="06e8b-118">Name</span></span>       | <span data-ttu-id="06e8b-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="06e8b-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="06e8b-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="06e8b-120">Authorization</span></span>  | <span data-ttu-id="06e8b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="06e8b-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="06e8b-123">workbook-session-id</span><span class="sxs-lookup"><span data-stu-id="06e8b-123">workbook-session-id</span></span> | <span data-ttu-id="06e8b-124">Id. de sesión del libro que se va a actualizar</span><span class="sxs-lookup"><span data-stu-id="06e8b-124">Workbook session Id to be refreshed</span></span> |

## <a name="request-body"></a><span data-ttu-id="06e8b-125">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="06e8b-125">Request body</span></span>
<span data-ttu-id="06e8b-126">Esta API no requiere ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="06e8b-126">This API does not require any request body.</span></span>

## <a name="response"></a><span data-ttu-id="06e8b-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="06e8b-127">Response</span></span>

<span data-ttu-id="06e8b-128">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="06e8b-128">If successful, this method returns `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="06e8b-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="06e8b-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="06e8b-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="06e8b-130">Request</span></span>
<span data-ttu-id="06e8b-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="06e8b-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "refresh_excel_session"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/refreshSession
Content-type: application/json
workbook-session-id: {session-id}
Content-length: 0

{

}
```

<span data-ttu-id="06e8b-132">Tenga en cuenta que se necesita dicho encabezado workbook-session-id.</span><span class="sxs-lookup"><span data-stu-id="06e8b-132">Note that workbook-session-id header is required.</span></span> 


##### <a name="response"></a><span data-ttu-id="06e8b-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="06e8b-133">Response</span></span>
<span data-ttu-id="06e8b-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="06e8b-134">Here is an example of the response.</span></span> 

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```
