---
title: Crear propietario
description: Utilice esta API para crear un nuevo propietario.
ms.openlocfilehash: fdfbaf31b954b7621b7c59fc61741c12644aaf4b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084661"
---
# <a name="create-owner"></a><span data-ttu-id="eec88-103">Crear propietario</span><span class="sxs-lookup"><span data-stu-id="eec88-103">Create owner</span></span>

> <span data-ttu-id="eec88-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eec88-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eec88-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eec88-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="eec88-106">Utilice esta API para crear un nuevo propietario.</span><span class="sxs-lookup"><span data-stu-id="eec88-106">Use this API to create a new owner.</span></span>
## <a name="permissions"></a><span data-ttu-id="eec88-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="eec88-107">Permissions</span></span>
<span data-ttu-id="eec88-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eec88-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eec88-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eec88-110">Permission type</span></span>      | <span data-ttu-id="eec88-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eec88-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="eec88-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eec88-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="eec88-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="eec88-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="eec88-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eec88-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="eec88-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eec88-115">Not supported.</span></span>    |
|<span data-ttu-id="eec88-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eec88-116">Application</span></span> | <span data-ttu-id="eec88-117">Application.ReadWrite.OwnedBy y Directory.Read.All, Application.ReadWrite.All y Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="eec88-117">Application.ReadWrite.OwnedBy and Directory.Read.All, Application.ReadWrite.All and Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="eec88-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eec88-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /applications/{id}/owners

```
## <a name="request-headers"></a><span data-ttu-id="eec88-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eec88-119">Request headers</span></span>
| <span data-ttu-id="eec88-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="eec88-120">Name</span></span>       | <span data-ttu-id="eec88-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="eec88-121">Type</span></span> | <span data-ttu-id="eec88-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="eec88-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="eec88-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="eec88-123">Authorization</span></span>  | <span data-ttu-id="eec88-124">string</span><span class="sxs-lookup"><span data-stu-id="eec88-124">string</span></span>  | <span data-ttu-id="eec88-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eec88-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="eec88-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eec88-127">Request body</span></span>
<span data-ttu-id="eec88-128">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="eec88-128">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="eec88-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eec88-129">Response</span></span>

<span data-ttu-id="eec88-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eec88-130">If successful, this method returns `201 Created` response code and [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eec88-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eec88-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="eec88-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eec88-132">Request</span></span>
<span data-ttu-id="eec88-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eec88-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_application"
}-->
```http
POST https://graph.microsoft.com/beta/applications/{id}/owners
Content-type: application/json
Content-length: 30

{
  "directoryObject": {
  }
}
```
<span data-ttu-id="eec88-134">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="eec88-134">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="eec88-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eec88-135">Response</span></span>
<span data-ttu-id="eec88-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eec88-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Create owner",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->