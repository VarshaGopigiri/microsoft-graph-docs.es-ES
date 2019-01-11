---
title: Create registeredOwner
description: Agrega un usuario como propietario registrado del dispositivo.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e1c8151f43ea7c4eb8e1235727a6b9f40f193853
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27824265"
---
# <a name="create-registeredowner"></a><span data-ttu-id="448bd-103">Create registeredOwner</span><span class="sxs-lookup"><span data-stu-id="448bd-103">Create registeredOwner</span></span>

> <span data-ttu-id="448bd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="448bd-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="448bd-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="448bd-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="448bd-106">Agrega un usuario como propietario registrado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="448bd-106">Add a user as a registered owner of the device.</span></span>
## <a name="permissions"></a><span data-ttu-id="448bd-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="448bd-107">Permissions</span></span>
<span data-ttu-id="448bd-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="448bd-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="448bd-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="448bd-110">Permission type</span></span>      | <span data-ttu-id="448bd-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="448bd-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="448bd-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="448bd-112">Delegated (work or school account)</span></span> | <span data-ttu-id="448bd-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="448bd-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="448bd-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="448bd-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="448bd-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="448bd-115">Not supported.</span></span>    |
|<span data-ttu-id="448bd-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="448bd-116">Application</span></span> | <span data-ttu-id="448bd-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="448bd-117">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="448bd-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="448bd-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /devices/{id}/registeredOwners/$ref

```
## <a name="request-headers"></a><span data-ttu-id="448bd-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="448bd-119">Request headers</span></span>
| <span data-ttu-id="448bd-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="448bd-120">Name</span></span>       | <span data-ttu-id="448bd-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="448bd-121">Type</span></span> | <span data-ttu-id="448bd-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="448bd-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="448bd-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="448bd-123">Authorization</span></span>  | <span data-ttu-id="448bd-124">string</span><span class="sxs-lookup"><span data-stu-id="448bd-124">string</span></span>  | <span data-ttu-id="448bd-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="448bd-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="448bd-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="448bd-127">Request body</span></span>
<span data-ttu-id="448bd-128">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="448bd-128">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="448bd-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="448bd-129">Response</span></span>

<span data-ttu-id="448bd-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="448bd-130">If successful, this method returns `201 Created` response code and [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="448bd-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="448bd-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="448bd-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="448bd-132">Request</span></span>
<span data-ttu-id="448bd-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="448bd-133">Here is an example of the request.</span></span>
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
<span data-ttu-id="448bd-134">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="448bd-134">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="448bd-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="448bd-135">Response</span></span>
<span data-ttu-id="448bd-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="448bd-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
