---
title: Obtener privilegedApproval
description: Recuperar las propiedades y relaciones del objeto privilegedapproval.
localization_priority: Normal
ms.openlocfilehash: eef213416232db67bb0c1134e35d4af94734b468
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27847624"
---
# <a name="get-privilegedapproval"></a><span data-ttu-id="a0adf-103">Obtener privilegedApproval</span><span class="sxs-lookup"><span data-stu-id="a0adf-103">Get privilegedApproval</span></span>

> <span data-ttu-id="a0adf-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a0adf-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a0adf-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a0adf-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a0adf-106">Recuperar las propiedades y relaciones del objeto privilegedapproval.</span><span class="sxs-lookup"><span data-stu-id="a0adf-106">Retrieve the properties and relationships of privilegedapproval object.</span></span>
## <a name="permissions"></a><span data-ttu-id="a0adf-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a0adf-107">Permissions</span></span>
<span data-ttu-id="a0adf-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a0adf-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="a0adf-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a0adf-110">Permission type</span></span>      | <span data-ttu-id="a0adf-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a0adf-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a0adf-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a0adf-112">Delegated (work or school account)</span></span> | <span data-ttu-id="a0adf-113">PrivilegedAccess.ReadWrite.AzureAD, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="a0adf-113">PrivilegedAccess.ReadWrite.AzureAD, Directory.AccessAsUser.All</span></span>   |
|<span data-ttu-id="a0adf-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a0adf-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a0adf-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a0adf-115">Not supported.</span></span>    |
|<span data-ttu-id="a0adf-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a0adf-116">Application</span></span> | <span data-ttu-id="a0adf-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a0adf-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a0adf-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a0adf-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedApproval/<id>
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a0adf-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a0adf-119">Optional query parameters</span></span>
<span data-ttu-id="a0adf-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0adf-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a0adf-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a0adf-121">Request headers</span></span>
| <span data-ttu-id="a0adf-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="a0adf-122">Name</span></span>      |<span data-ttu-id="a0adf-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0adf-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="a0adf-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="a0adf-124">Authorization</span></span>  | <span data-ttu-id="a0adf-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a0adf-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a0adf-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a0adf-127">Request body</span></span>
<span data-ttu-id="a0adf-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a0adf-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a0adf-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0adf-129">Response</span></span>

<span data-ttu-id="a0adf-130">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [privilegedApproval](../resources/privilegedapproval.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0adf-130">If successful, this method returns a `200 OK` response code and [privilegedApproval](../resources/privilegedapproval.md) object in the response body.</span></span>

<span data-ttu-id="a0adf-131">Tenga en cuenta que el inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="a0adf-131">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="a0adf-132">De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="a0adf-132">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>

## <a name="example"></a><span data-ttu-id="a0adf-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a0adf-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a0adf-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a0adf-134">Request</span></span>
<span data-ttu-id="a0adf-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a0adf-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_privilegedapproval"
}-->
```http
GET https://graph.microsoft.com/beta/privilegedApproval/<id>
```
##### <a name="response"></a><span data-ttu-id="a0adf-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0adf-136">Response</span></span>
<span data-ttu-id="a0adf-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a0adf-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedApproval"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 193

{
  "id": "id-value",
  "userId": "userId-value",
  "roleId": "roleId-value",
  "approvalType": "approvalType-value",
  "approvalState": "approvalState-value",
  "approvalDuration": "datetime-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get privilegedApproval",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
