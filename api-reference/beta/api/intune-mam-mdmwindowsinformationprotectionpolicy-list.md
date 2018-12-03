---
title: Enumerar mdmWindowsInformationProtectionPolicies
description: Enumere las propiedades y las relaciones de los objetos mdmWindowsInformationProtectionPolicy.
ms.openlocfilehash: 0709b2d1ed2466cbcf222d5c0ede808e0c5c8c97
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087201"
---
# <a name="list-mdmwindowsinformationprotectionpolicies"></a><span data-ttu-id="50a79-103">Enumerar mdmWindowsInformationProtectionPolicies</span><span class="sxs-lookup"><span data-stu-id="50a79-103">List mdmWindowsInformationProtectionPolicies</span></span>

> <span data-ttu-id="50a79-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="50a79-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="50a79-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="50a79-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="50a79-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="50a79-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="50a79-107">Enumere las propiedades y las relaciones de los objetos [mdmWindowsInformationProtectionPolicy](../resources/intune-mam-mdmwindowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="50a79-107">List properties and relationships of the [mdmWindowsInformationProtectionPolicy](../resources/intune-mam-mdmwindowsinformationprotectionpolicy.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="50a79-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="50a79-108">Prerequisites</span></span>
<span data-ttu-id="50a79-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="50a79-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="50a79-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="50a79-111">Permission type</span></span>|<span data-ttu-id="50a79-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="50a79-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="50a79-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="50a79-113">Delegated (work or school account)</span></span>|<span data-ttu-id="50a79-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="50a79-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="50a79-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="50a79-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="50a79-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="50a79-116">Not supported.</span></span>|
|<span data-ttu-id="50a79-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="50a79-117">Application</span></span>|<span data-ttu-id="50a79-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="50a79-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="50a79-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="50a79-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mdmWindowsInformationProtectionPolicies
```

## <a name="request-headers"></a><span data-ttu-id="50a79-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="50a79-120">Request headers</span></span>
|<span data-ttu-id="50a79-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50a79-121">Header</span></span>|<span data-ttu-id="50a79-122">Valor</span><span class="sxs-lookup"><span data-stu-id="50a79-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="50a79-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="50a79-123">Authorization</span></span>|<span data-ttu-id="50a79-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="50a79-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="50a79-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="50a79-125">Accept</span></span>|<span data-ttu-id="50a79-126">application/json</span><span class="sxs-lookup"><span data-stu-id="50a79-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="50a79-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="50a79-127">Request body</span></span>
<span data-ttu-id="50a79-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="50a79-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="50a79-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="50a79-129">Response</span></span>
<span data-ttu-id="50a79-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [mdmWindowsInformationProtectionPolicy](../resources/intune-mam-mdmwindowsinformationprotectionpolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="50a79-130">If successful, this method returns a `200 OK` response code and a collection of [mdmWindowsInformationProtectionPolicy](../resources/intune-mam-mdmwindowsinformationprotectionpolicy.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="50a79-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="50a79-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="50a79-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="50a79-132">Request</span></span>
<span data-ttu-id="50a79-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="50a79-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mdmWindowsInformationProtectionPolicies
```

### <a name="response"></a><span data-ttu-id="50a79-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="50a79-134">Response</span></span>
<span data-ttu-id="50a79-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="50a79-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 4610

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.mdmWindowsInformationProtectionPolicy",
      "displayName": "Display Name value",
      "description": "Description value",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "id": "8efb0c35-0c35-8efb-350c-fb8e350cfb8e",
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




