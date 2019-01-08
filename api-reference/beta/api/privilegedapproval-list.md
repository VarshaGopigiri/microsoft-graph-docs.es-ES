---
title: Lista privilegedApproval
description: Recuperar una lista de objetos de privilegedapproval.
ms.openlocfilehash: 35b3e2cf6b4034731c8ddf9d1af41e129acbfe3f
ms.sourcegitcommit: 37591c2299c80e7675cd2b5f781e1eeeba628a60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2019
ms.locfileid: "27748174"
---
# <a name="list-privilegedapproval"></a><span data-ttu-id="a8854-103">Lista privilegedApproval</span><span class="sxs-lookup"><span data-stu-id="a8854-103">List privilegedApproval</span></span>

> <span data-ttu-id="a8854-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a8854-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a8854-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a8854-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a8854-106">Recuperar una lista de objetos de privilegedapproval.</span><span class="sxs-lookup"><span data-stu-id="a8854-106">Retrieve a list of privilegedapproval objects.</span></span>

<span data-ttu-id="a8854-107">Para filtrar los resultados de la consulta, use el estándar OData ``$filter`` expresiones en los URI.</span><span class="sxs-lookup"><span data-stu-id="a8854-107">To filter the results from the query, use the standard OData ``$filter`` expressions in the URIs.</span></span>
## <a name="permissions"></a><span data-ttu-id="a8854-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="a8854-108">Permissions</span></span>
<span data-ttu-id="a8854-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a8854-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="a8854-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a8854-111">Permission type</span></span>      | <span data-ttu-id="a8854-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a8854-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a8854-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a8854-113">Delegated (work or school account)</span></span> | <span data-ttu-id="a8854-114">PrivilegedAccess.ReadWrite.AzureAD, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="a8854-114">PrivilegedAccess.ReadWrite.AzureAD, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="a8854-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a8854-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a8854-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a8854-116">Not supported.</span></span>    |
|<span data-ttu-id="a8854-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a8854-117">Application</span></span> | <span data-ttu-id="a8854-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a8854-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a8854-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a8854-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedApproval
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a8854-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a8854-120">Optional query parameters</span></span>
<span data-ttu-id="a8854-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a8854-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a8854-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a8854-122">Request headers</span></span>
| <span data-ttu-id="a8854-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="a8854-123">Name</span></span>      |<span data-ttu-id="a8854-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8854-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="a8854-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="a8854-125">Authorization</span></span>  | <span data-ttu-id="a8854-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a8854-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a8854-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a8854-128">Request body</span></span>
<span data-ttu-id="a8854-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a8854-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a8854-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a8854-130">Response</span></span>

<span data-ttu-id="a8854-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [privilegedApproval](../resources/privilegedapproval.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a8854-131">If successful, this method returns a `200 OK` response code and collection of [privilegedApproval](../resources/privilegedapproval.md) objects in the response body.</span></span>

<span data-ttu-id="a8854-132">Tenga en cuenta que el inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="a8854-132">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="a8854-133">De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="a8854-133">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>

## <a name="example"></a><span data-ttu-id="a8854-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a8854-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a8854-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a8854-135">Request</span></span>
<span data-ttu-id="a8854-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a8854-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_privilegedapproval"
}-->
```http
GET https://graph.microsoft.com/beta/privilegedApproval
```
##### <a name="response"></a><span data-ttu-id="a8854-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a8854-137">Response</span></span>
<span data-ttu-id="a8854-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a8854-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedApproval",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 246

{
  "value": [
    {
      "id": "id-value",
      "userId": "userId-value",
      "roleId": "roleId-value",
      "approvalType": "approvalType-value",
      "approvalState": "approvalState-value",
      "approvalDuration": "datetime-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List privilegedApproval",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
