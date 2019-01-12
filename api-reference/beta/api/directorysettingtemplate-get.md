---
title: Obtener una plantilla de configuración de Active directory
description: Una plantilla de configuración de Active directory representa una plantilla de configuración desde la que puede crearse la configuración dentro de un inquilino. Esta operación permite recuperar de las propiedades del objeto directorySettingTemplate, incluida la configuración disponible y sus valores predeterminados.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 2fb9f8edbc374760f16496bd9ec5bcf666a09883
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27935678"
---
# <a name="get-a-directory-setting-template"></a><span data-ttu-id="05ac2-104">Obtener una plantilla de configuración de Active directory</span><span class="sxs-lookup"><span data-stu-id="05ac2-104">Get a directory setting template</span></span>

> <span data-ttu-id="05ac2-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="05ac2-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="05ac2-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="05ac2-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="05ac2-107">Una plantilla de configuración de Active directory representa una plantilla de configuración desde la que puede crearse la configuración dentro de un inquilino.</span><span class="sxs-lookup"><span data-stu-id="05ac2-107">A directory setting template represents a template of settings from which settings may be created within a tenant.</span></span> <span data-ttu-id="05ac2-108">Esta operación permite recuperar de las propiedades del objeto directorySettingTemplate, incluida la configuración disponible y sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="05ac2-108">This operation allows retrieval of the properties of the directorySettingTemplate object, including the available settings and their defaults.</span></span>

> <span data-ttu-id="05ac2-109">**Nota**: la versión de /beta de esta API es sólo se aplica a los grupos.</span><span class="sxs-lookup"><span data-stu-id="05ac2-109">**Note**: The /beta version of this API is only applies to groups.</span></span> <span data-ttu-id="05ac2-110">Se ha cambiado la versión /v1.0 de esta API para *obtener groupSettingTemplate*.</span><span class="sxs-lookup"><span data-stu-id="05ac2-110">The /v1.0 version of this API has been renamed to *Get groupSettingTemplate*.</span></span>

## <a name="permissions"></a><span data-ttu-id="05ac2-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="05ac2-111">Permissions</span></span>
<span data-ttu-id="05ac2-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="05ac2-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="05ac2-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="05ac2-114">Permission type</span></span>      | <span data-ttu-id="05ac2-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="05ac2-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="05ac2-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="05ac2-116">Delegated (work or school account)</span></span> | <span data-ttu-id="05ac2-117">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="05ac2-117">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="05ac2-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="05ac2-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="05ac2-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="05ac2-119">Not supported.</span></span>    |
|<span data-ttu-id="05ac2-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="05ac2-120">Application</span></span> | <span data-ttu-id="05ac2-121">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="05ac2-121">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="05ac2-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="05ac2-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directorySettingTemplates/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="05ac2-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="05ac2-123">Optional query parameters</span></span>
<span data-ttu-id="05ac2-124">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="05ac2-124">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="05ac2-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="05ac2-125">Request headers</span></span>
| <span data-ttu-id="05ac2-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="05ac2-126">Name</span></span>      |<span data-ttu-id="05ac2-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="05ac2-127">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="05ac2-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="05ac2-128">Authorization</span></span>  | <span data-ttu-id="05ac2-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="05ac2-p106">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="05ac2-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="05ac2-131">Request body</span></span>
<span data-ttu-id="05ac2-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="05ac2-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="05ac2-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05ac2-133">Response</span></span>

<span data-ttu-id="05ac2-134">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [directorySettingTemplate](../resources/directorysettingtemplate.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="05ac2-134">If successful, this method returns a `200 OK` response code and [directorySettingTemplate](../resources/directorysettingtemplate.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="05ac2-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="05ac2-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="05ac2-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="05ac2-136">Request</span></span>
<span data-ttu-id="05ac2-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="05ac2-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_directorysettingtemplate"
}-->
```http
GET https://graph.microsoft.com/beta/directorySettingTemplates/{id}
```
##### <a name="response"></a><span data-ttu-id="05ac2-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05ac2-138">Response</span></span>
<span data-ttu-id="05ac2-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="05ac2-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directorySettingTemplate"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 270

{
  "id": "id-value",
  "displayName": "displayName-value",
  "description": "description-value",
  "values": [
    {
      "name": "name-value",
      "type": "type-value",
      "defaultValue": "defaultValue-value",
      "description": "description-value"
    }
  ],
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get directorySettingTemplate",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
