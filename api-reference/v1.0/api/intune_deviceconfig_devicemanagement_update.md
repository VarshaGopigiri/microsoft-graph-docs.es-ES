# <a name="update-devicemanagement"></a><span data-ttu-id="55a44-101">Actualizar deviceManagement</span><span class="sxs-lookup"><span data-stu-id="55a44-101">Update deviceManagement</span></span>

> <span data-ttu-id="55a44-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="55a44-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="55a44-103">Actualice las propiedades de un objeto [deviceManagement](../resources/intune_deviceconfig_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="55a44-103">Update the properties of a [calendar](../resources/intune_deviceconfig_devicemanagement.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="55a44-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="55a44-104">Prerequisites</span></span>
<span data-ttu-id="55a44-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="55a44-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="55a44-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="55a44-107">Permission type</span></span>|<span data-ttu-id="55a44-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="55a44-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="55a44-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="55a44-109">Delegated (work or school account)</span></span>|<span data-ttu-id="55a44-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="55a44-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="55a44-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="55a44-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="55a44-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="55a44-112">Not supported.</span></span>|
|<span data-ttu-id="55a44-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="55a44-113">Application</span></span>|<span data-ttu-id="55a44-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="55a44-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="55a44-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="55a44-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement
```

## <a name="request-headers"></a><span data-ttu-id="55a44-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="55a44-116">Request headers</span></span>
|<span data-ttu-id="55a44-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55a44-117">Header</span></span>|<span data-ttu-id="55a44-118">Valor</span><span class="sxs-lookup"><span data-stu-id="55a44-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="55a44-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="55a44-119">Authorization</span></span>|<span data-ttu-id="55a44-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="55a44-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="55a44-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="55a44-121">Accept</span></span>|<span data-ttu-id="55a44-122">application/json</span><span class="sxs-lookup"><span data-stu-id="55a44-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="55a44-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="55a44-123">Request body</span></span>
<span data-ttu-id="55a44-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceManagement](../resources/intune_deviceconfig_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="55a44-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_deviceconfig_devicemanagement.md) object.</span></span>

<span data-ttu-id="55a44-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceManagement](../resources/intune_deviceconfig_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="55a44-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="55a44-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="55a44-126">Property</span></span>|<span data-ttu-id="55a44-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="55a44-127">Type</span></span>|<span data-ttu-id="55a44-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="55a44-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="55a44-129">id</span><span class="sxs-lookup"><span data-stu-id="55a44-129">id</span></span>|<span data-ttu-id="55a44-130">String</span><span class="sxs-lookup"><span data-stu-id="55a44-130">String</span></span>|<span data-ttu-id="55a44-131">Identificador único</span><span class="sxs-lookup"><span data-stu-id="55a44-131">Unique Identifier</span></span>|
|<span data-ttu-id="55a44-132">configuración</span><span class="sxs-lookup"><span data-stu-id="55a44-132">settings</span></span>|[<span data-ttu-id="55a44-133">deviceManagementSettings</span><span class="sxs-lookup"><span data-stu-id="55a44-133">deviceManagementSettings</span></span>](../resources/intune_deviceconfig_devicemanagementsettings.md)|<span data-ttu-id="55a44-134">Configuración de niveles de cuenta.</span><span class="sxs-lookup"><span data-stu-id="55a44-134">Account level settings.</span></span>|



## <a name="response"></a><span data-ttu-id="55a44-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55a44-135">Response</span></span>
<span data-ttu-id="55a44-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceManagement](../resources/intune_deviceconfig_devicemanagement.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="55a44-136">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_deviceconfig_devicemanagement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="55a44-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="55a44-137">Example</span></span>
### <a name="request"></a><span data-ttu-id="55a44-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="55a44-138">Request</span></span>
<span data-ttu-id="55a44-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="55a44-139">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement
Content-type: application/json
Content-length: 206

{
  "settings": {
    "@odata.type": "microsoft.graph.deviceManagementSettings",
    "deviceComplianceCheckinThresholdDays": 4,
    "isScheduledActionEnabled": true,
    "secureByDefault": true
  }
}
```

### <a name="response"></a><span data-ttu-id="55a44-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55a44-140">Response</span></span>
<span data-ttu-id="55a44-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="55a44-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 310

{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "0b283420-3420-0b28-2034-280b2034280b",
  "settings": {
    "@odata.type": "microsoft.graph.deviceManagementSettings",
    "deviceComplianceCheckinThresholdDays": 4,
    "isScheduledActionEnabled": true,
    "secureByDefault": true
  }
}
```



