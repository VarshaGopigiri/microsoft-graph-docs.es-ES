# <a name="create-windowsinformationprotectionapplockerfile"></a><span data-ttu-id="270dd-101">Crear windowsInformationProtectionAppLockerFile</span><span class="sxs-lookup"><span data-stu-id="270dd-101">Create windowsInformationProtectionAppLockerFile</span></span>

> <span data-ttu-id="270dd-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="270dd-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="270dd-103">Cree un objeto [windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md).</span><span class="sxs-lookup"><span data-stu-id="270dd-103">Create a new [windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="270dd-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="270dd-104">Prerequisites</span></span>
<span data-ttu-id="270dd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="270dd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="270dd-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="270dd-107">Permission type</span></span>|<span data-ttu-id="270dd-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="270dd-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="270dd-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="270dd-109">Delegated (work or school account)</span></span>|<span data-ttu-id="270dd-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="270dd-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="270dd-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="270dd-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="270dd-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="270dd-112">Not supported.</span></span>|
|<span data-ttu-id="270dd-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="270dd-113">Application</span></span>|<span data-ttu-id="270dd-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="270dd-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="270dd-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="270dd-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}/exemptAppLockerFiles
POST /deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}/protectedAppLockerFiles
POST /deviceAppManagement/mdmWindowsInformationProtectionPolicies/{mdmWindowsInformationProtectionPolicyId}/exemptAppLockerFiles
POST /deviceAppManagement/mdmWindowsInformationProtectionPolicies/{mdmWindowsInformationProtectionPolicyId}/protectedAppLockerFiles
```

## <a name="request-headers"></a><span data-ttu-id="270dd-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="270dd-116">Request headers</span></span>
|<span data-ttu-id="270dd-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="270dd-117">Header</span></span>|<span data-ttu-id="270dd-118">Valor</span><span class="sxs-lookup"><span data-stu-id="270dd-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="270dd-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="270dd-119">Authorization</span></span>|<span data-ttu-id="270dd-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="270dd-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="270dd-121">Accept</span><span class="sxs-lookup"><span data-stu-id="270dd-121">Accept</span></span>|<span data-ttu-id="270dd-122">application/json</span><span class="sxs-lookup"><span data-stu-id="270dd-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="270dd-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="270dd-123">Request body</span></span>
<span data-ttu-id="270dd-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsInformationProtectionAppLockerFile.</span><span class="sxs-lookup"><span data-stu-id="270dd-124">In the request body, supply a JSON representation for the windowsInformationProtectionAppLockerFile object.</span></span>

<span data-ttu-id="270dd-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsInformationProtectionAppLockerFile.</span><span class="sxs-lookup"><span data-stu-id="270dd-125">The following table shows the properties that are required when you create the windowsInformationProtectionAppLockerFile.</span></span>

|<span data-ttu-id="270dd-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="270dd-126">Property</span></span>|<span data-ttu-id="270dd-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="270dd-127">Type</span></span>|<span data-ttu-id="270dd-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="270dd-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="270dd-129">displayName</span><span class="sxs-lookup"><span data-stu-id="270dd-129">displayName</span></span>|<span data-ttu-id="270dd-130">String</span><span class="sxs-lookup"><span data-stu-id="270dd-130">String</span></span>|<span data-ttu-id="270dd-131">El nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="270dd-131">The friendly name</span></span>|
|<span data-ttu-id="270dd-132">fileHash</span><span class="sxs-lookup"><span data-stu-id="270dd-132">fileHash</span></span>|<span data-ttu-id="270dd-133">String</span><span class="sxs-lookup"><span data-stu-id="270dd-133">String</span></span>|<span data-ttu-id="270dd-134">Hash del archivo SHA256</span><span class="sxs-lookup"><span data-stu-id="270dd-134">SHA256 hash of the file</span></span>|
|<span data-ttu-id="270dd-135">file</span><span class="sxs-lookup"><span data-stu-id="270dd-135">file</span></span>|<span data-ttu-id="270dd-136">Binario</span><span class="sxs-lookup"><span data-stu-id="270dd-136">Binary</span></span>|<span data-ttu-id="270dd-137">Archivo como una matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="270dd-137">File as a byte array</span></span>|
|<span data-ttu-id="270dd-138">id</span><span class="sxs-lookup"><span data-stu-id="270dd-138">id</span></span>|<span data-ttu-id="270dd-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="270dd-139">String</span></span>|<span data-ttu-id="270dd-140">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="270dd-140">Key of the entity.</span></span>|
|<span data-ttu-id="270dd-141">version</span><span class="sxs-lookup"><span data-stu-id="270dd-141">version</span></span>|<span data-ttu-id="270dd-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="270dd-142">String</span></span>|<span data-ttu-id="270dd-143">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="270dd-143">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="270dd-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="270dd-144">Response</span></span>
<span data-ttu-id="270dd-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="270dd-145">If successful, this method returns a `201 Created` response code and a [windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="270dd-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="270dd-146">Example</span></span>
### <a name="request"></a><span data-ttu-id="270dd-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="270dd-147">Request</span></span>
<span data-ttu-id="270dd-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="270dd-148">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}/exemptAppLockerFiles
Content-type: application/json
Content-length: 211

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLockerFile",
  "displayName": "Display Name value",
  "fileHash": "File Hash value",
  "file": "ZmlsZQ==",
  "version": "Version value"
}
```

### <a name="response"></a><span data-ttu-id="270dd-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="270dd-149">Response</span></span>
<span data-ttu-id="270dd-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="270dd-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 260

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLockerFile",
  "displayName": "Display Name value",
  "fileHash": "File Hash value",
  "file": "ZmlsZQ==",
  "id": "d81f0e40-0e40-d81f-400e-1fd8400e1fd8",
  "version": "Version value"
}
```








