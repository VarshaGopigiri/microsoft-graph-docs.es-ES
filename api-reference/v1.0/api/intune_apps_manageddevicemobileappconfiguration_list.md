# <a name="list-manageddevicemobileappconfigurations"></a><span data-ttu-id="56d79-101">Enumerar managedDeviceMobileAppConfigurations</span><span class="sxs-lookup"><span data-stu-id="56d79-101">List managedDeviceMobileAppConfigurations</span></span>

> <span data-ttu-id="56d79-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="56d79-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="56d79-103">Enumere las propiedades y las relaciones de los objetos [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="56d79-103">List properties and relationships of the [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="56d79-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="56d79-104">Prerequisites</span></span>
<span data-ttu-id="56d79-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="56d79-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="56d79-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="56d79-107">Permission type</span></span>|<span data-ttu-id="56d79-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="56d79-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="56d79-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="56d79-109">Delegated (work or school account)</span></span>|<span data-ttu-id="56d79-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="56d79-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="56d79-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="56d79-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="56d79-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="56d79-112">Not supported.</span></span>|
|<span data-ttu-id="56d79-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="56d79-113">Application</span></span>|<span data-ttu-id="56d79-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="56d79-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="56d79-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="56d79-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileAppConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="56d79-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="56d79-116">Request headers</span></span>
|<span data-ttu-id="56d79-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56d79-117">Header</span></span>|<span data-ttu-id="56d79-118">Valor</span><span class="sxs-lookup"><span data-stu-id="56d79-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="56d79-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="56d79-119">Authorization</span></span>|<span data-ttu-id="56d79-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="56d79-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="56d79-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="56d79-121">Accept</span></span>|<span data-ttu-id="56d79-122">application/json</span><span class="sxs-lookup"><span data-stu-id="56d79-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="56d79-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="56d79-123">Request body</span></span>
<span data-ttu-id="56d79-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="56d79-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="56d79-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56d79-125">Response</span></span>
<span data-ttu-id="56d79-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="56d79-126">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/intune_apps_manageddevicemobileappconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="56d79-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="56d79-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="56d79-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="56d79-128">Request</span></span>
<span data-ttu-id="56d79-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="56d79-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppConfigurations
```

### <a name="response"></a><span data-ttu-id="56d79-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56d79-130">Response</span></span>
<span data-ttu-id="56d79-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="56d79-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 485

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfiguration",
      "id": "c60e7591-7591-c60e-9175-0ec691750ec6",
      "targetedMobileApps": [
        "Targeted Mobile Apps value"
      ],
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "displayName": "Display Name value",
      "version": 7
    }
  ]
}
```



