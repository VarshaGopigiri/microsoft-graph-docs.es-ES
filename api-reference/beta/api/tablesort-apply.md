---
title: 'TableSort: apply'
description: Realizar una operación de ordenación.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: f39108f0413917fcf1204f4c2fb6640094d25ced
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27918409"
---
# <a name="tablesort-apply"></a><span data-ttu-id="25bf3-103">TableSort: apply</span><span class="sxs-lookup"><span data-stu-id="25bf3-103">TableSort: apply</span></span>

> <span data-ttu-id="25bf3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="25bf3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="25bf3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="25bf3-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="25bf3-106">Realizar una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="25bf3-106">Perform a sort operation.</span></span>
## <a name="permissions"></a><span data-ttu-id="25bf3-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="25bf3-107">Permissions</span></span>
<span data-ttu-id="25bf3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="25bf3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="25bf3-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="25bf3-110">Permission type</span></span>      | <span data-ttu-id="25bf3-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="25bf3-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="25bf3-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="25bf3-112">Delegated (work or school account)</span></span> | <span data-ttu-id="25bf3-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="25bf3-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="25bf3-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="25bf3-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="25bf3-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="25bf3-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="25bf3-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="25bf3-116">Application</span></span> | <span data-ttu-id="25bf3-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="25bf3-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="25bf3-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="25bf3-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/sort/apply
POST /workbook/worksheets/{id|name}/tables/{id|name}/sort/apply

```
## <a name="request-headers"></a><span data-ttu-id="25bf3-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="25bf3-119">Request headers</span></span>
| <span data-ttu-id="25bf3-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="25bf3-120">Name</span></span>       | <span data-ttu-id="25bf3-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="25bf3-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="25bf3-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="25bf3-122">Authorization</span></span>  | <span data-ttu-id="25bf3-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="25bf3-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="25bf3-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="25bf3-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="25bf3-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="25bf3-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="25bf3-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="25bf3-128">Request body</span></span>
<span data-ttu-id="25bf3-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="25bf3-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="25bf3-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="25bf3-130">Parameter</span></span>    | <span data-ttu-id="25bf3-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="25bf3-131">Type</span></span>   |<span data-ttu-id="25bf3-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="25bf3-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="25bf3-133">fields</span><span class="sxs-lookup"><span data-stu-id="25bf3-133">fields</span></span>|<span data-ttu-id="25bf3-134">SortField</span><span class="sxs-lookup"><span data-stu-id="25bf3-134">SortField</span></span>|<span data-ttu-id="25bf3-135">La lista de condiciones por las que realizar la ordenación.</span><span class="sxs-lookup"><span data-stu-id="25bf3-135">The list of conditions to sort on.</span></span>|
|<span data-ttu-id="25bf3-136">matchCase</span><span class="sxs-lookup"><span data-stu-id="25bf3-136">matchCase</span></span>|<span data-ttu-id="25bf3-137">boolean</span><span class="sxs-lookup"><span data-stu-id="25bf3-137">boolean</span></span>|<span data-ttu-id="25bf3-p105">Opcional. Indica si la ordenación de cadenas distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="25bf3-p105">Optional. Whether to have the casing impact string ordering.</span></span>|
|<span data-ttu-id="25bf3-140">method</span><span class="sxs-lookup"><span data-stu-id="25bf3-140">method</span></span>|<span data-ttu-id="25bf3-141">string</span><span class="sxs-lookup"><span data-stu-id="25bf3-141">string</span></span>|<span data-ttu-id="25bf3-p106">Opcional. Método de ordenación que se usa para los caracteres chinos.  Valores posibles: `PinYin`, `StrokeCount`.</span><span class="sxs-lookup"><span data-stu-id="25bf3-p106">Optional. The ordering method used for Chinese characters.  Possible values are: `PinYin`, `StrokeCount`.</span></span>|

## <a name="response"></a><span data-ttu-id="25bf3-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="25bf3-145">Response</span></span>

<span data-ttu-id="25bf3-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="25bf3-p107">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="25bf3-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="25bf3-148">Example</span></span>
<span data-ttu-id="25bf3-149">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="25bf3-149">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="25bf3-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="25bf3-150">Request</span></span>
<span data-ttu-id="25bf3-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="25bf3-151">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablesort_apply"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/sort/apply
Content-type: application/json
Content-length: 298

{
  "fields": [
    {
      "key": 99,
      "sortOn": "sortOn-value",
      "ascending": true,
      "color": "color-value",
      "dataOption": "dataOption-value",
      "icon": {
        "set": "set-value",
        "index": 99
      }
    }
  ],
  "matchCase": true,
  "method": "method-value"
}
```

##### <a name="response"></a><span data-ttu-id="25bf3-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="25bf3-152">Response</span></span>
<span data-ttu-id="25bf3-153">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="25bf3-153">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableSort: apply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
