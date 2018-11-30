---
title: Create registeredOwner
description: Agrega un usuario como propietario registrado del dispositivo.
ms.openlocfilehash: 976f4f788716ad1e739ceeaaa1db61963b002f45
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029145"
---
# <a name="create-registeredowner"></a><span data-ttu-id="4ee0a-103">Create registeredOwner</span><span class="sxs-lookup"><span data-stu-id="4ee0a-103">Create registeredOwner</span></span>

<span data-ttu-id="4ee0a-104">Agrega un usuario como propietario registrado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ee0a-104">Add a user as a registered owner of the device.</span></span>
## <a name="permissions"></a><span data-ttu-id="4ee0a-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="4ee0a-105">Permissions</span></span>
<span data-ttu-id="4ee0a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4ee0a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="4ee0a-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4ee0a-108">Permission type</span></span>      | <span data-ttu-id="4ee0a-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4ee0a-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4ee0a-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4ee0a-110">Delegated (work or school account)</span></span> | <span data-ttu-id="4ee0a-111">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="4ee0a-111">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="4ee0a-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4ee0a-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4ee0a-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4ee0a-113">Not supported.</span></span>    |
|<span data-ttu-id="4ee0a-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4ee0a-114">Application</span></span> | <span data-ttu-id="4ee0a-115">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4ee0a-115">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4ee0a-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4ee0a-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /devices/{id}/registeredOwners/$ref

```
## <a name="request-headers"></a><span data-ttu-id="4ee0a-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4ee0a-117">Request headers</span></span>
| <span data-ttu-id="4ee0a-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="4ee0a-118">Name</span></span>       | <span data-ttu-id="4ee0a-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="4ee0a-119">Type</span></span> | <span data-ttu-id="4ee0a-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ee0a-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="4ee0a-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="4ee0a-121">Authorization</span></span>  | <span data-ttu-id="4ee0a-122">string</span><span class="sxs-lookup"><span data-stu-id="4ee0a-122">string</span></span>  | <span data-ttu-id="4ee0a-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4ee0a-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4ee0a-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4ee0a-125">Request body</span></span>
<span data-ttu-id="4ee0a-126">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="4ee0a-126">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="4ee0a-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4ee0a-127">Response</span></span>

<span data-ttu-id="4ee0a-128">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4ee0a-128">If successful, this method returns `201 Created` response code and [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4ee0a-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4ee0a-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4ee0a-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4ee0a-130">Request</span></span>
<span data-ttu-id="4ee0a-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4ee0a-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_device"
}-->
```http
POST https://graph.microsoft.com/v1.0/devices/{id}/registeredOwners
Content-type: application/json
Content-length: 30

{
  "directoryObject": {
  }
}
```
<span data-ttu-id="4ee0a-132">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="4ee0a-132">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="4ee0a-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4ee0a-133">Response</span></span>
<span data-ttu-id="4ee0a-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4ee0a-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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