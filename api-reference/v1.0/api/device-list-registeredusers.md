---
title: List registeredUsers
description: Recupera una lista de usuarios que son usuarios registrados del dispositivo.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 58b691bbf71dde1aa6247cfa19164f8cc44b3674
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27846392"
---
# <a name="list-registeredusers"></a><span data-ttu-id="ea32d-103">List registeredUsers</span><span class="sxs-lookup"><span data-stu-id="ea32d-103">List registeredUsers</span></span>

<span data-ttu-id="ea32d-104">Recupera una lista de usuarios que son usuarios registrados del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea32d-104">Retrieve a list of users that are registered users of the device.</span></span>

<span data-ttu-id="ea32d-105">En el caso de los dispositivos unidos a la nube y los dispositivos personales registrados, los usuarios registrados se establecen en el mismo valor que los propietarios registrados en el momento del registro.</span><span class="sxs-lookup"><span data-stu-id="ea32d-105">For cloud joined devices and registered personal devices, registered users are set to the same value as registered owners at the time of registration.</span></span>

## <a name="permissions"></a><span data-ttu-id="ea32d-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="ea32d-106">Permissions</span></span>
<span data-ttu-id="ea32d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ea32d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="ea32d-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ea32d-109">Permission type</span></span>      | <span data-ttu-id="ea32d-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ea32d-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ea32d-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ea32d-111">Delegated (work or school account)</span></span> | <span data-ttu-id="ea32d-112">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="ea32d-112">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="ea32d-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ea32d-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ea32d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea32d-114">Not supported.</span></span>    |
|<span data-ttu-id="ea32d-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ea32d-115">Application</span></span> | <span data-ttu-id="ea32d-116">Directory.Read.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ea32d-116">Directory.Read.All or Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ea32d-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ea32d-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices/{id}/registeredUsers
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ea32d-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ea32d-118">Optional query parameters</span></span>
<span data-ttu-id="ea32d-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea32d-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="ea32d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ea32d-120">Request headers</span></span>
| <span data-ttu-id="ea32d-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="ea32d-121">Name</span></span>       | <span data-ttu-id="ea32d-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea32d-122">Type</span></span> | <span data-ttu-id="ea32d-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea32d-123">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="ea32d-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="ea32d-124">Authorization</span></span>  | <span data-ttu-id="ea32d-125">string</span><span class="sxs-lookup"><span data-stu-id="ea32d-125">string</span></span>  | <span data-ttu-id="ea32d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ea32d-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ea32d-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ea32d-128">Request body</span></span>
<span data-ttu-id="ea32d-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ea32d-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ea32d-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea32d-130">Response</span></span>

<span data-ttu-id="ea32d-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea32d-131">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ea32d-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ea32d-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ea32d-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ea32d-133">Request</span></span>
<span data-ttu-id="ea32d-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea32d-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_registeredusers"
}-->
```http
GET https://graph.microsoft.com/v1.0/devices/{id}/registeredUsers
```
##### <a name="response"></a><span data-ttu-id="ea32d-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea32d-135">Response</span></span>
<span data-ttu-id="ea32d-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ea32d-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List registeredUsers",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
