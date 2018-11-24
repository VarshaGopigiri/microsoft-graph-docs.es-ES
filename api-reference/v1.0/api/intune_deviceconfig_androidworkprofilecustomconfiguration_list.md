# <a name="list-androidworkprofilecustomconfigurations"></a><span data-ttu-id="4cab4-101">Lista androidWorkProfileCustomConfigurations</span><span class="sxs-lookup"><span data-stu-id="4cab4-101">List androidWorkProfileCustomConfigurations</span></span>

> <span data-ttu-id="4cab4-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4cab4-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4cab4-103">Propiedades de la lista y relaciones de los objetos [androidWorkProfileCustomConfiguration](../resources/intune_deviceconfig_androidworkprofilecustomconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="4cab4-103">List properties and relationships of the [androidWorkProfileCustomConfiguration](../resources/intune_deviceconfig_androidworkprofilecustomconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4cab4-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4cab4-104">Prerequisites</span></span>
<span data-ttu-id="4cab4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4cab4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="4cab4-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4cab4-107">Permission type</span></span>|<span data-ttu-id="4cab4-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4cab4-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4cab4-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4cab4-109">Delegated (work or school account)</span></span>|<span data-ttu-id="4cab4-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="4cab4-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="4cab4-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4cab4-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4cab4-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4cab4-112">Not supported.</span></span>|
|<span data-ttu-id="4cab4-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4cab4-113">Application</span></span>|<span data-ttu-id="4cab4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4cab4-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4cab4-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4cab4-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="4cab4-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4cab4-116">Request headers</span></span>
|<span data-ttu-id="4cab4-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4cab4-117">Header</span></span>|<span data-ttu-id="4cab4-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4cab4-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4cab4-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="4cab4-119">Authorization</span></span>|<span data-ttu-id="4cab4-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4cab4-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4cab4-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4cab4-121">Accept</span></span>|<span data-ttu-id="4cab4-122">application/json</span><span class="sxs-lookup"><span data-stu-id="4cab4-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4cab4-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4cab4-123">Request body</span></span>
<span data-ttu-id="4cab4-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4cab4-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4cab4-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4cab4-125">Response</span></span>
<span data-ttu-id="4cab4-126">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [androidWorkProfileCustomConfiguration](../resources/intune_deviceconfig_androidworkprofilecustomconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4cab4-126">If successful, this method returns a `200 OK` response code and a collection of [androidWorkProfileCustomConfiguration](../resources/intune_deviceconfig_androidworkprofilecustomconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4cab4-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4cab4-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="4cab4-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4cab4-128">Request</span></span>
<span data-ttu-id="4cab4-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4cab4-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="4cab4-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4cab4-130">Response</span></span>
<span data-ttu-id="4cab4-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4cab4-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 682

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidWorkProfileCustomConfiguration",
      "id": "76c5d59b-d59b-76c5-9bd5-c5769bd5c576",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7,
      "omaSettings": [
        {
          "@odata.type": "microsoft.graph.omaSettingInteger",
          "displayName": "Display Name value",
          "description": "Description value",
          "omaUri": "Oma Uri value",
          "value": 5
        }
      ]
    }
  ]
}
```



