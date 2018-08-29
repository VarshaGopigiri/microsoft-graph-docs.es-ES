# <a name="list-mdmwindowsinformationprotectionpolicies"></a><span data-ttu-id="1bbcc-101">Enumerar mdmWindowsInformationProtectionPolicies</span><span class="sxs-lookup"><span data-stu-id="1bbcc-101">List mdmWindowsInformationProtectionPolicies</span></span>

> <span data-ttu-id="1bbcc-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1bbcc-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1bbcc-103">Enumere las propiedades y las relaciones de los objetos [mdmWindowsInformationProtectionPolicy](../resources/intune_mam_mdmwindowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1bbcc-103">List properties and relationships of the [mdmWindowsInformationProtectionPolicy](../resources/intune_mam_mdmwindowsinformationprotectionpolicy.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1bbcc-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1bbcc-104">Prerequisites</span></span>
<span data-ttu-id="1bbcc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1bbcc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="1bbcc-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1bbcc-107">Permission type</span></span>|<span data-ttu-id="1bbcc-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1bbcc-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1bbcc-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1bbcc-109">Delegated (work or school account)</span></span>|<span data-ttu-id="1bbcc-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="1bbcc-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="1bbcc-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1bbcc-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1bbcc-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1bbcc-112">Not supported.</span></span>|
|<span data-ttu-id="1bbcc-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1bbcc-113">Application</span></span>|<span data-ttu-id="1bbcc-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1bbcc-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1bbcc-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1bbcc-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mdmWindowsInformationProtectionPolicies
```

## <a name="request-headers"></a><span data-ttu-id="1bbcc-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1bbcc-116">Request headers</span></span>
|<span data-ttu-id="1bbcc-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1bbcc-117">Header</span></span>|<span data-ttu-id="1bbcc-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1bbcc-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1bbcc-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="1bbcc-119">Authorization</span></span>|<span data-ttu-id="1bbcc-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1bbcc-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1bbcc-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1bbcc-121">Accept</span></span>|<span data-ttu-id="1bbcc-122">application/json</span><span class="sxs-lookup"><span data-stu-id="1bbcc-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1bbcc-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1bbcc-123">Request body</span></span>
<span data-ttu-id="1bbcc-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1bbcc-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1bbcc-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1bbcc-125">Response</span></span>
<span data-ttu-id="1bbcc-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [mdmWindowsInformationProtectionPolicy](../resources/intune_mam_mdmwindowsinformationprotectionpolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1bbcc-126">If successful, this method returns a `200 OK` response code and a collection of [mdmWindowsInformationProtectionPolicy](../resources/intune_mam_mdmwindowsinformationprotectionpolicy.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1bbcc-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1bbcc-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="1bbcc-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1bbcc-128">Request</span></span>
<span data-ttu-id="1bbcc-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1bbcc-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mdmWindowsInformationProtectionPolicies
```

### <a name="response"></a><span data-ttu-id="1bbcc-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1bbcc-130">Response</span></span>
<span data-ttu-id="1bbcc-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1bbcc-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 4607

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
      "rightsManagementServicesTemplateId": "79199ed9-e50b-4257-8de4-70b9c8685061",
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



