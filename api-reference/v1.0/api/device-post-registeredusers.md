---
title: Create registeredUser
description: Agrega un usuario registrado para el dispositivo.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 224475a5727f7ed048aed1aa3ec33fd48f1b0248
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917653"
---
# <a name="create-registereduser"></a><span data-ttu-id="c742c-103">Create registeredUser</span><span class="sxs-lookup"><span data-stu-id="c742c-103">Create registeredUser</span></span>

<span data-ttu-id="c742c-104">Agrega un usuario registrado para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c742c-104">Add a registered user for the device.</span></span>

## <a name="permissions"></a><span data-ttu-id="c742c-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="c742c-105">Permissions</span></span>
<span data-ttu-id="c742c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c742c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="c742c-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c742c-108">Permission type</span></span>      | <span data-ttu-id="c742c-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c742c-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c742c-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c742c-110">Delegated (work or school account)</span></span> | <span data-ttu-id="c742c-111">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="c742c-111">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="c742c-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c742c-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c742c-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c742c-113">Not supported.</span></span>    |
|<span data-ttu-id="c742c-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c742c-114">Application</span></span> | <span data-ttu-id="c742c-115">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c742c-115">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c742c-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c742c-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /devices/{id}/registeredUsers/$ref

```
## <a name="request-headers"></a><span data-ttu-id="c742c-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c742c-117">Request headers</span></span>
| <span data-ttu-id="c742c-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="c742c-118">Name</span></span>       | <span data-ttu-id="c742c-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="c742c-119">Type</span></span> | <span data-ttu-id="c742c-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="c742c-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="c742c-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="c742c-121">Authorization</span></span>  | <span data-ttu-id="c742c-122">string</span><span class="sxs-lookup"><span data-stu-id="c742c-122">string</span></span>  | <span data-ttu-id="c742c-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c742c-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c742c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c742c-125">Request body</span></span>
<span data-ttu-id="c742c-126">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="c742c-126">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="c742c-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c742c-127">Response</span></span>

<span data-ttu-id="c742c-128">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c742c-128">If successful, this method returns `201 Created` response code and [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c742c-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c742c-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c742c-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c742c-130">Request</span></span>
<span data-ttu-id="c742c-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c742c-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_device"
}-->
```http
POST https://graph.microsoft.com/v1.0/devices/{id}/registeredUsers
Content-type: application/json
Content-length: 30

{
  "directoryObject": {
  }
}
```
<span data-ttu-id="c742c-132">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="c742c-132">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="c742c-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c742c-133">Response</span></span>
<span data-ttu-id="c742c-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c742c-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Create registeredUser",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
