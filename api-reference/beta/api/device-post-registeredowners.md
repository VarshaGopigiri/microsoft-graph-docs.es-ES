---
title: Create registeredOwner
description: Agrega un usuario como propietario registrado del dispositivo.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 3db0e62e30dd5776283b93bd2a786bd0f398621d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27960899"
---
# <a name="create-registeredowner"></a><span data-ttu-id="cffaa-103">Create registeredOwner</span><span class="sxs-lookup"><span data-stu-id="cffaa-103">Create registeredOwner</span></span>

> <span data-ttu-id="cffaa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cffaa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cffaa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cffaa-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="cffaa-106">Agrega un usuario como propietario registrado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cffaa-106">Add a user as a registered owner of the device.</span></span>
## <a name="permissions"></a><span data-ttu-id="cffaa-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="cffaa-107">Permissions</span></span>
<span data-ttu-id="cffaa-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cffaa-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="cffaa-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cffaa-110">Permission type</span></span>      | <span data-ttu-id="cffaa-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cffaa-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cffaa-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cffaa-112">Delegated (work or school account)</span></span> | <span data-ttu-id="cffaa-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="cffaa-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="cffaa-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cffaa-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cffaa-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cffaa-115">Not supported.</span></span>    |
|<span data-ttu-id="cffaa-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cffaa-116">Application</span></span> | <span data-ttu-id="cffaa-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cffaa-117">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="cffaa-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cffaa-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /devices/{id}/registeredOwners/$ref

```
## <a name="request-headers"></a><span data-ttu-id="cffaa-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cffaa-119">Request headers</span></span>
| <span data-ttu-id="cffaa-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="cffaa-120">Name</span></span>       | <span data-ttu-id="cffaa-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="cffaa-121">Type</span></span> | <span data-ttu-id="cffaa-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="cffaa-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="cffaa-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="cffaa-123">Authorization</span></span>  | <span data-ttu-id="cffaa-124">string</span><span class="sxs-lookup"><span data-stu-id="cffaa-124">string</span></span>  | <span data-ttu-id="cffaa-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cffaa-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="cffaa-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cffaa-127">Request body</span></span>
<span data-ttu-id="cffaa-128">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="cffaa-128">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="cffaa-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cffaa-129">Response</span></span>

<span data-ttu-id="cffaa-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cffaa-130">If successful, this method returns `201 Created` response code and [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cffaa-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cffaa-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="cffaa-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cffaa-132">Request</span></span>
<span data-ttu-id="cffaa-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cffaa-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_device"
}-->
```http
POST https://graph.microsoft.com/beta/devices/{id}/registeredOwners/$ref
Content-type: application/json
Content-length: 30

{
  "directoryObject": {
  }
}
```
<span data-ttu-id="cffaa-134">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="cffaa-134">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="cffaa-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cffaa-135">Response</span></span>
<span data-ttu-id="cffaa-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cffaa-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Create registeredOwner",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
