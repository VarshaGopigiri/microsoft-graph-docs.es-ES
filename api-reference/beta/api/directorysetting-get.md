---
title: Obtener una configuración de Active directory
description: Recuperar las propiedades de un objeto de configuración de Active directory específicos.
ms.openlocfilehash: ee0f4c2ea6120bbaba510315da304c8ab27d9e13
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085317"
---
# <a name="get-a-directory-setting"></a><span data-ttu-id="df7a1-103">Obtener una configuración de Active directory</span><span class="sxs-lookup"><span data-stu-id="df7a1-103">Get a directory setting</span></span>

> <span data-ttu-id="df7a1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="df7a1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="df7a1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="df7a1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="df7a1-106">Recuperar las propiedades de un objeto de configuración de Active directory específicos.</span><span class="sxs-lookup"><span data-stu-id="df7a1-106">Retrieve the properties of a specific directory setting object.</span></span>

> <span data-ttu-id="df7a1-107">**Nota**: la versión de /beta de esta API es sólo se aplica a los grupos.</span><span class="sxs-lookup"><span data-stu-id="df7a1-107">**Note**: The /beta version of this API is only applies to groups.</span></span> <span data-ttu-id="df7a1-108">Se ha cambiado la versión /v1.0 de esta API para *obtener groupSettings*.</span><span class="sxs-lookup"><span data-stu-id="df7a1-108">The /v1.0 version of this API has been renamed to *Get groupSettings*.</span></span>

## <a name="permissions"></a><span data-ttu-id="df7a1-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="df7a1-109">Permissions</span></span>
<span data-ttu-id="df7a1-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="df7a1-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="df7a1-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="df7a1-112">Permission type</span></span>      | <span data-ttu-id="df7a1-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="df7a1-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="df7a1-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="df7a1-114">Delegated (work or school account)</span></span> | <span data-ttu-id="df7a1-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="df7a1-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="df7a1-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="df7a1-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="df7a1-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="df7a1-117">Not supported.</span></span>    |
|<span data-ttu-id="df7a1-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="df7a1-118">Application</span></span> | <span data-ttu-id="df7a1-119">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="df7a1-119">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="df7a1-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="df7a1-120">HTTP request</span></span>
<span data-ttu-id="df7a1-121"><!-- { "blockType": "ignored" } -->Obtener un todo el inquilino específico o configuración de grupo</span><span class="sxs-lookup"><span data-stu-id="df7a1-121"><!-- { "blockType": "ignored" } --> Get a specific tenant-wide or group setting</span></span>
```http
GET /settings/{id}
GET /groups/{id}/settings/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="df7a1-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="df7a1-122">Optional query parameters</span></span>
<span data-ttu-id="df7a1-123">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="df7a1-123">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="df7a1-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="df7a1-124">Request headers</span></span>
| <span data-ttu-id="df7a1-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="df7a1-125">Name</span></span>      |<span data-ttu-id="df7a1-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="df7a1-126">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="df7a1-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="df7a1-127">Authorization</span></span>  | <span data-ttu-id="df7a1-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="df7a1-p104">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="df7a1-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="df7a1-130">Request body</span></span>
<span data-ttu-id="df7a1-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="df7a1-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="df7a1-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="df7a1-132">Response</span></span>

<span data-ttu-id="df7a1-133">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [establecer](../resources/directorysetting.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="df7a1-133">If successful, this method returns a `200 OK` response code and [directorySetting](../resources/directorysetting.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="df7a1-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="df7a1-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="df7a1-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="df7a1-135">Request</span></span>
<span data-ttu-id="df7a1-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="df7a1-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_directorysetting"
}-->
```http
GET https://graph.microsoft.com/beta/settings/{id}
```
##### <a name="response"></a><span data-ttu-id="df7a1-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="df7a1-137">Response</span></span>
<span data-ttu-id="df7a1-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="df7a1-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directorySetting"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 198

{
  "id": "id-value",
  "displayName": "displayName-value",
  "settingTemplateId": "settingTemplateId-value",
  "values": [
    {
      "name": "name-value",
      "value": "value-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get directorySetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->