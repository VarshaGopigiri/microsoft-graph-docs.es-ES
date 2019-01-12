---
title: 'llamar a: changeScreenSharingRole'
description: Iniciar y detener el uso compartido de pantalla en la llamada. Esta API se usa para permitir que las aplicaciones compartir el contenido de la pantalla con los participantes de una llamada o una reunión.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: c7463f54ab5bfc74a55ed7dc5360a4f16876116c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976229"
---
# <a name="call-changescreensharingrole"></a><span data-ttu-id="b3818-104">llamar a: changeScreenSharingRole</span><span class="sxs-lookup"><span data-stu-id="b3818-104">call: changeScreenSharingRole</span></span>

> <span data-ttu-id="b3818-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b3818-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b3818-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b3818-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b3818-107">Iniciar y detener el uso compartido de pantalla en la llamada.</span><span class="sxs-lookup"><span data-stu-id="b3818-107">Start and stop sharing screen in the call.</span></span> <span data-ttu-id="b3818-108">Esta API se usa para permitir que las aplicaciones compartir el contenido de la pantalla con los participantes de una llamada o una reunión.</span><span class="sxs-lookup"><span data-stu-id="b3818-108">This API is used to allow applications to share screen content with the participants of a call or meeting.</span></span>

## <a name="permissions"></a><span data-ttu-id="b3818-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="b3818-109">Permissions</span></span>
<span data-ttu-id="b3818-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b3818-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="b3818-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b3818-112">Permission type</span></span>                        | <span data-ttu-id="b3818-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b3818-113">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="b3818-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b3818-114">Delegated (work or school account)</span></span>     | <span data-ttu-id="b3818-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="b3818-115">Not Supported</span></span>                               |
| <span data-ttu-id="b3818-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b3818-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b3818-117">No se admite</span><span class="sxs-lookup"><span data-stu-id="b3818-117">Not Supported</span></span>                               |
| <span data-ttu-id="b3818-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b3818-118">Application</span></span>                            | <span data-ttu-id="b3818-119">Calls.AccessMedia.All</span><span class="sxs-lookup"><span data-stu-id="b3818-119">Calls.AccessMedia.All</span></span>                       |

## <a name="http-request"></a><span data-ttu-id="b3818-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b3818-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/changeScreenSharingRole
POST /applications/{id}/calls/{id}/changeScreenSharingRole
```

## <a name="request-headers"></a><span data-ttu-id="b3818-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b3818-121">Request headers</span></span>
| <span data-ttu-id="b3818-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="b3818-122">Name</span></span>          | <span data-ttu-id="b3818-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3818-123">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="b3818-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="b3818-124">Authorization</span></span> | <span data-ttu-id="b3818-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b3818-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b3818-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b3818-127">Request body</span></span>
<span data-ttu-id="b3818-128">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="b3818-128">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="b3818-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b3818-129">Parameter</span></span>      | <span data-ttu-id="b3818-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="b3818-130">Type</span></span>    |<span data-ttu-id="b3818-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3818-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b3818-132">role</span><span class="sxs-lookup"><span data-stu-id="b3818-132">role</span></span>|<span data-ttu-id="b3818-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="b3818-133">String</span></span>|<span data-ttu-id="b3818-134">Los valores posibles son: 'Visor', 'Que comparte'</span><span class="sxs-lookup"><span data-stu-id="b3818-134">Possible values are: 'Viewer', 'Sharer'</span></span>|

## <a name="response"></a><span data-ttu-id="b3818-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b3818-135">Response</span></span>
<span data-ttu-id="b3818-136">Devuelve `202 Accepted` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="b3818-136">Returns `202 Accepted` response code.</span></span>

## <a name="example"></a><span data-ttu-id="b3818-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b3818-137">Example</span></span>
<span data-ttu-id="b3818-138">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b3818-138">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="b3818-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b3818-139">Request</span></span>
<span data-ttu-id="b3818-140">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b3818-140">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "call-changeScreenSharingRole"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/changeScreenSharingRole
Content-Type: application/json
Content-Length: 24

{
  "role": "viewer"
}
```

##### <a name="response"></a><span data-ttu-id="b3818-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b3818-141">Response</span></span>
<span data-ttu-id="b3818-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b3818-142">Here is an example of the response.</span></span> 

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "call: changeScreenSharingRole",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
