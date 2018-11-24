# <a name="list-androidworkprofilegeneraldeviceconfigurations"></a><span data-ttu-id="d7a58-101">Lista androidWorkProfileGeneralDeviceConfigurations</span><span class="sxs-lookup"><span data-stu-id="d7a58-101">List androidWorkProfileGeneralDeviceConfigurations</span></span>

> <span data-ttu-id="d7a58-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d7a58-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d7a58-103">Propiedades de la lista y relaciones de los objetos [androidWorkProfileGeneralDeviceConfiguration](../resources/intune_deviceconfig_androidworkprofilegeneraldeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="d7a58-103">List properties and relationships of the [androidWorkProfileGeneralDeviceConfiguration](../resources/intune_deviceconfig_androidworkprofilegeneraldeviceconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d7a58-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d7a58-104">Prerequisites</span></span>
<span data-ttu-id="d7a58-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d7a58-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d7a58-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d7a58-107">Permission type</span></span>|<span data-ttu-id="d7a58-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d7a58-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d7a58-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d7a58-109">Delegated (work or school account)</span></span>|<span data-ttu-id="d7a58-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="d7a58-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="d7a58-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d7a58-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d7a58-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d7a58-112">Not supported.</span></span>|
|<span data-ttu-id="d7a58-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d7a58-113">Application</span></span>|<span data-ttu-id="d7a58-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d7a58-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d7a58-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d7a58-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="d7a58-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d7a58-116">Request headers</span></span>
|<span data-ttu-id="d7a58-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7a58-117">Header</span></span>|<span data-ttu-id="d7a58-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d7a58-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d7a58-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="d7a58-119">Authorization</span></span>|<span data-ttu-id="d7a58-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d7a58-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d7a58-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d7a58-121">Accept</span></span>|<span data-ttu-id="d7a58-122">application/json</span><span class="sxs-lookup"><span data-stu-id="d7a58-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d7a58-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d7a58-123">Request body</span></span>
<span data-ttu-id="d7a58-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d7a58-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d7a58-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7a58-125">Response</span></span>
<span data-ttu-id="d7a58-126">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [androidWorkProfileGeneralDeviceConfiguration](../resources/intune_deviceconfig_androidworkprofilegeneraldeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d7a58-126">If successful, this method returns a `200 OK` response code and a collection of [androidWorkProfileGeneralDeviceConfiguration](../resources/intune_deviceconfig_androidworkprofilegeneraldeviceconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d7a58-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d7a58-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="d7a58-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d7a58-128">Request</span></span>
<span data-ttu-id="d7a58-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d7a58-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="d7a58-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7a58-130">Response</span></span>
<span data-ttu-id="d7a58-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d7a58-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2200

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidWorkProfileGeneralDeviceConfiguration",
      "id": "6decda7e-da7e-6dec-7eda-ec6d7edaec6d",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7,
      "passwordBlockFingerprintUnlock": true,
      "passwordBlockTrustAgents": true,
      "passwordExpirationDays": 6,
      "passwordMinimumLength": 5,
      "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
      "passwordPreviousPasswordBlockCount": 2,
      "passwordSignInFailureCountBeforeFactoryReset": 12,
      "passwordRequiredType": "lowSecurityBiometric",
      "workProfileDataSharingType": "preventAny",
      "workProfileBlockNotificationsWhileDeviceLocked": true,
      "workProfileBlockAddingAccounts": true,
      "workProfileBluetoothEnableContactSharing": true,
      "workProfileBlockScreenCapture": true,
      "workProfileBlockCrossProfileCallerId": true,
      "workProfileBlockCamera": true,
      "workProfileBlockCrossProfileContactsSearch": true,
      "workProfileBlockCrossProfileCopyPaste": true,
      "workProfileDefaultAppPermissionPolicy": "prompt",
      "workProfilePasswordBlockFingerprintUnlock": true,
      "workProfilePasswordBlockTrustAgents": true,
      "workProfilePasswordExpirationDays": 1,
      "workProfilePasswordMinimumLength": 0,
      "workProfilePasswordMinNumericCharacters": 7,
      "workProfilePasswordMinNonLetterCharacters": 9,
      "workProfilePasswordMinLetterCharacters": 6,
      "workProfilePasswordMinLowerCaseCharacters": 9,
      "workProfilePasswordMinUpperCaseCharacters": 9,
      "workProfilePasswordMinSymbolCharacters": 6,
      "workProfilePasswordMinutesOfInactivityBeforeScreenTimeout": 9,
      "workProfilePasswordPreviousPasswordBlockCount": 13,
      "workProfilePasswordSignInFailureCountBeforeFactoryReset": 7,
      "workProfilePasswordRequiredType": "lowSecurityBiometric",
      "workProfileRequirePassword": true,
      "securityRequireVerifyApps": true
    }
  ]
}
```



