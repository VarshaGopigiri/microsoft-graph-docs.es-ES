---
title: Cerrar sesión
description: 'Use esta API para cerrar una sesión existente del libro. '
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 0e4d00b1ebf9ba90f6085f8dc7fc1005375efc0d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27818637"
---
# <a name="close-session"></a><span data-ttu-id="d04d5-103">Cerrar sesión</span><span class="sxs-lookup"><span data-stu-id="d04d5-103">Close Session</span></span>

<span data-ttu-id="d04d5-104">Use esta API para cerrar una sesión existente del libro.</span><span class="sxs-lookup"><span data-stu-id="d04d5-104">Use this API to close an existing workbook session.</span></span> 

## <a name="permissions"></a><span data-ttu-id="d04d5-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="d04d5-105">Permissions</span></span>
<span data-ttu-id="d04d5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d04d5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d04d5-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d04d5-108">Permission type</span></span>      | <span data-ttu-id="d04d5-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d04d5-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d04d5-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d04d5-110">Delegated (work or school account)</span></span> | <span data-ttu-id="d04d5-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d04d5-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="d04d5-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d04d5-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d04d5-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d04d5-113">Not supported.</span></span>    |
|<span data-ttu-id="d04d5-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d04d5-114">Application</span></span> | <span data-ttu-id="d04d5-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d04d5-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d04d5-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d04d5-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/closeSession
workbook-session-id: {session-id}
```
## <a name="request-headers"></a><span data-ttu-id="d04d5-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d04d5-117">Request headers</span></span>
| <span data-ttu-id="d04d5-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="d04d5-118">Name</span></span>       | <span data-ttu-id="d04d5-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="d04d5-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="d04d5-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="d04d5-120">Authorization</span></span>  | <span data-ttu-id="d04d5-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d04d5-p102">Bearer {token}. Required.</span></span> | | <span data-ttu-id="d04d5-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="d04d5-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="d04d5-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="d04d5-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|
| <span data-ttu-id="d04d5-126">workbook-session-id</span><span class="sxs-lookup"><span data-stu-id="d04d5-126">workbook-session-id</span></span> | <span data-ttu-id="d04d5-127">Workbook session Id que se va a cerrar</span><span class="sxs-lookup"><span data-stu-id="d04d5-127">Workbook session Id to be closed</span></span> |

## <a name="request-body"></a><span data-ttu-id="d04d5-128">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="d04d5-128">Request body</span></span>
<span data-ttu-id="d04d5-129">Esta API no requiere ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d04d5-129">This API does not require any request body.</span></span>

## <a name="response"></a><span data-ttu-id="d04d5-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d04d5-130">Response</span></span>

<span data-ttu-id="d04d5-131">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="d04d5-131">If successful, this method returns `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="d04d5-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d04d5-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d04d5-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d04d5-133">Request</span></span>
<span data-ttu-id="d04d5-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d04d5-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "close_excel_session"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/closeSession
Content-type: application/json
workbook-session-id: {session-id}
Content-length: 0

{

}
```

<span data-ttu-id="d04d5-135">Tenga en cuenta que se necesita dicho encabezado workbook-session-id.</span><span class="sxs-lookup"><span data-stu-id="d04d5-135">Note that workbook-session-id header is required.</span></span> 


##### <a name="response"></a><span data-ttu-id="d04d5-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d04d5-136">Response</span></span>
<span data-ttu-id="d04d5-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d04d5-137">Here is an example of the response.</span></span> 

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- {
  "type": "#page.annotation",
  "suppressions": [
    "Warning: close_excel_session//api-reference/v1.0/api/workbook-closesession.md:
      Request includes a non-standard header: workbook-session-id"
  ]
}-->
