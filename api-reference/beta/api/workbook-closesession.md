---
title: Cerrar sesión
description: 'Use esta API para cerrar una sesión existente del libro. '
ms.openlocfilehash: b591ea94552e05e108bf0582a6026087d7c115f8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089947"
---
# <a name="close-session"></a><span data-ttu-id="1b7a1-103">Cerrar sesión</span><span class="sxs-lookup"><span data-stu-id="1b7a1-103">Close Session</span></span>

<span data-ttu-id="1b7a1-104">Use esta API para cerrar una sesión existente del libro.</span><span class="sxs-lookup"><span data-stu-id="1b7a1-104">Use this API to close an existing workbook session.</span></span> 

## <a name="permissions"></a><span data-ttu-id="1b7a1-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="1b7a1-105">Permissions</span></span>
<span data-ttu-id="1b7a1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1b7a1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1b7a1-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1b7a1-108">Permission type</span></span>      | <span data-ttu-id="1b7a1-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1b7a1-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1b7a1-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1b7a1-110">Delegated (work or school account)</span></span> | <span data-ttu-id="1b7a1-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1b7a1-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="1b7a1-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1b7a1-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1b7a1-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1b7a1-113">Not supported.</span></span>    |
|<span data-ttu-id="1b7a1-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1b7a1-114">Application</span></span> | <span data-ttu-id="1b7a1-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1b7a1-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="1b7a1-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1b7a1-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/closeSession
workbook-session-id: {session-id}
```
## <a name="request-headers"></a><span data-ttu-id="1b7a1-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1b7a1-117">Request headers</span></span>
| <span data-ttu-id="1b7a1-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="1b7a1-118">Name</span></span>       | <span data-ttu-id="1b7a1-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b7a1-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="1b7a1-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="1b7a1-120">Authorization</span></span>  | <span data-ttu-id="1b7a1-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1b7a1-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1b7a1-123">workbook-session-id</span><span class="sxs-lookup"><span data-stu-id="1b7a1-123">workbook-session-id</span></span> | <span data-ttu-id="1b7a1-124">Workbook session Id que se va a cerrar</span><span class="sxs-lookup"><span data-stu-id="1b7a1-124">Workbook session Id to be closed</span></span> |

## <a name="request-body"></a><span data-ttu-id="1b7a1-125">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="1b7a1-125">Request body</span></span>
<span data-ttu-id="1b7a1-126">Esta API no requiere ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1b7a1-126">This API does not require any request body.</span></span>

## <a name="response"></a><span data-ttu-id="1b7a1-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b7a1-127">Response</span></span>

<span data-ttu-id="1b7a1-128">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="1b7a1-128">If successful, this method returns `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="1b7a1-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1b7a1-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1b7a1-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1b7a1-130">Request</span></span>
<span data-ttu-id="1b7a1-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1b7a1-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "close_excel_session"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/closeSession
Content-type: application/json
workbook-session-id: {session-id}
Content-length: 0

{

}
```

<span data-ttu-id="1b7a1-132">Tenga en cuenta que se necesita dicho encabezado workbook-session-id.</span><span class="sxs-lookup"><span data-stu-id="1b7a1-132">Note that workbook-session-id header is required.</span></span> 


##### <a name="response"></a><span data-ttu-id="1b7a1-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b7a1-133">Response</span></span>
<span data-ttu-id="1b7a1-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1b7a1-134">Here is an example of the response.</span></span> 

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```