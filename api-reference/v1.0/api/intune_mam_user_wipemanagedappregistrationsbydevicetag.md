# <a name="wipemanagedappregistrationsbydevicetag-action"></a><span data-ttu-id="abc55-101">Acción wipeManagedAppRegistrationsByDeviceTag</span><span class="sxs-lookup"><span data-stu-id="abc55-101">wipeManagedAppRegistrationsByDeviceTag action</span></span>

> <span data-ttu-id="abc55-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="abc55-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="abc55-103">Emite una operación de borrado en un registro de la aplicación con la etiqueta del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="abc55-103">Issues a wipe operation on an app registration with specified device tag.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="abc55-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="abc55-104">Prerequisites</span></span>
<span data-ttu-id="abc55-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="abc55-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="abc55-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="abc55-107">Permission type</span></span>|<span data-ttu-id="abc55-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="abc55-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="abc55-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="abc55-109">Delegated (work or school account)</span></span>|<span data-ttu-id="abc55-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="abc55-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="abc55-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="abc55-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="abc55-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="abc55-112">Not supported.</span></span>|
|<span data-ttu-id="abc55-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="abc55-113">Application</span></span>|<span data-ttu-id="abc55-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="abc55-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="abc55-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="abc55-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/wipeManagedAppRegistrationsByDeviceTag
```

## <a name="request-headers"></a><span data-ttu-id="abc55-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="abc55-116">Request headers</span></span>
|<span data-ttu-id="abc55-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="abc55-117">Header</span></span>|<span data-ttu-id="abc55-118">Valor</span><span class="sxs-lookup"><span data-stu-id="abc55-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="abc55-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="abc55-119">Authorization</span></span>|<span data-ttu-id="abc55-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="abc55-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="abc55-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="abc55-121">Accept</span></span>|<span data-ttu-id="abc55-122">application/json</span><span class="sxs-lookup"><span data-stu-id="abc55-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="abc55-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="abc55-123">Request body</span></span>
<span data-ttu-id="abc55-124">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="abc55-124">In the request body, supply a JSON representation of the Contact object.</span></span>

<span data-ttu-id="abc55-125">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="abc55-125">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="abc55-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="abc55-126">Property</span></span>|<span data-ttu-id="abc55-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="abc55-127">Type</span></span>|<span data-ttu-id="abc55-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="abc55-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="abc55-129">deviceTag</span><span class="sxs-lookup"><span data-stu-id="abc55-129">deviceTag</span></span>|<span data-ttu-id="abc55-130">String</span><span class="sxs-lookup"><span data-stu-id="abc55-130">String</span></span>|<span data-ttu-id="abc55-131">etiqueta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="abc55-131">device tag</span></span>|



## <a name="response"></a><span data-ttu-id="abc55-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="abc55-132">Response</span></span>
<span data-ttu-id="abc55-133">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="abc55-133">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="abc55-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="abc55-134">Example</span></span>
### <a name="request"></a><span data-ttu-id="abc55-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="abc55-135">Request</span></span>
<span data-ttu-id="abc55-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="abc55-136">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/users/{usersId}/wipeManagedAppRegistrationsByDeviceTag

Content-type: application/json
Content-length: 39

{
  "deviceTag": "Device Tag value"
}
```

### <a name="response"></a><span data-ttu-id="abc55-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="abc55-137">Response</span></span>
<span data-ttu-id="abc55-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="abc55-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



