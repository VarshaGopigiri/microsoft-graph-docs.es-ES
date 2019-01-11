---
title: List registeredOwners
description: Recupera una lista de usuarios que son propietarios registrados del dispositivo. El usuario registrado es el usuario que ha unido el dispositivo a la nube o que ha registrado su dispositivo personal. El propietario registrado se establece en el momento del registro. Actualmente, solo puede haber un propietario.
localization_priority: Normal
ms.openlocfilehash: f2b39217485ef248cb7da203152f8e87c483096d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845685"
---
# <a name="list-registeredowners"></a><span data-ttu-id="2ede4-106">List registeredOwners</span><span class="sxs-lookup"><span data-stu-id="2ede4-106">List registeredOwners</span></span>

<span data-ttu-id="2ede4-107">Recupera una lista de usuarios que son propietarios registrados del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2ede4-107">Retrieve a list of users that are registered owners of the device.</span></span> <span data-ttu-id="2ede4-108">El usuario registrado es el usuario que ha unido el dispositivo a la nube o que ha registrado su dispositivo personal.</span><span class="sxs-lookup"><span data-stu-id="2ede4-108">A registered owner is the user that cloud joined the device or registered their personal device.</span></span> <span data-ttu-id="2ede4-109">El propietario registrado se establece en el momento del registro.</span><span class="sxs-lookup"><span data-stu-id="2ede4-109">The registered owner is set at the time of registration.</span></span> <span data-ttu-id="2ede4-110">Actualmente, solo puede haber un propietario.</span><span class="sxs-lookup"><span data-stu-id="2ede4-110">Currently, there can be only one owner.</span></span>

## <a name="permissions"></a><span data-ttu-id="2ede4-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="2ede4-111">Permissions</span></span>
<span data-ttu-id="2ede4-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2ede4-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="2ede4-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2ede4-114">Permission type</span></span>      | <span data-ttu-id="2ede4-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2ede4-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2ede4-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2ede4-116">Delegated (work or school account)</span></span> | <span data-ttu-id="2ede4-117">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="2ede4-117">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="2ede4-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2ede4-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2ede4-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2ede4-119">Not supported.</span></span>    |
|<span data-ttu-id="2ede4-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2ede4-120">Application</span></span> | <span data-ttu-id="2ede4-121">Directory.Read.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2ede4-121">Directory.Read.All or Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="2ede4-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2ede4-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices/{id}/registeredOwners
```
## <a name="optional-query-parameters"></a><span data-ttu-id="2ede4-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="2ede4-123">Optional query parameters</span></span>
<span data-ttu-id="2ede4-124">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ede4-124">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="2ede4-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2ede4-125">Request headers</span></span>
| <span data-ttu-id="2ede4-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="2ede4-126">Name</span></span>       | <span data-ttu-id="2ede4-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ede4-127">Type</span></span> | <span data-ttu-id="2ede4-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ede4-128">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="2ede4-129">Autorización</span><span class="sxs-lookup"><span data-stu-id="2ede4-129">Authorization</span></span>  | <span data-ttu-id="2ede4-130">string</span><span class="sxs-lookup"><span data-stu-id="2ede4-130">string</span></span>  | <span data-ttu-id="2ede4-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2ede4-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2ede4-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2ede4-133">Request body</span></span>
<span data-ttu-id="2ede4-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2ede4-134">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2ede4-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ede4-135">Response</span></span>

<span data-ttu-id="2ede4-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ede4-136">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="2ede4-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2ede4-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2ede4-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2ede4-138">Request</span></span>
<span data-ttu-id="2ede4-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2ede4-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_registeredowners"
}-->
```http
GET https://graph.microsoft.com/v1.0/devices/{id}/registeredOwners
```
##### <a name="response"></a><span data-ttu-id="2ede4-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ede4-140">Response</span></span>
<span data-ttu-id="2ede4-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2ede4-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
