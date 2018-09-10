# <a name="list-iosdevicefeaturesconfigurations"></a><span data-ttu-id="5203f-101">Enumerar iosDeviceFeaturesConfigurations</span><span class="sxs-lookup"><span data-stu-id="5203f-101">List iosDeviceFeaturesConfigurations</span></span>

> <span data-ttu-id="5203f-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5203f-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5203f-103">Enumere las propiedades y las relaciones de los objetos [iosDeviceFeaturesConfiguration](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="5203f-103">List properties and relationships of the [iosDeviceFeaturesConfiguration](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5203f-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5203f-104">Prerequisites</span></span>
<span data-ttu-id="5203f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5203f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5203f-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5203f-107">Permission type</span></span>|<span data-ttu-id="5203f-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5203f-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5203f-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5203f-109">Delegated (work or school account)</span></span>|<span data-ttu-id="5203f-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="5203f-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="5203f-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5203f-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5203f-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5203f-112">Not supported.</span></span>|
|<span data-ttu-id="5203f-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5203f-113">Application</span></span>|<span data-ttu-id="5203f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5203f-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5203f-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5203f-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="5203f-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5203f-116">Request headers</span></span>
|<span data-ttu-id="5203f-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5203f-117">Header</span></span>|<span data-ttu-id="5203f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5203f-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5203f-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="5203f-119">Authorization</span></span>|<span data-ttu-id="5203f-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5203f-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5203f-121">Accept</span><span class="sxs-lookup"><span data-stu-id="5203f-121">Accept</span></span>|<span data-ttu-id="5203f-122">application/json</span><span class="sxs-lookup"><span data-stu-id="5203f-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5203f-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5203f-123">Request body</span></span>
<span data-ttu-id="5203f-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5203f-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5203f-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5203f-125">Response</span></span>
<span data-ttu-id="5203f-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [iosDeviceFeaturesConfiguration](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5203f-126">If successful, this method returns a `200 OK` response code and a collection of [iosDeviceFeaturesConfiguration](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5203f-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5203f-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="5203f-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5203f-128">Request</span></span>
<span data-ttu-id="5203f-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5203f-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="5203f-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5203f-130">Response</span></span>
<span data-ttu-id="5203f-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5203f-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2461

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.iosDeviceFeaturesConfiguration",
      "id": "651e0ab3-0ab3-651e-b30a-1e65b30a1e65",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7,
      "assetTagTemplate": "Asset Tag Template value",
      "lockScreenFootnote": "Lock Screen Footnote value",
      "homeScreenDockIcons": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolder",
          "displayName": "Display Name value",
          "pages": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
              "displayName": "Display Name value",
              "apps": [
                {
                  "@odata.type": "microsoft.graph.iosHomeScreenApp",
                  "displayName": "Display Name value",
                  "bundleID": "Bundle ID value"
                }
              ]
            }
          ]
        }
      ],
      "homeScreenPages": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenPage",
          "displayName": "Display Name value",
          "icons": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenFolder",
              "displayName": "Display Name value",
              "pages": [
                {
                  "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
                  "displayName": "Display Name value",
                  "apps": [
                    {
                      "@odata.type": "microsoft.graph.iosHomeScreenApp",
                      "displayName": "Display Name value",
                      "bundleID": "Bundle ID value"
                    }
                  ]
                }
              ]
            }
          ]
        }
      ],
      "notificationSettings": [
        {
          "@odata.type": "microsoft.graph.iosNotificationSettings",
          "bundleID": "Bundle ID value",
          "appName": "App Name value",
          "publisher": "Publisher value",
          "enabled": true,
          "showInNotificationCenter": true,
          "showOnLockScreen": true,
          "alertType": "banner",
          "badgesEnabled": true,
          "soundsEnabled": true
        }
      ]
    }
  ]
}
```








