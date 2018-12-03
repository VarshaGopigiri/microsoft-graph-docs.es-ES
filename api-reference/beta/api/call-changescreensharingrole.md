---
title: 'llamar a: changeScreenSharingRole'
description: Iniciar y detener el uso compartido de pantalla en la llamada. Esta API se usa para permitir que las aplicaciones compartir el contenido de la pantalla con los participantes de una llamada o una reunión.
ms.openlocfilehash: f0aa69b43813bd248048ad1bd965dfbc4afc012b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086549"
---
# <a name="call-changescreensharingrole"></a><span data-ttu-id="ad153-104">llamar a: changeScreenSharingRole</span><span class="sxs-lookup"><span data-stu-id="ad153-104">call: changeScreenSharingRole</span></span>

> <span data-ttu-id="ad153-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ad153-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ad153-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ad153-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ad153-107">Iniciar y detener el uso compartido de pantalla en la llamada.</span><span class="sxs-lookup"><span data-stu-id="ad153-107">Start and stop sharing screen in the call.</span></span> <span data-ttu-id="ad153-108">Esta API se usa para permitir que las aplicaciones compartir el contenido de la pantalla con los participantes de una llamada o una reunión.</span><span class="sxs-lookup"><span data-stu-id="ad153-108">This API is used to allow applications to share screen content with the participants of a call or meeting.</span></span>

## <a name="permissions"></a><span data-ttu-id="ad153-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="ad153-109">Permissions</span></span>
<span data-ttu-id="ad153-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ad153-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="ad153-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ad153-112">Permission type</span></span>                        | <span data-ttu-id="ad153-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ad153-113">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="ad153-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ad153-114">Delegated (work or school account)</span></span>     | <span data-ttu-id="ad153-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="ad153-115">Not Supported</span></span>                               |
| <span data-ttu-id="ad153-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ad153-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ad153-117">No se admite</span><span class="sxs-lookup"><span data-stu-id="ad153-117">Not Supported</span></span>                               |
| <span data-ttu-id="ad153-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ad153-118">Application</span></span>                            | <span data-ttu-id="ad153-119">Calls.AccessMedia.All</span><span class="sxs-lookup"><span data-stu-id="ad153-119">Calls.AccessMedia.All</span></span>                       |

## <a name="http-request"></a><span data-ttu-id="ad153-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ad153-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/changeScreenSharingRole
POST /applications/{id}/calls/{id}/changeScreenSharingRole
```

## <a name="request-headers"></a><span data-ttu-id="ad153-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ad153-121">Request headers</span></span>
| <span data-ttu-id="ad153-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="ad153-122">Name</span></span>          | <span data-ttu-id="ad153-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad153-123">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="ad153-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="ad153-124">Authorization</span></span> | <span data-ttu-id="ad153-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ad153-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ad153-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ad153-127">Request body</span></span>
<span data-ttu-id="ad153-128">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="ad153-128">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="ad153-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ad153-129">Parameter</span></span>      | <span data-ttu-id="ad153-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad153-130">Type</span></span>    |<span data-ttu-id="ad153-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad153-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ad153-132">role</span><span class="sxs-lookup"><span data-stu-id="ad153-132">role</span></span>|<span data-ttu-id="ad153-133">String</span><span class="sxs-lookup"><span data-stu-id="ad153-133">String</span></span>|<span data-ttu-id="ad153-134">Los valores posibles son: 'Visor', 'Que comparte'</span><span class="sxs-lookup"><span data-stu-id="ad153-134">Possible values are: 'Viewer', 'Sharer'</span></span>|

## <a name="response"></a><span data-ttu-id="ad153-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad153-135">Response</span></span>
<span data-ttu-id="ad153-136">Devuelve `202 Accepted` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="ad153-136">Returns `202 Accepted` response code.</span></span>

## <a name="example"></a><span data-ttu-id="ad153-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ad153-137">Example</span></span>
<span data-ttu-id="ad153-138">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="ad153-138">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="ad153-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ad153-139">Request</span></span>
<span data-ttu-id="ad153-140">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ad153-140">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "call_changeScreenSharingRole"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/changeScreenSharingRole
Content-Type: application/json
Content-Length: 24

{
  "role": "viewer"
}
```

##### <a name="response"></a><span data-ttu-id="ad153-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad153-141">Response</span></span>
<span data-ttu-id="ad153-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ad153-142">Here is an example of the response.</span></span> 

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