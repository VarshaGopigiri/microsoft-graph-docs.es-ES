---
title: List pivotTables
description: Recuperar una lista de objetos workbookpivottable.
ms.openlocfilehash: 21a1056b45462c1ac719e8af45fa5dfbaf428ee4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084446"
---
# <a name="list-pivottables"></a><span data-ttu-id="08b2a-103">List pivotTables</span><span class="sxs-lookup"><span data-stu-id="08b2a-103">List pivotTables</span></span>

> <span data-ttu-id="08b2a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="08b2a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="08b2a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="08b2a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="08b2a-106">Recuperar una lista de objetos workbookpivottable.</span><span class="sxs-lookup"><span data-stu-id="08b2a-106">Retrieve a list of workbookpivottable objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="08b2a-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="08b2a-107">Permissions</span></span>
<span data-ttu-id="08b2a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="08b2a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="08b2a-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="08b2a-110">Permission type</span></span>      | <span data-ttu-id="08b2a-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="08b2a-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="08b2a-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="08b2a-112">Delegated (work or school account)</span></span> | <span data-ttu-id="08b2a-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="08b2a-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="08b2a-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="08b2a-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="08b2a-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="08b2a-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="08b2a-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="08b2a-116">Application</span></span> | <span data-ttu-id="08b2a-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="08b2a-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="08b2a-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="08b2a-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/drive/root/workbook/worksheets/{id}/pivotTables
```
## <a name="optional-query-parameters"></a><span data-ttu-id="08b2a-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="08b2a-119">Optional query parameters</span></span>
<span data-ttu-id="08b2a-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="08b2a-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="08b2a-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="08b2a-121">Request headers</span></span>
| <span data-ttu-id="08b2a-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="08b2a-122">Name</span></span>      |<span data-ttu-id="08b2a-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="08b2a-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="08b2a-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="08b2a-124">Authorization</span></span>  | <span data-ttu-id="08b2a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="08b2a-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="08b2a-127">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="08b2a-127">Workbook-Session-Id</span></span>  | <span data-ttu-id="08b2a-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="08b2a-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="08b2a-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="08b2a-130">Request body</span></span>
<span data-ttu-id="08b2a-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="08b2a-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="08b2a-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="08b2a-132">Response</span></span>

<span data-ttu-id="08b2a-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [workbookPivotTable](../resources/workbookpivottable.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="08b2a-133">If successful, this method returns a `200 OK` response code and collection of [workbookPivotTable](../resources/workbookpivottable.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="08b2a-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="08b2a-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="08b2a-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="08b2a-135">Request</span></span>
<span data-ttu-id="08b2a-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="08b2a-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_pivottables"
}-->
```http
GET https://graph.microsoft.com/beta/drive/root/workbook/worksheets/{id}/pivotTables
```
##### <a name="response"></a><span data-ttu-id="08b2a-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="08b2a-137">Response</span></span>
<span data-ttu-id="08b2a-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="08b2a-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookPivotTable",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 83

{
  "value": [
    {
      "id": "id-value",
      "name": "name-value"
    }
  ]
}
```