---
title: Lista directorySettingTemplates
description: Configuración de las plantillas del directorio representa un conjunto de plantillas de configuración de Active directory, desde el directorio de configuración puede crearse y se usa dentro un inquilino.  Esta operación recupera la lista de objetos de directorySettingTemplates disponible.
ms.openlocfilehash: 964e2cfc9e06b6a996f63c92cae830e03c953cd8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087710"
---
# <a name="list-directorysettingtemplates"></a><span data-ttu-id="4f4e1-104">Lista directorySettingTemplates</span><span class="sxs-lookup"><span data-stu-id="4f4e1-104">List directorySettingTemplates</span></span>

> <span data-ttu-id="4f4e1-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4f4e1-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4f4e1-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4f4e1-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4f4e1-107">Configuración de las plantillas del directorio representa un conjunto de plantillas de configuración de Active directory, desde el directorio de configuración puede crearse y se usa dentro un inquilino.</span><span class="sxs-lookup"><span data-stu-id="4f4e1-107">Directory setting templates represents a set of templates of directory settings, from which directory settings may be created and used within a tenant.</span></span>  <span data-ttu-id="4f4e1-108">Esta operación recupera la lista de objetos de directorySettingTemplates disponible.</span><span class="sxs-lookup"><span data-stu-id="4f4e1-108">This operation retrieves the list of available directorySettingTemplates objects.</span></span>

> <span data-ttu-id="4f4e1-109">**Nota**: la versión de /beta de esta API es sólo se aplica a los grupos.</span><span class="sxs-lookup"><span data-stu-id="4f4e1-109">**Note**: The /beta version of this API is only applies to groups.</span></span> <span data-ttu-id="4f4e1-110">La versión /v1.0 de esta API ha cambiado de nombre a la *lista groupSettingTemplate*.</span><span class="sxs-lookup"><span data-stu-id="4f4e1-110">The /v1.0 version of this API has been renamed to *List groupSettingTemplate*.</span></span>

## <a name="permissions"></a><span data-ttu-id="4f4e1-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="4f4e1-111">Permissions</span></span>
<span data-ttu-id="4f4e1-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4f4e1-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4f4e1-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4f4e1-114">Permission type</span></span>      | <span data-ttu-id="4f4e1-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4f4e1-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4f4e1-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4f4e1-116">Delegated (work or school account)</span></span> | <span data-ttu-id="4f4e1-117">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="4f4e1-117">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="4f4e1-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4f4e1-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4f4e1-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4f4e1-119">Not supported.</span></span>    |
|<span data-ttu-id="4f4e1-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4f4e1-120">Application</span></span> | <span data-ttu-id="4f4e1-121">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4f4e1-121">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4f4e1-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4f4e1-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directorySettingTemplates
```
## <a name="optional-query-parameters"></a><span data-ttu-id="4f4e1-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="4f4e1-123">Optional query parameters</span></span>
<span data-ttu-id="4f4e1-124">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4f4e1-124">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="4f4e1-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4f4e1-125">Request headers</span></span>
| <span data-ttu-id="4f4e1-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="4f4e1-126">Name</span></span>      |<span data-ttu-id="4f4e1-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f4e1-127">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="4f4e1-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="4f4e1-128">Authorization</span></span>  | <span data-ttu-id="4f4e1-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4f4e1-p106">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="4f4e1-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4f4e1-131">Request body</span></span>
<span data-ttu-id="4f4e1-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4f4e1-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4f4e1-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4f4e1-133">Response</span></span>

<span data-ttu-id="4f4e1-134">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [directorySettingTemplate](../resources/directorysettingtemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4f4e1-134">If successful, this method returns a `200 OK` response code and collection of [directorySettingTemplate](../resources/directorysettingtemplate.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="4f4e1-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4f4e1-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4f4e1-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4f4e1-136">Request</span></span>
<span data-ttu-id="4f4e1-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4f4e1-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_directorysettingtemplates"
}-->
```http
GET https://graph.microsoft.com/beta/directorySettingTemplates
```
##### <a name="response"></a><span data-ttu-id="4f4e1-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4f4e1-138">Response</span></span>
<span data-ttu-id="4f4e1-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4f4e1-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directorySettingTemplate",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 343

{
  "value": [
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
      ]
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List directorySettingTemplates",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->