# <a name="create-windowsinformationprotectionnetworklearningsummary"></a><span data-ttu-id="f6a9e-101">Crear windowsInformationProtectionNetworkLearningSummary</span><span class="sxs-lookup"><span data-stu-id="f6a9e-101">Create windowsInformationProtectionNetworkLearningSummary</span></span>

> <span data-ttu-id="f6a9e-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f6a9e-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f6a9e-103">Cree un objeto [windowsInformationProtectionNetworkLearningSummary](../resources/intune_wip_windowsinformationprotectionnetworklearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="f6a9e-103">Create a new [windowsInformationProtectionNetworkLearningSummary](../resources/intune_wip_windowsinformationprotectionnetworklearningsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f6a9e-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f6a9e-104">Prerequisites</span></span>
<span data-ttu-id="f6a9e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f6a9e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f6a9e-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f6a9e-107">Permission type</span></span>|<span data-ttu-id="f6a9e-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f6a9e-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f6a9e-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f6a9e-109">Delegated (work or school account)</span></span>|<span data-ttu-id="f6a9e-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f6a9e-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f6a9e-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f6a9e-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f6a9e-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f6a9e-112">Not supported.</span></span>|
|<span data-ttu-id="f6a9e-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f6a9e-113">Application</span></span>|<span data-ttu-id="f6a9e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f6a9e-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f6a9e-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f6a9e-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/windowsInformationProtectionNetworkLearningSummaries
```

## <a name="request-headers"></a><span data-ttu-id="f6a9e-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f6a9e-116">Request headers</span></span>
|<span data-ttu-id="f6a9e-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6a9e-117">Header</span></span>|<span data-ttu-id="f6a9e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f6a9e-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f6a9e-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="f6a9e-119">Authorization</span></span>|<span data-ttu-id="f6a9e-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f6a9e-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f6a9e-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f6a9e-121">Accept</span></span>|<span data-ttu-id="f6a9e-122">application/json</span><span class="sxs-lookup"><span data-stu-id="f6a9e-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f6a9e-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f6a9e-123">Request body</span></span>
<span data-ttu-id="f6a9e-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsInformationProtectionNetworkLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="f6a9e-124">In the request body, supply a JSON representation for the windowsInformationProtectionNetworkLearningSummary object.</span></span>

<span data-ttu-id="f6a9e-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsInformationProtectionNetworkLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="f6a9e-125">The following table shows the properties that are required when you create the windowsInformationProtectionNetworkLearningSummary.</span></span>

|<span data-ttu-id="f6a9e-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f6a9e-126">Property</span></span>|<span data-ttu-id="f6a9e-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6a9e-127">Type</span></span>|<span data-ttu-id="f6a9e-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6a9e-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f6a9e-129">id</span><span class="sxs-lookup"><span data-stu-id="f6a9e-129">id</span></span>|<span data-ttu-id="f6a9e-130">String</span><span class="sxs-lookup"><span data-stu-id="f6a9e-130">String</span></span>|<span data-ttu-id="f6a9e-131">Identificador único para WindowsInformationProtectionNetworkLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="f6a9e-131">Unique Identifier for the WindowsInformationProtectionNetworkLearningSummary.</span></span>|
|<span data-ttu-id="f6a9e-132">url</span><span class="sxs-lookup"><span data-stu-id="f6a9e-132">url</span></span>|<span data-ttu-id="f6a9e-133">String</span><span class="sxs-lookup"><span data-stu-id="f6a9e-133">String</span></span>|<span data-ttu-id="f6a9e-134">Dirección URL del sitio web</span><span class="sxs-lookup"><span data-stu-id="f6a9e-134">Website url</span></span>|
|<span data-ttu-id="f6a9e-135">deviceCount</span><span class="sxs-lookup"><span data-stu-id="f6a9e-135">deviceCount</span></span>|<span data-ttu-id="f6a9e-136">Int32</span><span class="sxs-lookup"><span data-stu-id="f6a9e-136">Int32</span></span>|<span data-ttu-id="f6a9e-137">Recuento de dispositivos</span><span class="sxs-lookup"><span data-stu-id="f6a9e-137">Device Count</span></span>|



## <a name="response"></a><span data-ttu-id="f6a9e-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6a9e-138">Response</span></span>
<span data-ttu-id="f6a9e-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsInformationProtectionNetworkLearningSummary](../resources/intune_wip_windowsinformationprotectionnetworklearningsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f6a9e-139">If successful, this method returns a `201 Created` response code and a [windowsInformationProtectionNetworkLearningSummary](../resources/intune_wip_windowsinformationprotectionnetworklearningsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f6a9e-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f6a9e-140">Example</span></span>
### <a name="request"></a><span data-ttu-id="f6a9e-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f6a9e-141">Request</span></span>
<span data-ttu-id="f6a9e-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f6a9e-142">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/windowsInformationProtectionNetworkLearningSummaries
Content-type: application/json
Content-length: 137

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionNetworkLearningSummary",
  "url": "Url value",
  "deviceCount": 11
}
```

### <a name="response"></a><span data-ttu-id="f6a9e-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6a9e-143">Response</span></span>
<span data-ttu-id="f6a9e-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f6a9e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 186

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionNetworkLearningSummary",
  "id": "242108f7-08f7-2421-f708-2124f7082124",
  "url": "Url value",
  "deviceCount": 11
}
```



