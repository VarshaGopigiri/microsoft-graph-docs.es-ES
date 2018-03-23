# <a name="update-devicemanagement"></a><span data-ttu-id="0d435-101">Actualizar deviceManagement</span><span class="sxs-lookup"><span data-stu-id="0d435-101">Update deviceManagement</span></span>

> <span data-ttu-id="0d435-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0d435-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0d435-103">Actualice las propiedades de un objeto [deviceManagement](../resources/intune_wip_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="0d435-103">Update the properties of a [calendar](../resources/intune_wip_devicemanagement.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0d435-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0d435-104">Prerequisites</span></span>
<span data-ttu-id="0d435-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0d435-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="0d435-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0d435-107">Permission type</span></span>|<span data-ttu-id="0d435-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0d435-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0d435-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0d435-109">Delegated (work or school account)</span></span>|<span data-ttu-id="0d435-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0d435-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="0d435-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0d435-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0d435-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0d435-112">Not supported.</span></span>|
|<span data-ttu-id="0d435-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0d435-113">Application</span></span>|<span data-ttu-id="0d435-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0d435-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0d435-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0d435-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement
```

## <a name="request-headers"></a><span data-ttu-id="0d435-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0d435-116">Request headers</span></span>
|<span data-ttu-id="0d435-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d435-117">Header</span></span>|<span data-ttu-id="0d435-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0d435-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0d435-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="0d435-119">Authorization</span></span>|<span data-ttu-id="0d435-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0d435-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="0d435-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0d435-121">Accept</span></span>|<span data-ttu-id="0d435-122">application/json</span><span class="sxs-lookup"><span data-stu-id="0d435-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0d435-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0d435-123">Request body</span></span>
<span data-ttu-id="0d435-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceManagement](../resources/intune_wip_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="0d435-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_wip_devicemanagement.md) object.</span></span>

<span data-ttu-id="0d435-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceManagement](../resources/intune_wip_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="0d435-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="0d435-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0d435-126">Property</span></span>|<span data-ttu-id="0d435-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="0d435-127">Type</span></span>|<span data-ttu-id="0d435-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d435-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0d435-129">id</span><span class="sxs-lookup"><span data-stu-id="0d435-129">id</span></span>|<span data-ttu-id="0d435-130">String</span><span class="sxs-lookup"><span data-stu-id="0d435-130">String</span></span>|<span data-ttu-id="0d435-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="0d435-131">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="0d435-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0d435-132">Response</span></span>
<span data-ttu-id="0d435-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceManagement](../resources/intune_wip_devicemanagement.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0d435-133">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_wip_devicemanagement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0d435-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0d435-134">Example</span></span>
### <a name="request"></a><span data-ttu-id="0d435-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0d435-135">Request</span></span>
<span data-ttu-id="0d435-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0d435-136">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a><span data-ttu-id="0d435-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0d435-137">Response</span></span>
<span data-ttu-id="0d435-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0d435-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 107

{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "0b283420-3420-0b28-2034-280b2034280b"
}
```



