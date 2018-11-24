# <a name="list-targetedmanagedappprotections"></a><span data-ttu-id="d50d9-101">Enumerar targetedManagedAppProtections</span><span class="sxs-lookup"><span data-stu-id="d50d9-101">List targetedManagedAppProtections</span></span>

> <span data-ttu-id="d50d9-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d50d9-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d50d9-103">Enumere las propiedades y los relaciones de los objetos [targetedManagedAppProtection](../resources/intune_mam_targetedmanagedappprotection.md).</span><span class="sxs-lookup"><span data-stu-id="d50d9-103">List properties and relationships of the [targetedManagedAppProtection](../resources/intune_mam_targetedmanagedappprotection.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d50d9-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d50d9-104">Prerequisites</span></span>
<span data-ttu-id="d50d9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d50d9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d50d9-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d50d9-107">Permission type</span></span>|<span data-ttu-id="d50d9-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d50d9-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d50d9-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d50d9-109">Delegated (work or school account)</span></span>|<span data-ttu-id="d50d9-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="d50d9-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="d50d9-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d50d9-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d50d9-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d50d9-112">Not supported.</span></span>|
|<span data-ttu-id="d50d9-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d50d9-113">Application</span></span>|<span data-ttu-id="d50d9-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d50d9-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d50d9-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d50d9-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppPolicies
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/appliedPolicies
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/intendedPolicies
```

## <a name="request-headers"></a><span data-ttu-id="d50d9-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d50d9-116">Request headers</span></span>
|<span data-ttu-id="d50d9-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d50d9-117">Header</span></span>|<span data-ttu-id="d50d9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d50d9-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d50d9-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="d50d9-119">Authorization</span></span>|<span data-ttu-id="d50d9-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d50d9-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d50d9-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d50d9-121">Accept</span></span>|<span data-ttu-id="d50d9-122">application/json</span><span class="sxs-lookup"><span data-stu-id="d50d9-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d50d9-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d50d9-123">Request body</span></span>
<span data-ttu-id="d50d9-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d50d9-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d50d9-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d50d9-125">Response</span></span>
<span data-ttu-id="d50d9-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [targetedManagedAppProtection](../resources/intune_mam_targetedmanagedappprotection.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d50d9-126">If successful, this method returns a `200 OK` response code and a collection of [targetedManagedAppProtection](../resources/intune_mam_targetedmanagedappprotection.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d50d9-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d50d9-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="d50d9-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d50d9-128">Request</span></span>
<span data-ttu-id="d50d9-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d50d9-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppPolicies
```

### <a name="response"></a><span data-ttu-id="d50d9-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d50d9-130">Response</span></span>
<span data-ttu-id="d50d9-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d50d9-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1750

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.targetedManagedAppProtection",
      "displayName": "Display Name value",
      "description": "Description value",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "id": "b6b92266-2266-b6b9-6622-b9b66622b9b6",
      "version": "Version value",
      "periodOfflineBeforeAccessCheck": "-PT17.1357909S",
      "periodOnlineBeforeAccessCheck": "PT35.0018757S",
      "allowedInboundDataTransferSources": "managedApps",
      "allowedOutboundDataTransferDestinations": "managedApps",
      "organizationalCredentialsRequired": true,
      "allowedOutboundClipboardSharingLevel": "managedAppsWithPasteIn",
      "dataBackupBlocked": true,
      "deviceComplianceRequired": true,
      "managedBrowserToOpenLinksRequired": true,
      "saveAsBlocked": true,
      "periodOfflineBeforeWipeIsEnforced": "-PT3M22.1587532S",
      "pinRequired": true,
      "maximumPinRetries": 1,
      "simplePinBlocked": true,
      "minimumPinLength": 0,
      "pinCharacterSet": "alphanumericAndSymbol",
      "periodBeforePinReset": "PT3M29.6631862S",
      "allowedDataStorageLocations": [
        "sharePoint"
      ],
      "contactSyncBlocked": true,
      "printBlocked": true,
      "fingerprintBlocked": true,
      "disableAppPinIfDevicePinIsSet": true,
      "minimumRequiredOsVersion": "Minimum Required Os Version value",
      "minimumWarningOsVersion": "Minimum Warning Os Version value",
      "minimumRequiredAppVersion": "Minimum Required App Version value",
      "minimumWarningAppVersion": "Minimum Warning App Version value",
      "isAssigned": true
    }
  ]
}
```



