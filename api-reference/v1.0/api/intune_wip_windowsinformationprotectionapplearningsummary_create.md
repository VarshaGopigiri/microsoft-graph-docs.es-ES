# <a name="create-windowsinformationprotectionapplearningsummary"></a><span data-ttu-id="8aad4-101">Crear windowsInformationProtectionAppLearningSummary</span><span class="sxs-lookup"><span data-stu-id="8aad4-101">Create windowsInformationProtectionAppLearningSummary</span></span>

> <span data-ttu-id="8aad4-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8aad4-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8aad4-103">Cree un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="8aad4-103">Create a new [plannerBucket](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8aad4-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8aad4-104">Prerequisites</span></span>
<span data-ttu-id="8aad4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8aad4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8aad4-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8aad4-107">Permission type</span></span>|<span data-ttu-id="8aad4-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8aad4-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8aad4-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8aad4-109">Delegated (work or school account)</span></span>|<span data-ttu-id="8aad4-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8aad4-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="8aad4-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8aad4-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8aad4-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8aad4-112">Not supported.</span></span>|
|<span data-ttu-id="8aad4-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8aad4-113">Application</span></span>|<span data-ttu-id="8aad4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8aad4-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8aad4-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8aad4-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/windowsInformationProtectionAppLearningSummaries
```

## <a name="request-headers"></a><span data-ttu-id="8aad4-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8aad4-116">Request headers</span></span>
|<span data-ttu-id="8aad4-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8aad4-117">Header</span></span>|<span data-ttu-id="8aad4-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8aad4-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8aad4-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="8aad4-119">Authorization</span></span>|<span data-ttu-id="8aad4-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8aad4-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="8aad4-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8aad4-121">Accept</span></span>|<span data-ttu-id="8aad4-122">application/json</span><span class="sxs-lookup"><span data-stu-id="8aad4-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8aad4-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8aad4-123">Request body</span></span>
<span data-ttu-id="8aad4-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="8aad4-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="8aad4-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="8aad4-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="8aad4-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8aad4-126">Property</span></span>|<span data-ttu-id="8aad4-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="8aad4-127">Type</span></span>|<span data-ttu-id="8aad4-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="8aad4-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8aad4-129">id</span><span class="sxs-lookup"><span data-stu-id="8aad4-129">id</span></span>|<span data-ttu-id="8aad4-130">String</span><span class="sxs-lookup"><span data-stu-id="8aad4-130">String</span></span>|<span data-ttu-id="8aad4-131">Identificador único para WindowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="8aad4-131">Unique Identifier for the WindowsInformationProtectionAppLearningSummary.</span></span>|
|<span data-ttu-id="8aad4-132">applicationName</span><span class="sxs-lookup"><span data-stu-id="8aad4-132">applicationName</span></span>|<span data-ttu-id="8aad4-133">String</span><span class="sxs-lookup"><span data-stu-id="8aad4-133">String</span></span>|<span data-ttu-id="8aad4-134">Nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="8aad4-134">Application Name</span></span>|
|<span data-ttu-id="8aad4-135">applicationType</span><span class="sxs-lookup"><span data-stu-id="8aad4-135">applicationType</span></span>|<span data-ttu-id="8aad4-136">String</span><span class="sxs-lookup"><span data-stu-id="8aad4-136">String</span></span>|<span data-ttu-id="8aad4-137">Tipo de aplicación Los valores posibles son: `universal` y `desktop`.</span><span class="sxs-lookup"><span data-stu-id="8aad4-137">Application Type Possible values are: `universal`, `desktop`.</span></span>|
|<span data-ttu-id="8aad4-138">deviceCount</span><span class="sxs-lookup"><span data-stu-id="8aad4-138">deviceCount</span></span>|<span data-ttu-id="8aad4-139">Int32</span><span class="sxs-lookup"><span data-stu-id="8aad4-139">Int32</span></span>|<span data-ttu-id="8aad4-140">Recuento de dispositivos</span><span class="sxs-lookup"><span data-stu-id="8aad4-140">Device Count</span></span>|



## <a name="response"></a><span data-ttu-id="8aad4-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8aad4-141">Response</span></span>
<span data-ttu-id="8aad4-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8aad4-142">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8aad4-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8aad4-143">Example</span></span>
### <a name="request"></a><span data-ttu-id="8aad4-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8aad4-144">Request</span></span>
<span data-ttu-id="8aad4-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8aad4-145">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="8aad4-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8aad4-146">Response</span></span>
<span data-ttu-id="8aad4-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8aad4-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



