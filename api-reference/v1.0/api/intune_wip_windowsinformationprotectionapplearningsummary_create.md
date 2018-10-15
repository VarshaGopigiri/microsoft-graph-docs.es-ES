# <a name="create-windowsinformationprotectionapplearningsummary"></a><span data-ttu-id="01ded-101">Crear windowsInformationProtectionAppLearningSummary</span><span class="sxs-lookup"><span data-stu-id="01ded-101">Create windowsInformationProtectionAppLearningSummary</span></span>

> <span data-ttu-id="01ded-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="01ded-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="01ded-103">Cree un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="01ded-103">Create a new [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="01ded-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="01ded-104">Prerequisites</span></span>
<span data-ttu-id="01ded-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="01ded-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="01ded-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="01ded-107">Permission type</span></span>|<span data-ttu-id="01ded-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="01ded-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="01ded-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="01ded-109">Delegated (work or school account)</span></span>|<span data-ttu-id="01ded-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="01ded-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="01ded-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="01ded-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="01ded-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01ded-112">Not supported.</span></span>|
|<span data-ttu-id="01ded-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="01ded-113">Application</span></span>|<span data-ttu-id="01ded-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01ded-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="01ded-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="01ded-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/windowsInformationProtectionAppLearningSummaries
```

## <a name="request-headers"></a><span data-ttu-id="01ded-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="01ded-116">Request headers</span></span>
|<span data-ttu-id="01ded-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01ded-117">Header</span></span>|<span data-ttu-id="01ded-118">Valor</span><span class="sxs-lookup"><span data-stu-id="01ded-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="01ded-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="01ded-119">Authorization</span></span>|<span data-ttu-id="01ded-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="01ded-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="01ded-121">Accept</span><span class="sxs-lookup"><span data-stu-id="01ded-121">Accept</span></span>|<span data-ttu-id="01ded-122">application/json</span><span class="sxs-lookup"><span data-stu-id="01ded-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="01ded-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="01ded-123">Request body</span></span>
<span data-ttu-id="01ded-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="01ded-124">In the request body, supply a JSON representation for the windowsInformationProtectionAppLearningSummary object.</span></span>

<span data-ttu-id="01ded-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="01ded-125">The following table shows the properties that are required when you create the windowsInformationProtectionAppLearningSummary.</span></span>

|<span data-ttu-id="01ded-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="01ded-126">Property</span></span>|<span data-ttu-id="01ded-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="01ded-127">Type</span></span>|<span data-ttu-id="01ded-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="01ded-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="01ded-129">id</span><span class="sxs-lookup"><span data-stu-id="01ded-129">id</span></span>|<span data-ttu-id="01ded-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="01ded-130">String</span></span>|<span data-ttu-id="01ded-131">Identificador único para WindowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="01ded-131">Unique Identifier for the WindowsInformationProtectionAppLearningSummary.</span></span>|
|<span data-ttu-id="01ded-132">applicationName</span><span class="sxs-lookup"><span data-stu-id="01ded-132">applicationName</span></span>|<span data-ttu-id="01ded-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="01ded-133">String</span></span>|<span data-ttu-id="01ded-134">Nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="01ded-134">Application Name</span></span>|
|<span data-ttu-id="01ded-135">applicationType</span><span class="sxs-lookup"><span data-stu-id="01ded-135">applicationType</span></span>|[<span data-ttu-id="01ded-136">applicationType</span><span class="sxs-lookup"><span data-stu-id="01ded-136">applicationType</span></span>](../resources/intune_wip_applicationtype.md)|<span data-ttu-id="01ded-p102">Tipo de aplicación. Los valores posibles son: `universal` y `desktop`.</span><span class="sxs-lookup"><span data-stu-id="01ded-p102">Application Type Possible values are: `universal`, `desktop`.</span></span>|
|<span data-ttu-id="01ded-139">deviceCount</span><span class="sxs-lookup"><span data-stu-id="01ded-139">deviceCount</span></span>|<span data-ttu-id="01ded-140">Int32</span><span class="sxs-lookup"><span data-stu-id="01ded-140">Int32</span></span>|<span data-ttu-id="01ded-141">Recuento de dispositivos</span><span class="sxs-lookup"><span data-stu-id="01ded-141">Device Count</span></span>|



## <a name="response"></a><span data-ttu-id="01ded-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01ded-142">Response</span></span>
<span data-ttu-id="01ded-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01ded-143">If successful, this method returns a `201 Created` response code and a [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="01ded-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="01ded-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="01ded-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="01ded-145">Request</span></span>
<span data-ttu-id="01ded-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="01ded-146">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/windowsInformationProtectionAppLearningSummaries
Content-type: application/json
Content-length: 191

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLearningSummary",
  "applicationName": "Application Name value",
  "applicationType": "desktop",
  "deviceCount": 11
}
```

### <a name="response"></a><span data-ttu-id="01ded-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01ded-147">Response</span></span>
<span data-ttu-id="01ded-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="01ded-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 240

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLearningSummary",
  "id": "063baf50-af50-063b-50af-3b0650af3b06",
  "applicationName": "Application Name value",
  "applicationType": "desktop",
  "deviceCount": 11
}
```








