---
title: Enumerar windowsInformationProtectionPolicies
description: Enumere las propiedades y las relaciones de los objetos windowsInformationProtectionPolicy.
ms.openlocfilehash: bc2532712611148d4c2ec897dc0aabc7ccca6eb3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030037"
---
# <a name="list-windowsinformationprotectionpolicies"></a><span data-ttu-id="6d5c4-103">Enumerar windowsInformationProtectionPolicies</span><span class="sxs-lookup"><span data-stu-id="6d5c4-103">List windowsInformationProtectionPolicies</span></span>

> <span data-ttu-id="6d5c4-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6d5c4-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6d5c4-105">Enumere las propiedades y las relaciones de los objetos [windowsInformationProtectionPolicy](../resources/intune-mam-windowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="6d5c4-105">List properties and relationships of the [windowsInformationProtectionPolicy](../resources/intune-mam-windowsinformationprotectionpolicy.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6d5c4-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6d5c4-106">Prerequisites</span></span>
<span data-ttu-id="6d5c4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6d5c4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6d5c4-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6d5c4-109">Permission type</span></span>|<span data-ttu-id="6d5c4-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6d5c4-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6d5c4-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6d5c4-111">Delegated (work or school account)</span></span>|<span data-ttu-id="6d5c4-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="6d5c4-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="6d5c4-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6d5c4-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6d5c4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6d5c4-114">Not supported.</span></span>|
|<span data-ttu-id="6d5c4-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6d5c4-115">Application</span></span>|<span data-ttu-id="6d5c4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6d5c4-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6d5c4-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6d5c4-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/windowsInformationProtectionPolicies
```

## <a name="request-headers"></a><span data-ttu-id="6d5c4-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6d5c4-118">Request headers</span></span>
|<span data-ttu-id="6d5c4-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d5c4-119">Header</span></span>|<span data-ttu-id="6d5c4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6d5c4-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6d5c4-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="6d5c4-121">Authorization</span></span>|<span data-ttu-id="6d5c4-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6d5c4-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6d5c4-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6d5c4-123">Accept</span></span>|<span data-ttu-id="6d5c4-124">application/json</span><span class="sxs-lookup"><span data-stu-id="6d5c4-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6d5c4-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6d5c4-125">Request body</span></span>
<span data-ttu-id="6d5c4-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6d5c4-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6d5c4-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d5c4-127">Response</span></span>
<span data-ttu-id="6d5c4-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windowsInformationProtectionPolicy](../resources/intune-mam-windowsinformationprotectionpolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d5c4-128">If successful, this method returns a `200 OK` response code and a collection of [windowsInformationProtectionPolicy](../resources/intune-mam-windowsinformationprotectionpolicy.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6d5c4-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6d5c4-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="6d5c4-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6d5c4-130">Request</span></span>
<span data-ttu-id="6d5c4-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6d5c4-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/windowsInformationProtectionPolicies
```

### <a name="response"></a><span data-ttu-id="6d5c4-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d5c4-132">Response</span></span>
<span data-ttu-id="6d5c4-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6d5c4-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 5158

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsInformationProtectionPolicy",
      "displayName": "Display Name value",
      "description": "Description value",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "id": "6397be61-be61-6397-61be-976361be9763",
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
      "isAssigned": true,
      "revokeOnMdmHandoffDisabled": true,
      "mdmEnrollmentUrl": "https://example.com/mdmEnrollmentUrl/",
      "windowsHelloForBusinessBlocked": true,
      "pinMinimumLength": 0,
      "pinUppercaseLetters": "requireAtLeastOne",
      "pinLowercaseLetters": "requireAtLeastOne",
      "pinSpecialCharacters": "requireAtLeastOne",
      "pinExpirationDays": 1,
      "numberOfPastPinsRemembered": 10,
      "passwordMaximumAttemptCount": 11,
      "minutesOfInactivityBeforeDeviceLock": 3,
      "daysWithoutContactBeforeUnenroll": 0
    }
  ]
}
```



