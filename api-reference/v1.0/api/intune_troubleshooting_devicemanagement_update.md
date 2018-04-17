# <a name="update-devicemanagement"></a><span data-ttu-id="215a2-101">Actualizar deviceManagement</span><span class="sxs-lookup"><span data-stu-id="215a2-101">Update deviceManagement</span></span>

> <span data-ttu-id="215a2-102">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="215a2-102">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="215a2-103">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="215a2-103">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="215a2-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="215a2-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="215a2-105">Actualice las propiedades de un objeto [deviceManagement](../resources/intune_troubleshooting_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="215a2-105">Update the properties of a [deviceManagement](../resources/intune_troubleshooting_devicemanagement.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="215a2-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="215a2-106">Prerequisites</span></span>
<span data-ttu-id="215a2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="215a2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="215a2-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="215a2-109">Permission type</span></span>|<span data-ttu-id="215a2-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="215a2-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="215a2-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="215a2-111">Delegated (work or school account)</span></span>|<span data-ttu-id="215a2-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="215a2-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="215a2-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="215a2-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="215a2-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="215a2-114">Not supported.</span></span>|
|<span data-ttu-id="215a2-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="215a2-115">Application</span></span>|<span data-ttu-id="215a2-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="215a2-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="215a2-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="215a2-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement
```

## <a name="request-headers"></a><span data-ttu-id="215a2-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="215a2-118">Request headers</span></span>
|<span data-ttu-id="215a2-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="215a2-119">Header</span></span>|<span data-ttu-id="215a2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="215a2-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="215a2-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="215a2-121">Authorization</span></span>|<span data-ttu-id="215a2-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="215a2-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="215a2-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="215a2-123">Accept</span></span>|<span data-ttu-id="215a2-124">application/json</span><span class="sxs-lookup"><span data-stu-id="215a2-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="215a2-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="215a2-125">Request body</span></span>
<span data-ttu-id="215a2-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceManagement](../resources/intune_troubleshooting_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="215a2-126">In the request body, supply a JSON representation for the [deviceManagement](../resources/intune_troubleshooting_devicemanagement.md) object.</span></span>

<span data-ttu-id="215a2-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceManagement](../resources/intune_troubleshooting_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="215a2-127">The following table shows the properties that are required when you create the [deviceManagement](../resources/intune_troubleshooting_devicemanagement.md).</span></span>

|<span data-ttu-id="215a2-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="215a2-128">Property</span></span>|<span data-ttu-id="215a2-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="215a2-129">Type</span></span>|<span data-ttu-id="215a2-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="215a2-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="215a2-131">id</span><span class="sxs-lookup"><span data-stu-id="215a2-131">id</span></span>|<span data-ttu-id="215a2-132">String</span><span class="sxs-lookup"><span data-stu-id="215a2-132">String</span></span>|<span data-ttu-id="215a2-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="215a2-133">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="215a2-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="215a2-134">Response</span></span>
<span data-ttu-id="215a2-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceManagement](../resources/intune_troubleshooting_devicemanagement.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="215a2-135">If successful, this method returns a `200 OK` response code and an updated [deviceManagement](../resources/intune_troubleshooting_devicemanagement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="215a2-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="215a2-136">Example</span></span>
### <a name="request"></a><span data-ttu-id="215a2-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="215a2-137">Request</span></span>
<span data-ttu-id="215a2-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="215a2-138">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a><span data-ttu-id="215a2-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="215a2-139">Response</span></span>
<span data-ttu-id="215a2-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="215a2-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 107

{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "0b283420-3420-0b28-2034-280b2034280b"
}
```



