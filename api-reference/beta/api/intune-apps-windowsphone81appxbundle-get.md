---
title: Obtener windowsPhone81AppXBundle
description: Leer las propiedades y las relaciones del objeto windowsPhone81AppXBundle.
author: tfitzmac
ms.openlocfilehash: a48b58201952f9d6115ee496e29355ab9015f21c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27358117"
---
# <a name="get-windowsphone81appxbundle"></a><span data-ttu-id="0644d-103">Obtener windowsPhone81AppXBundle</span><span class="sxs-lookup"><span data-stu-id="0644d-103">Get windowsPhone81AppXBundle</span></span>

> <span data-ttu-id="0644d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0644d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0644d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0644d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0644d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0644d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0644d-107">Leer las propiedades y las relaciones del objeto [windowsPhone81AppXBundle](../resources/intune-apps-windowsphone81appxbundle.md) .</span><span class="sxs-lookup"><span data-stu-id="0644d-107">Read properties and relationships of the [windowsPhone81AppXBundle](../resources/intune-apps-windowsphone81appxbundle.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0644d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0644d-108">Prerequisites</span></span>
<span data-ttu-id="0644d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0644d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0644d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0644d-111">Permission type</span></span>|<span data-ttu-id="0644d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0644d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0644d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0644d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="0644d-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="0644d-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="0644d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0644d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0644d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0644d-116">Not supported.</span></span>|
|<span data-ttu-id="0644d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0644d-117">Application</span></span>|<span data-ttu-id="0644d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0644d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0644d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0644d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/{mobileAppId}
GET /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
GET /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="optional-query-parameters"></a><span data-ttu-id="0644d-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="0644d-120">Optional query parameters</span></span>
<span data-ttu-id="0644d-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0644d-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="0644d-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0644d-122">Request headers</span></span>
|<span data-ttu-id="0644d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0644d-123">Header</span></span>|<span data-ttu-id="0644d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0644d-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0644d-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="0644d-125">Authorization</span></span>|<span data-ttu-id="0644d-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0644d-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0644d-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0644d-127">Accept</span></span>|<span data-ttu-id="0644d-128">application/json</span><span class="sxs-lookup"><span data-stu-id="0644d-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0644d-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0644d-129">Request body</span></span>
<span data-ttu-id="0644d-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0644d-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0644d-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0644d-131">Response</span></span>
<span data-ttu-id="0644d-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [windowsPhone81AppXBundle](../resources/intune-apps-windowsphone81appxbundle.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0644d-132">If successful, this method returns a `200 OK` response code and [windowsPhone81AppXBundle](../resources/intune-apps-windowsphone81appxbundle.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0644d-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0644d-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="0644d-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0644d-134">Request</span></span>
<span data-ttu-id="0644d-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0644d-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
```

### <a name="response"></a><span data-ttu-id="0644d-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0644d-136">Response</span></span>
<span data-ttu-id="0644d-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0644d-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2412

{
  "value": {
    "@odata.type": "#microsoft.graph.windowsPhone81AppXBundle",
    "id": "2433be7c-be7c-2433-7cbe-33247cbe3324",
    "displayName": "Display Name value",
    "description": "Description value",
    "publisher": "Publisher value",
    "largeIcon": {
      "@odata.type": "microsoft.graph.mimeContent",
      "type": "Type value",
      "value": "dmFsdWU="
    },
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "isFeatured": true,
    "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
    "informationUrl": "https://example.com/informationUrl/",
    "owner": "Owner value",
    "developer": "Developer value",
    "notes": "Notes value",
    "uploadState": 11,
    "publishingState": "processing",
    "committedContentVersion": "Committed Content Version value",
    "fileName": "File Name value",
    "size": 4,
    "applicableArchitectures": "x86",
    "identityName": "Identity Name value",
    "identityPublisherHash": "Identity Publisher Hash value",
    "identityResourceIdentifier": "Identity Resource Identifier value",
    "minimumSupportedOperatingSystem": {
      "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
      "v8_0": true,
      "v8_1": true,
      "v10_0": true,
      "v10_1607": true,
      "v10_1703": true,
      "v10_1709": true,
      "v10_1803": true
    },
    "phoneProductIdentifier": "Phone Product Identifier value",
    "phonePublisherId": "Phone Publisher Id value",
    "identityVersion": "Identity Version value",
    "appXPackageInformationList": [
      {
        "@odata.type": "microsoft.graph.windowsPackageInformation",
        "applicableArchitecture": "x86",
        "displayName": "Display Name value",
        "identityName": "Identity Name value",
        "identityPublisher": "Identity Publisher value",
        "identityResourceIdentifier": "Identity Resource Identifier value",
        "identityVersion": "Identity Version value",
        "minimumSupportedOperatingSystem": {
          "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
          "v8_0": true,
          "v8_1": true,
          "v10_0": true,
          "v10_1607": true,
          "v10_1703": true,
          "v10_1709": true,
          "v10_1803": true
        }
      }
    ]
  }
}
```





