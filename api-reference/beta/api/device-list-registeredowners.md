---
title: List registeredOwners
description: Recupera una lista de usuarios que son propietarios registrados del dispositivo. El usuario registrado es el usuario que ha unido el dispositivo a la nube o que ha registrado su dispositivo personal. El propietario registrado se establece en el momento del registro. Actualmente, solo puede haber un propietario.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: ebf6350de33d2dfa70f9c098cd618abf7d7df4ce
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27931716"
---
# <a name="list-registeredowners"></a><span data-ttu-id="f850f-106">List registeredOwners</span><span class="sxs-lookup"><span data-stu-id="f850f-106">List registeredOwners</span></span>

> <span data-ttu-id="f850f-107">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f850f-107">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f850f-108">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f850f-108">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f850f-109">Recupera una lista de usuarios que son propietarios registrados del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f850f-109">Retrieve a list of users that are registered owners of the device.</span></span> <span data-ttu-id="f850f-110">El usuario registrado es el usuario que ha unido el dispositivo a la nube o que ha registrado su dispositivo personal.</span><span class="sxs-lookup"><span data-stu-id="f850f-110">A registered owner is the user that cloud joined the device or registered their personal device.</span></span> <span data-ttu-id="f850f-111">El propietario registrado se establece en el momento del registro.</span><span class="sxs-lookup"><span data-stu-id="f850f-111">The registered owner is set at the time of registration.</span></span> <span data-ttu-id="f850f-112">Actualmente, solo puede haber un propietario.</span><span class="sxs-lookup"><span data-stu-id="f850f-112">Currently, there can be only one owner.</span></span>

## <a name="permissions"></a><span data-ttu-id="f850f-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="f850f-113">Permissions</span></span>

<span data-ttu-id="f850f-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f850f-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f850f-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f850f-116">Permission type</span></span>      | <span data-ttu-id="f850f-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f850f-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f850f-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f850f-118">Delegated (work or school account)</span></span> | <span data-ttu-id="f850f-119">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="f850f-119">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="f850f-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f850f-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f850f-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f850f-121">Not supported.</span></span>    |
|<span data-ttu-id="f850f-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f850f-122">Application</span></span> | <span data-ttu-id="f850f-123">Directory.Read.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f850f-123">Directory.Read.All or Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f850f-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f850f-124">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices/{id}/registeredOwners
```

> <span data-ttu-id="f850f-125">Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".</span><span class="sxs-lookup"><span data-stu-id="f850f-125">Note: The "id" in the request is the "id" property of the device, not the "deviceId" property.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="f850f-126">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f850f-126">Optional query parameters</span></span>
<span data-ttu-id="f850f-127">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f850f-127">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="f850f-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f850f-128">Request headers</span></span>
| <span data-ttu-id="f850f-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="f850f-129">Name</span></span>       | <span data-ttu-id="f850f-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="f850f-130">Type</span></span> | <span data-ttu-id="f850f-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="f850f-131">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="f850f-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="f850f-132">Authorization</span></span>  | <span data-ttu-id="f850f-133">string</span><span class="sxs-lookup"><span data-stu-id="f850f-133">string</span></span>  | <span data-ttu-id="f850f-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f850f-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f850f-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f850f-136">Request body</span></span>
<span data-ttu-id="f850f-137">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f850f-137">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f850f-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f850f-138">Response</span></span>

<span data-ttu-id="f850f-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f850f-139">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="f850f-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f850f-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f850f-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f850f-141">Request</span></span>
<span data-ttu-id="f850f-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f850f-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_registeredowners"
}-->
```http
GET https://graph.microsoft.com/beta/devices/{id}/registeredOwners
```
##### <a name="response"></a><span data-ttu-id="f850f-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f850f-143">Response</span></span>
<span data-ttu-id="f850f-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f850f-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 55

{
  "value": [
    {
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List registeredOwners",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
