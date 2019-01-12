---
title: Creación de miembro
description: Utilice esta API para crear un nuevo miembro.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: ca5aa856f1f2e64f3a3b73ccff15f686c048cfda
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27970006"
---
# <a name="create-memberof"></a><span data-ttu-id="bfad2-103">Creación de miembro</span><span class="sxs-lookup"><span data-stu-id="bfad2-103">Create memberOf</span></span>

> <span data-ttu-id="bfad2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bfad2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bfad2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bfad2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bfad2-106">Utilice esta API para crear un nuevo miembro.</span><span class="sxs-lookup"><span data-stu-id="bfad2-106">Use this API to create a new memberOf.</span></span>
## <a name="permissions"></a><span data-ttu-id="bfad2-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="bfad2-107">Permissions</span></span>
<span data-ttu-id="bfad2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bfad2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bfad2-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bfad2-110">Permission type</span></span>      | <span data-ttu-id="bfad2-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bfad2-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bfad2-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bfad2-112">Delegated (work or school account)</span></span> | <span data-ttu-id="bfad2-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bfad2-113">Not supported.</span></span>    |
|<span data-ttu-id="bfad2-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bfad2-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bfad2-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bfad2-115">Not supported.</span></span>    |
|<span data-ttu-id="bfad2-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bfad2-116">Application</span></span> | <span data-ttu-id="bfad2-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bfad2-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="bfad2-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bfad2-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /contacts/{id}/memberOf

```
## <a name="request-headers"></a><span data-ttu-id="bfad2-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bfad2-119">Request headers</span></span>
| <span data-ttu-id="bfad2-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="bfad2-120">Name</span></span>       | <span data-ttu-id="bfad2-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="bfad2-121">Type</span></span> | <span data-ttu-id="bfad2-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfad2-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="bfad2-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="bfad2-123">Authorization</span></span>  | <span data-ttu-id="bfad2-124">string</span><span class="sxs-lookup"><span data-stu-id="bfad2-124">string</span></span>  | <span data-ttu-id="bfad2-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bfad2-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bfad2-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bfad2-127">Request body</span></span>
<span data-ttu-id="bfad2-128">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="bfad2-128">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="bfad2-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bfad2-129">Response</span></span>

<span data-ttu-id="bfad2-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bfad2-130">If successful, this method returns `201 Created` response code and [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bfad2-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bfad2-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bfad2-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bfad2-132">Request</span></span>
<span data-ttu-id="bfad2-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bfad2-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_orgcontact"
}-->
```http
POST https://graph.microsoft.com/beta/contacts/{id}/memberOf
Content-type: application/json
Content-length: 30

{
  "directoryObject": {
  }
}
```
<span data-ttu-id="bfad2-134">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="bfad2-134">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="bfad2-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bfad2-135">Response</span></span>
<span data-ttu-id="bfad2-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bfad2-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 51

{
  "directoryObject": {
    "id": "id-value"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create memberOf",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
