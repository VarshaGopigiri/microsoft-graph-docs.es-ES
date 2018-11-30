---
title: Enumerar windowsInformationProtections
description: Enumere las propiedades y las relaciones de los objetos windowsInformationProtection.
ms.openlocfilehash: 94c26f1128374a571d1d719659845246213e619f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089487"
---
# <a name="list-windowsinformationprotections"></a><span data-ttu-id="bab28-103">Enumerar windowsInformationProtections</span><span class="sxs-lookup"><span data-stu-id="bab28-103">List windowsInformationProtections</span></span>

> <span data-ttu-id="bab28-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bab28-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bab28-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bab28-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bab28-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bab28-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bab28-107">Enumere las propiedades y las relaciones de los objetos [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="bab28-107">List properties and relationships of the [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bab28-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bab28-108">Prerequisites</span></span>
<span data-ttu-id="bab28-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bab28-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bab28-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bab28-111">Permission type</span></span>|<span data-ttu-id="bab28-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bab28-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bab28-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bab28-113">Delegated (work or school account)</span></span>|<span data-ttu-id="bab28-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="bab28-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="bab28-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bab28-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bab28-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bab28-116">Not supported.</span></span>|
|<span data-ttu-id="bab28-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bab28-117">Application</span></span>|<span data-ttu-id="bab28-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bab28-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bab28-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bab28-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppPolicies
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/appliedPolicies
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/intendedPolicies
```

## <a name="request-headers"></a><span data-ttu-id="bab28-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bab28-120">Request headers</span></span>
|<span data-ttu-id="bab28-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bab28-121">Header</span></span>|<span data-ttu-id="bab28-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bab28-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bab28-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="bab28-123">Authorization</span></span>|<span data-ttu-id="bab28-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bab28-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bab28-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="bab28-125">Accept</span></span>|<span data-ttu-id="bab28-126">application/json</span><span class="sxs-lookup"><span data-stu-id="bab28-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bab28-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bab28-127">Request body</span></span>
<span data-ttu-id="bab28-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bab28-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bab28-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bab28-129">Response</span></span>
<span data-ttu-id="bab28-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bab28-130">If successful, this method returns a `200 OK` response code and a collection of [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bab28-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bab28-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="bab28-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bab28-132">Request</span></span>
<span data-ttu-id="bab28-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bab28-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/managedAppPolicies
```

### <a name="response"></a><span data-ttu-id="bab28-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bab28-134">Response</span></span>
<span data-ttu-id="bab28-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bab28-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 4601

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsInformationProtection",
      "displayName": "Display Name value",
      "description": "Description value",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "id": "ca339419-9419-ca33-1994-33ca199433ca",
      "version": "Version value",
      "enforcementLevel": "encryptAndAuditOnly",
      "enterpriseDomain": "Enterprise Domain value",
      "enterpriseProtectedDomainNames": [
        {
          "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
          "displayName": "Display Name value",
          "resources": [
            "Resources value"
          ]
        }
      ],
      "protectionUnderLockConfigRequired": true,
      "dataRecoveryCertificate": {
        "@odata.type": "microsoft.graph.windowsInformationProtectionDataRecoveryCertificate",
        "subjectName": "Subject Name value",
        "description": "Description value",
        "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
        "certificate": "Y2VydGlmaWNhdGU="
      },
      "revokeOnUnenrollDisabled": true,
      "rightsManagementServicesTemplateId": "abf7b16f-b16f-abf7-6fb1-f7ab6fb1f7ab",
      "azureRightsManagementServicesAllowed": true,
      "iconsVisible": true,
      "protectedApps": [
        {
          "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
          "displayName": "Display Name value",
          "description": "Description value",
          "publisherName": "Publisher Name value",
          "productName": "Product Name value",
          "denied": true
        }
      ],
      "exemptApps": [
        {
          "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
          "displayName": "Display Name value",
          "description": "Description value",
          "publisherName": "Publisher Name value",
          "productName": "Product Name value",
          "denied": true
        }
      ],
      "enterpriseNetworkDomainNames": [
        {
          "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
          "displayName": "Display Name value",
          "resources": [
            "Resources value"
          ]
        }
      ],
      "enterpriseProxiedDomains": [
        {
          "@odata.type": "microsoft.graph.windowsInformationProtectionProxiedDomainCollection",
          "displayName": "Display Name value",
          "proxiedDomains": [
            {
              "@odata.type": "microsoft.graph.proxiedDomain",
              "ipAddressOrFQDN": "Ip Address Or FQDN value",
              "proxy": "Proxy value"
            }
          ]
        }
      ],
      "enterpriseIPRanges": [
        {
          "@odata.type": "microsoft.graph.windowsInformationProtectionIPRangeCollection",
          "displayName": "Display Name value",
          "ranges": [
            {
              "@odata.type": "microsoft.graph.iPv6Range",
              "lowerAddress": "Lower Address value",
              "upperAddress": "Upper Address value"
            }
          ]
        }
      ],
      "enterpriseIPRangesAreAuthoritative": true,
      "enterpriseProxyServers": [
        {
          "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
          "displayName": "Display Name value",
          "resources": [
            "Resources value"
          ]
        }
      ],
      "enterpriseInternalProxyServers": [
        {
          "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
          "displayName": "Display Name value",
          "resources": [
            "Resources value"
          ]
        }
      ],
      "enterpriseProxyServersAreAuthoritative": true,
      "neutralDomainResources": [
        {
          "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
          "displayName": "Display Name value",
          "resources": [
            "Resources value"
          ]
        }
      ],
      "indexingEncryptedStoresOrItemsBlocked": true,
      "smbAutoEncryptedFileExtensions": [
        {
          "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
          "displayName": "Display Name value",
          "resources": [
            "Resources value"
          ]
        }
      ],
      "isAssigned": true
    }
  ]
}
```





