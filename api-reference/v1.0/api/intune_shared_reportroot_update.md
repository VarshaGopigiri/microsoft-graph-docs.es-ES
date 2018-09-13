# <a name="update-reportroot"></a><span data-ttu-id="6f732-101">Actualizar reportRoot</span><span class="sxs-lookup"><span data-stu-id="6f732-101">Update reportRoot</span></span>

> <span data-ttu-id="6f732-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6f732-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6f732-103">Actualice las propiedades de un objeto [reportRoot](../resources/intune_shared_reportroot.md).</span><span class="sxs-lookup"><span data-stu-id="6f732-103">Update the properties of a [reportRoot](../resources/intune_shared_reportroot.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6f732-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6f732-104">Prerequisites</span></span>
<span data-ttu-id="6f732-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6f732-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6f732-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6f732-107">Permission type</span></span>|<span data-ttu-id="6f732-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6f732-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6f732-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6f732-109">Delegated (work or school account)</span></span>||
| <span data-ttu-id="6f732-110">&nbsp; &nbsp; Configuración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="6f732-110">&nbsp; &nbsp;Device Configuration.</span></span> | <span data-ttu-id="6f732-111">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6f732-111">DeviceManagementConfiguration.ReadWrite.All</span></span>|
| <span data-ttu-id="6f732-112">&nbsp; &nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="6f732-112">&nbsp; &nbsp;Troubleshooting</span></span> | <span data-ttu-id="6f732-113">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6f732-113">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="6f732-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6f732-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6f732-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6f732-115">Not supported.</span></span>|
|<span data-ttu-id="6f732-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6f732-116">Application</span></span>|<span data-ttu-id="6f732-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6f732-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6f732-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6f732-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /reports
```

## <a name="request-headers"></a><span data-ttu-id="6f732-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6f732-119">Request headers</span></span>
|<span data-ttu-id="6f732-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f732-120">Header</span></span>|<span data-ttu-id="6f732-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6f732-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6f732-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="6f732-122">Authorization</span></span>|<span data-ttu-id="6f732-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6f732-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6f732-124">Accept</span><span class="sxs-lookup"><span data-stu-id="6f732-124">Accept</span></span>|<span data-ttu-id="6f732-125">application/json</span><span class="sxs-lookup"><span data-stu-id="6f732-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6f732-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6f732-126">Request body</span></span>
<span data-ttu-id="6f732-127">En el cuerpo de la solicitud, especifique una representación JSON del objeto [reportRoot](../resources/intune_shared_reportroot.md).</span><span class="sxs-lookup"><span data-stu-id="6f732-127">In the request body, supply a JSON representation for the [reportRoot](../resources/intune_shared_reportroot.md) object.</span></span>

<span data-ttu-id="6f732-128">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [reportRoot](../resources/intune_shared_reportroot.md).</span><span class="sxs-lookup"><span data-stu-id="6f732-128">The following table shows the properties that are required when you create the [reportRoot](../resources/intune_shared_reportroot.md).</span></span>

|<span data-ttu-id="6f732-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6f732-129">Property</span></span>|<span data-ttu-id="6f732-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f732-130">Type</span></span>|<span data-ttu-id="6f732-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f732-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6f732-132">id</span><span class="sxs-lookup"><span data-stu-id="6f732-132">id</span></span>|<span data-ttu-id="6f732-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="6f732-133">String</span></span>|<span data-ttu-id="6f732-134">El identificador único de esta entidad.</span><span class="sxs-lookup"><span data-stu-id="6f732-134">The unique identifier for this entity.</span></span>|



## <a name="response"></a><span data-ttu-id="6f732-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f732-135">Response</span></span>
<span data-ttu-id="6f732-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [reportRoot](../resources/intune_shared_reportroot.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6f732-136">If successful, this method returns a `200 OK` response code and an updated [reportRoot](../resources/intune_shared_reportroot.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6f732-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f732-137">Example</span></span>
### <a name="request"></a><span data-ttu-id="6f732-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6f732-138">Request</span></span>
<span data-ttu-id="6f732-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6f732-139">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/reports
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a><span data-ttu-id="6f732-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f732-140">Response</span></span>
<span data-ttu-id="6f732-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6f732-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 101

{
  "@odata.type": "#microsoft.graph.reportRoot",
  "id": "9ab6b3dd-b3dd-9ab6-ddb3-b69addb3b69a"
}
```








