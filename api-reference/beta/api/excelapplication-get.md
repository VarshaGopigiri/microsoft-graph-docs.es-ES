---
title: Obtener la aplicación
description: Recuperar las propiedades y relaciones del objeto application.
localization_priority: Normal
ms.openlocfilehash: 9226e697f3e8439740003887d8560ffaac9df2fa
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27864494"
---
# <a name="get-application"></a><span data-ttu-id="d487b-103">Obtener la aplicación</span><span class="sxs-lookup"><span data-stu-id="d487b-103">Get Application</span></span>

> <span data-ttu-id="d487b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d487b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d487b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d487b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d487b-106">Recuperar las propiedades y relaciones del objeto application.</span><span class="sxs-lookup"><span data-stu-id="d487b-106">Retrieve the properties and relationships of application object.</span></span>
## <a name="permissions"></a><span data-ttu-id="d487b-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d487b-107">Permissions</span></span>
<span data-ttu-id="d487b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d487b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d487b-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d487b-110">Permission type</span></span>      | <span data-ttu-id="d487b-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d487b-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d487b-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d487b-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d487b-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d487b-113">Not supported.</span></span>    |
|<span data-ttu-id="d487b-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d487b-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d487b-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d487b-115">Not supported.</span></span>    |
|<span data-ttu-id="d487b-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d487b-116">Application</span></span> | <span data-ttu-id="d487b-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d487b-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d487b-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d487b-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/application
```
## <a name="optional-query-parameters"></a><span data-ttu-id="d487b-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="d487b-119">Optional query parameters</span></span>
<span data-ttu-id="d487b-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d487b-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="d487b-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d487b-121">Request headers</span></span>
| <span data-ttu-id="d487b-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="d487b-122">Name</span></span>      |<span data-ttu-id="d487b-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="d487b-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="d487b-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="d487b-124">Authorization</span></span>  | <span data-ttu-id="d487b-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d487b-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d487b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d487b-127">Request body</span></span>
<span data-ttu-id="d487b-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d487b-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d487b-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d487b-129">Response</span></span>

<span data-ttu-id="d487b-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el objeto de [aplicación](../resources/application.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d487b-130">If successful, this method returns a `200 OK` response code and [Application](../resources/application.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="d487b-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d487b-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d487b-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d487b-132">Request</span></span>
<span data-ttu-id="d487b-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d487b-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_application"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/application
```
##### <a name="response"></a><span data-ttu-id="d487b-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d487b-134">Response</span></span>
<span data-ttu-id="d487b-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d487b-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.application"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 48

{
  "calculationMode": "calculationMode-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get Application",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
