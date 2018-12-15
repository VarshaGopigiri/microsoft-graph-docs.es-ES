---
title: 'usuario: exportPersonalData'
description: Envía una solicitud de operación de la directiva de datos, realizada por un administrador de la compañía para exportar datos de un usuario organizativa.
ms.openlocfilehash: 7d41d6d855fee992a4ff3a542e6c11f692adcfe3
ms.sourcegitcommit: f3d479edf03935d0edbbc7668a65f7cde2a56c92
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/15/2018
ms.locfileid: "27284136"
---
# <a name="user-exportpersonaldata"></a><span data-ttu-id="79b1d-103">usuario: exportPersonalData</span><span class="sxs-lookup"><span data-stu-id="79b1d-103">user: exportPersonalData</span></span>

<span data-ttu-id="79b1d-104">Enviar una solicitud de operación de directiva de datos de una aplicación para exportar datos de un usuario organizativa o un administrador de la compañía.</span><span class="sxs-lookup"><span data-stu-id="79b1d-104">Submit a data policy operation request from a company administrator or an application to export an organizational user's data.</span></span>

## <a name="permissions"></a><span data-ttu-id="79b1d-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="79b1d-105">Permissions</span></span>
<span data-ttu-id="79b1d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="79b1d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="79b1d-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="79b1d-108">Permission type</span></span>      | <span data-ttu-id="79b1d-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="79b1d-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="79b1d-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="79b1d-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="79b1d-111">User.Export.All, User.Read.All</span><span class="sxs-lookup"><span data-stu-id="79b1d-111">User.Export.All, User.Read.All</span></span>  |
|<span data-ttu-id="79b1d-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="79b1d-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="79b1d-113">No aplicable</span><span class="sxs-lookup"><span data-stu-id="79b1d-113">Not applicable</span></span>  |
|<span data-ttu-id="79b1d-114">Application</span><span class="sxs-lookup"><span data-stu-id="79b1d-114">Application</span></span> | <span data-ttu-id="79b1d-115">User.Export.All, User.Read.All</span><span class="sxs-lookup"><span data-stu-id="79b1d-115">User.Export.All, User.Read.All</span></span> |

><span data-ttu-id="79b1d-116">**Nota:** La exportación puede realizarse sólo por un administrador de la compañía cuando se usan los permisos delegados.</span><span class="sxs-lookup"><span data-stu-id="79b1d-116">**Note:** The export can only be performed by a company administrator when delegated permissions are used.</span></span>

## <a name="http-request"></a><span data-ttu-id="79b1d-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="79b1d-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id}/exportPersonalData

```
## <a name="request-headers"></a><span data-ttu-id="79b1d-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="79b1d-118">Request headers</span></span>
| <span data-ttu-id="79b1d-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="79b1d-119">Name</span></span>       | <span data-ttu-id="79b1d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="79b1d-120">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="79b1d-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="79b1d-121">Authorization</span></span>  | <span data-ttu-id="79b1d-122">Bearer {token}</span><span class="sxs-lookup"><span data-stu-id="79b1d-122">Bearer {token}</span></span>|

## <a name="request-body"></a><span data-ttu-id="79b1d-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="79b1d-123">Request body</span></span>
<span data-ttu-id="79b1d-124">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="79b1d-124">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="79b1d-125">Parámetro</span><span class="sxs-lookup"><span data-stu-id="79b1d-125">Parameter</span></span>    | <span data-ttu-id="79b1d-126">Type</span><span class="sxs-lookup"><span data-stu-id="79b1d-126">Type</span></span>   |<span data-ttu-id="79b1d-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="79b1d-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="79b1d-128">storageLocation</span><span class="sxs-lookup"><span data-stu-id="79b1d-128">storageLocation</span></span>|<span data-ttu-id="79b1d-129">String</span><span class="sxs-lookup"><span data-stu-id="79b1d-129">String</span></span>|<span data-ttu-id="79b1d-130">Esto es una dirección URL de firma (SAS) de acceso compartido a una cuenta de almacenamiento de Azure, para que se deben exportar los datos.</span><span class="sxs-lookup"><span data-stu-id="79b1d-130">This is a shared access signature (SAS) URL to an Azure Storage account, to where data should be exported.</span></span>|

## <a name="response"></a><span data-ttu-id="79b1d-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79b1d-131">Response</span></span>
<span data-ttu-id="79b1d-p102">Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="79b1d-p102">If successful, this method returns a `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="79b1d-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="79b1d-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="79b1d-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="79b1d-135">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "user_exportpersonaldata"
}-->
```http
POST https://graph.microsoft.com/v1.0/users/{id}/exportPersonalData
Content-type: application/json
Content-length: 48

{
  "storageLocation": "storageLocation-value"
}
```

##### <a name="response"></a><span data-ttu-id="79b1d-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79b1d-136">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: exportPersonalData",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
