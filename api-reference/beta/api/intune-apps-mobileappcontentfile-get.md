---
title: Obtener mobileAppContentFile
description: Lea las propiedades y las relaciones del objeto mobileAppContentFile.
ms.openlocfilehash: b34b92f48dca7fb70bcd7e40f6b81d7a10d187de
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088098"
---
# <a name="get-mobileappcontentfile"></a><span data-ttu-id="3cb75-103">Obtener mobileAppContentFile</span><span class="sxs-lookup"><span data-stu-id="3cb75-103">Get mobileAppContentFile</span></span>

> <span data-ttu-id="3cb75-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3cb75-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3cb75-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3cb75-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3cb75-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3cb75-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3cb75-107">Lea las propiedades y las relaciones del objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).</span><span class="sxs-lookup"><span data-stu-id="3cb75-107">Read properties and relationships of the [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3cb75-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3cb75-108">Prerequisites</span></span>
<span data-ttu-id="3cb75-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3cb75-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3cb75-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3cb75-111">Permission type</span></span>|<span data-ttu-id="3cb75-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3cb75-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3cb75-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3cb75-113">Delegated (work or school account)</span></span>|<span data-ttu-id="3cb75-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="3cb75-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="3cb75-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3cb75-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3cb75-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3cb75-116">Not supported.</span></span>|
|<span data-ttu-id="3cb75-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3cb75-117">Application</span></span>|<span data-ttu-id="3cb75-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3cb75-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3cb75-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3cb75-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files/{mobileAppContentFileId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="3cb75-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3cb75-120">Optional query parameters</span></span>
<span data-ttu-id="3cb75-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3cb75-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="3cb75-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3cb75-122">Request headers</span></span>
|<span data-ttu-id="3cb75-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3cb75-123">Header</span></span>|<span data-ttu-id="3cb75-124">Valor</span><span class="sxs-lookup"><span data-stu-id="3cb75-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3cb75-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="3cb75-125">Authorization</span></span>|<span data-ttu-id="3cb75-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3cb75-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3cb75-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3cb75-127">Accept</span></span>|<span data-ttu-id="3cb75-128">application/json</span><span class="sxs-lookup"><span data-stu-id="3cb75-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3cb75-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3cb75-129">Request body</span></span>
<span data-ttu-id="3cb75-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3cb75-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3cb75-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3cb75-131">Response</span></span>
<span data-ttu-id="3cb75-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3cb75-132">If successful, this method returns a `200 OK` response code and [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3cb75-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3cb75-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="3cb75-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3cb75-134">Request</span></span>
<span data-ttu-id="3cb75-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3cb75-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files/{mobileAppContentFileId}
```

### <a name="response"></a><span data-ttu-id="3cb75-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3cb75-136">Response</span></span>
<span data-ttu-id="3cb75-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3cb75-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 548

{
  "value": {
    "@odata.type": "#microsoft.graph.mobileAppContentFile",
    "azureStorageUri": "Azure Storage Uri value",
    "isCommitted": true,
    "id": "eab2e29b-e29b-eab2-9be2-b2ea9be2b2ea",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "name": "Name value",
    "size": 4,
    "sizeEncrypted": 13,
    "azureStorageUriExpirationDateTime": "2017-01-01T00:00:08.4940464-08:00",
    "manifest": "bWFuaWZlc3Q=",
    "uploadState": "transientError",
    "isFrameworkFile": true,
    "isDependency": true
  }
}
```




