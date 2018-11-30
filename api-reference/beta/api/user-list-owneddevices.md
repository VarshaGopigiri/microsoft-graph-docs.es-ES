---
title: List ownedDevices
description: Obtiene la lista de dispositivos que son propiedad del usuario.
ms.openlocfilehash: c78c61bb323e92b704e7ed0457662870c69fdf33
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088191"
---
# <a name="list-owneddevices"></a><span data-ttu-id="679b1-103">List ownedDevices</span><span class="sxs-lookup"><span data-stu-id="679b1-103">List ownedDevices</span></span>

> <span data-ttu-id="679b1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="679b1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="679b1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="679b1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="679b1-106">Obtiene la lista de dispositivos que son propiedad del usuario.</span><span class="sxs-lookup"><span data-stu-id="679b1-106">Get the list of devices that are owned by the user.</span></span>
## <a name="permissions"></a><span data-ttu-id="679b1-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="679b1-107">Permissions</span></span>
<span data-ttu-id="679b1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="679b1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="679b1-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="679b1-110">Permission type</span></span>      | <span data-ttu-id="679b1-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="679b1-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="679b1-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="679b1-112">Delegated (work or school account)</span></span> | <span data-ttu-id="679b1-113">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="679b1-113">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="679b1-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="679b1-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="679b1-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="679b1-115">Not supported.</span></span>    |
|<span data-ttu-id="679b1-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="679b1-116">Application</span></span> | <span data-ttu-id="679b1-117">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="679b1-117">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="679b1-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="679b1-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/ownedDevices
```
## <a name="optional-query-parameters"></a><span data-ttu-id="679b1-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="679b1-119">Optional query parameters</span></span>
<span data-ttu-id="679b1-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="679b1-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="679b1-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="679b1-121">Request headers</span></span>
| <span data-ttu-id="679b1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="679b1-122">Header</span></span>       | <span data-ttu-id="679b1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="679b1-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="679b1-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="679b1-124">Authorization</span></span>  | <span data-ttu-id="679b1-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="679b1-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="679b1-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="679b1-127">Accept</span></span>  | <span data-ttu-id="679b1-128">application/json</span><span class="sxs-lookup"><span data-stu-id="679b1-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="679b1-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="679b1-129">Request body</span></span>
<span data-ttu-id="679b1-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="679b1-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="679b1-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="679b1-131">Response</span></span>

<span data-ttu-id="679b1-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="679b1-132">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="679b1-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="679b1-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="679b1-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="679b1-134">Request</span></span>
<span data-ttu-id="679b1-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="679b1-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_owneddevices"
}-->
```http
GET https://graph.microsoft.com/beta/me/ownedDevices
```
##### <a name="response"></a><span data-ttu-id="679b1-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="679b1-136">Response</span></span>
<span data-ttu-id="679b1-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="679b1-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List ownedDevices",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->