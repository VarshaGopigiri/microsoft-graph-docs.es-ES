# <a name="create-userinstallstatesummary"></a><span data-ttu-id="18245-101">Crear userInstallStateSummary</span><span class="sxs-lookup"><span data-stu-id="18245-101">Create userInstallStateSummary</span></span>

> <span data-ttu-id="18245-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="18245-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="18245-103">Cree un objeto [userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="18245-103">Create a new [plannerBucket](../resources/intune_books_userinstallstatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="18245-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="18245-104">Prerequisites</span></span>
<span data-ttu-id="18245-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="18245-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="18245-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="18245-107">Permission type</span></span>|<span data-ttu-id="18245-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="18245-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="18245-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="18245-109">Delegated (work or school account)</span></span>|<span data-ttu-id="18245-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="18245-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="18245-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="18245-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="18245-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="18245-112">Not supported.</span></span>|
|<span data-ttu-id="18245-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="18245-113">Application</span></span>|<span data-ttu-id="18245-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="18245-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="18245-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="18245-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary
```

## <a name="request-headers"></a><span data-ttu-id="18245-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="18245-116">Request headers</span></span>
|<span data-ttu-id="18245-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18245-117">Header</span></span>|<span data-ttu-id="18245-118">Valor</span><span class="sxs-lookup"><span data-stu-id="18245-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="18245-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="18245-119">Authorization</span></span>|<span data-ttu-id="18245-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="18245-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="18245-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="18245-121">Accept</span></span>|<span data-ttu-id="18245-122">application/json</span><span class="sxs-lookup"><span data-stu-id="18245-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="18245-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="18245-123">Request body</span></span>
<span data-ttu-id="18245-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto userInstallStateSummary.</span><span class="sxs-lookup"><span data-stu-id="18245-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="18245-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto userInstallStateSummary.</span><span class="sxs-lookup"><span data-stu-id="18245-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="18245-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="18245-126">Property</span></span>|<span data-ttu-id="18245-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="18245-127">Type</span></span>|<span data-ttu-id="18245-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="18245-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="18245-129">id</span><span class="sxs-lookup"><span data-stu-id="18245-129">id</span></span>|<span data-ttu-id="18245-130">String</span><span class="sxs-lookup"><span data-stu-id="18245-130">String</span></span>|<span data-ttu-id="18245-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="18245-131">Key of the setting.</span></span>|
|<span data-ttu-id="18245-132">userName</span><span class="sxs-lookup"><span data-stu-id="18245-132">userName</span></span>|<span data-ttu-id="18245-133">String</span><span class="sxs-lookup"><span data-stu-id="18245-133">String</span></span>|<span data-ttu-id="18245-134">Nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="18245-134">User name.</span></span>|
|<span data-ttu-id="18245-135">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="18245-135">installedDeviceCount</span></span>|<span data-ttu-id="18245-136">Int32</span><span class="sxs-lookup"><span data-stu-id="18245-136">Int32</span></span>|<span data-ttu-id="18245-137">Número de dispositivos instalados.</span><span class="sxs-lookup"><span data-stu-id="18245-137">Installed Device Count.</span></span>|
|<span data-ttu-id="18245-138">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="18245-138">failedDeviceCount</span></span>|<span data-ttu-id="18245-139">Int32</span><span class="sxs-lookup"><span data-stu-id="18245-139">Int32</span></span>|<span data-ttu-id="18245-140">Número de dispositivos erróneos.</span><span class="sxs-lookup"><span data-stu-id="18245-140">Failed Device Count.</span></span>|
|<span data-ttu-id="18245-141">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="18245-141">notInstalledDeviceCount</span></span>|<span data-ttu-id="18245-142">Int32</span><span class="sxs-lookup"><span data-stu-id="18245-142">Int32</span></span>|<span data-ttu-id="18245-143">Número de dispositivos no instalados.</span><span class="sxs-lookup"><span data-stu-id="18245-143">Not installed device count.</span></span>|



## <a name="response"></a><span data-ttu-id="18245-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18245-144">Response</span></span>
<span data-ttu-id="18245-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18245-145">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_books_userinstallstatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="18245-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="18245-146">Example</span></span>
### <a name="request"></a><span data-ttu-id="18245-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="18245-147">Request</span></span>
<span data-ttu-id="18245-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="18245-148">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary
Content-type: application/json
Content-length: 189

{
  "@odata.type": "#microsoft.graph.userInstallStateSummary",
  "userName": "User Name value",
  "installedDeviceCount": 4,
  "failedDeviceCount": 1,
  "notInstalledDeviceCount": 7
}
```

### <a name="response"></a><span data-ttu-id="18245-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18245-149">Response</span></span>
<span data-ttu-id="18245-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="18245-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 238

{
  "@odata.type": "#microsoft.graph.userInstallStateSummary",
  "id": "1e5b41ba-41ba-1e5b-ba41-5b1eba415b1e",
  "userName": "User Name value",
  "installedDeviceCount": 4,
  "failedDeviceCount": 1,
  "notInstalledDeviceCount": 7
}
```



