---
title: Configuración de Active directory de la lista
description: Recuperar una lista de los objetos de configuración de Active directory.
ms.openlocfilehash: 844d2102b9bfd98e2ba0a585a7eb04c8e46b6a52
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084289"
---
# <a name="list-directory-settings"></a><span data-ttu-id="5f96e-103">Configuración de Active directory de la lista</span><span class="sxs-lookup"><span data-stu-id="5f96e-103">List directory settings</span></span>

> <span data-ttu-id="5f96e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5f96e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5f96e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5f96e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5f96e-106">Recuperar una lista de los objetos de configuración de Active directory.</span><span class="sxs-lookup"><span data-stu-id="5f96e-106">Retrieve a list of directory setting objects.</span></span>

> <span data-ttu-id="5f96e-107">**Nota**: la versión de /beta de esta API es sólo se aplica a los grupos.</span><span class="sxs-lookup"><span data-stu-id="5f96e-107">**Note**: The /beta version of this API is only applies to groups.</span></span> <span data-ttu-id="5f96e-108">La versión /v1.0 de esta API se ha cambiado a *groupSettings de lista*.</span><span class="sxs-lookup"><span data-stu-id="5f96e-108">The /v1.0 version of this API has been renamed to *List groupSettings*.</span></span>

## <a name="permissions"></a><span data-ttu-id="5f96e-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="5f96e-109">Permissions</span></span>
<span data-ttu-id="5f96e-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5f96e-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5f96e-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5f96e-112">Permission type</span></span>      | <span data-ttu-id="5f96e-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5f96e-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5f96e-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5f96e-114">Delegated (work or school account)</span></span> | <span data-ttu-id="5f96e-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="5f96e-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="5f96e-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5f96e-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5f96e-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5f96e-117">Not supported.</span></span>    |
|<span data-ttu-id="5f96e-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5f96e-118">Application</span></span> | <span data-ttu-id="5f96e-119">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5f96e-119">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="5f96e-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5f96e-120">HTTP request</span></span>
<span data-ttu-id="5f96e-121"><!-- { "blockType": "ignored" } -->Todo el inquilino de lista o configuración de grupo</span><span class="sxs-lookup"><span data-stu-id="5f96e-121"><!-- { "blockType": "ignored" } --> List tenant-wide or group settings</span></span>
```http
GET /settings
GET /group/{id}/settings
```
## <a name="optional-query-parameters"></a><span data-ttu-id="5f96e-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="5f96e-122">Optional query parameters</span></span>
<span data-ttu-id="5f96e-123">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f96e-123">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="5f96e-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5f96e-124">Request headers</span></span>
| <span data-ttu-id="5f96e-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="5f96e-125">Name</span></span>      |<span data-ttu-id="5f96e-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f96e-126">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="5f96e-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="5f96e-127">Authorization</span></span>  | <span data-ttu-id="5f96e-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5f96e-p104">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="5f96e-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5f96e-130">Request body</span></span>
<span data-ttu-id="5f96e-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5f96e-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5f96e-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f96e-132">Response</span></span>

<span data-ttu-id="5f96e-133">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [establecer](../resources/directorysetting.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f96e-133">If successful, this method returns a `200 OK` response code and collection of [directorySetting](../resources/directorysetting.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="5f96e-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5f96e-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5f96e-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5f96e-135">Request</span></span>
<span data-ttu-id="5f96e-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5f96e-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_settings"
}-->
```http
GET https://graph.microsoft.com/beta/settings
```
##### <a name="response"></a><span data-ttu-id="5f96e-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f96e-137">Response</span></span>
<span data-ttu-id="5f96e-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5f96e-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directorySetting",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 263

{
  "value": [
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
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List settings",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
