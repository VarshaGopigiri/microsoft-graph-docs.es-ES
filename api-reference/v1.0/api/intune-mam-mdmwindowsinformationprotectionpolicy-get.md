---
title: Obtener mdmWindowsInformationProtectionPolicy
description: Lea las propiedades y las relaciones del objeto mdmWindowsInformationProtectionPolicy.
ms.openlocfilehash: 35920b9c88016e7fc37a0e71b183994a1c668049
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029397"
---
# <a name="get-mdmwindowsinformationprotectionpolicy"></a><span data-ttu-id="c7b2f-103">Obtener mdmWindowsInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c7b2f-103">Get mdmWindowsInformationProtectionPolicy</span></span>

> <span data-ttu-id="c7b2f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c7b2f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c7b2f-105">Lea las propiedades y las relaciones del objeto [mdmWindowsInformationProtectionPolicy](../resources/intune-mam-mdmwindowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c7b2f-105">Read properties and relationships of the [mdmWindowsInformationProtectionPolicy](../resources/intune-mam-mdmwindowsinformationprotectionpolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c7b2f-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c7b2f-106">Prerequisites</span></span>
<span data-ttu-id="c7b2f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c7b2f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c7b2f-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c7b2f-109">Permission type</span></span>|<span data-ttu-id="c7b2f-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c7b2f-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c7b2f-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c7b2f-111">Delegated (work or school account)</span></span>|<span data-ttu-id="c7b2f-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="c7b2f-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="c7b2f-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c7b2f-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c7b2f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c7b2f-114">Not supported.</span></span>|
|<span data-ttu-id="c7b2f-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c7b2f-115">Application</span></span>|<span data-ttu-id="c7b2f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c7b2f-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c7b2f-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c7b2f-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mdmWindowsInformationProtectionPolicies/{mdmWindowsInformationProtectionPolicyId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="c7b2f-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c7b2f-118">Optional query parameters</span></span>
<span data-ttu-id="c7b2f-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7b2f-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="c7b2f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c7b2f-120">Request headers</span></span>
|<span data-ttu-id="c7b2f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7b2f-121">Header</span></span>|<span data-ttu-id="c7b2f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c7b2f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c7b2f-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="c7b2f-123">Authorization</span></span>|<span data-ttu-id="c7b2f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c7b2f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c7b2f-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c7b2f-125">Accept</span></span>|<span data-ttu-id="c7b2f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="c7b2f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c7b2f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c7b2f-127">Request body</span></span>
<span data-ttu-id="c7b2f-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c7b2f-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c7b2f-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7b2f-129">Response</span></span>
<span data-ttu-id="c7b2f-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [mdmWindowsInformationProtectionPolicy](../resources/intune-mam-mdmwindowsinformationprotectionpolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7b2f-130">If successful, this method returns a `200 OK` response code and [mdmWindowsInformationProtectionPolicy](../resources/intune-mam-mdmwindowsinformationprotectionpolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c7b2f-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7b2f-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="c7b2f-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c7b2f-132">Request</span></span>
<span data-ttu-id="c7b2f-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c7b2f-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mdmWindowsInformationProtectionPolicies/{mdmWindowsInformationProtectionPolicyId}
```

### <a name="response"></a><span data-ttu-id="c7b2f-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7b2f-134">Response</span></span>
<span data-ttu-id="c7b2f-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c7b2f-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 4346

{
  "value": {
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
}
```


