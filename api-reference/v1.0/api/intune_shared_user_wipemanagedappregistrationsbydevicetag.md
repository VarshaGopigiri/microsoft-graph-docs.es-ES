# <a name="wipemanagedappregistrationsbydevicetag-action"></a><span data-ttu-id="df5b0-101">Acción wipeManagedAppRegistrationsByDeviceTag</span><span class="sxs-lookup"><span data-stu-id="df5b0-101">wipeManagedAppRegistrationsByDeviceTag action</span></span>



> <span data-ttu-id="df5b0-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="df5b0-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="df5b0-103">Emite una operación de borrado en un registro de la aplicación con la etiqueta del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="df5b0-103">Issues a wipe operation on an app registration with specified device tag.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="df5b0-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="df5b0-104">Prerequisites</span></span>
<span data-ttu-id="df5b0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="df5b0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="df5b0-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="df5b0-107">Permission type</span></span>|<span data-ttu-id="df5b0-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="df5b0-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="df5b0-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="df5b0-109">Delegated (work or school account)</span></span>| <span data-ttu-id="df5b0-110">_varía según el contexto_</span><span class="sxs-lookup"><span data-stu-id="df5b0-110">_varies by context_</span></span> |
| <span data-ttu-id="df5b0-111">&nbsp;&nbsp; MAM</span><span class="sxs-lookup"><span data-stu-id="df5b0-111">&nbsp; &nbsp; MAM</span></span> | <span data-ttu-id="df5b0-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="df5b0-112">DeviceManagementApps.ReadWrite.All</span></span> |
|<span data-ttu-id="df5b0-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="df5b0-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="df5b0-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="df5b0-114">Not supported.</span></span>|
|<span data-ttu-id="df5b0-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="df5b0-115">Application</span></span>|<span data-ttu-id="df5b0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="df5b0-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="df5b0-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="df5b0-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/wipeManagedAppRegistrationsByDeviceTag
```

## <a name="request-headers"></a><span data-ttu-id="df5b0-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="df5b0-118">Request headers</span></span>
|<span data-ttu-id="df5b0-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df5b0-119">Header</span></span>|<span data-ttu-id="df5b0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="df5b0-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="df5b0-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="df5b0-121">Authorization</span></span>|<span data-ttu-id="df5b0-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="df5b0-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="df5b0-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="df5b0-123">Accept</span></span>|<span data-ttu-id="df5b0-124">application/json</span><span class="sxs-lookup"><span data-stu-id="df5b0-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="df5b0-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="df5b0-125">Request body</span></span>
<span data-ttu-id="df5b0-126">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="df5b0-126">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="df5b0-127">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="df5b0-127">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="df5b0-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="df5b0-128">Property</span></span>|<span data-ttu-id="df5b0-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="df5b0-129">Type</span></span>|<span data-ttu-id="df5b0-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="df5b0-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="df5b0-131">deviceTag</span><span class="sxs-lookup"><span data-stu-id="df5b0-131">deviceTag</span></span>|<span data-ttu-id="df5b0-132">String</span><span class="sxs-lookup"><span data-stu-id="df5b0-132">String</span></span>|<span data-ttu-id="df5b0-133">etiqueta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="df5b0-133">device tag</span></span>|

## <a name="response"></a><span data-ttu-id="df5b0-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="df5b0-134">Response</span></span>
<span data-ttu-id="df5b0-135">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="df5b0-135">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="df5b0-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="df5b0-136">Example</span></span>

### <a name="request"></a><span data-ttu-id="df5b0-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="df5b0-137">Request</span></span>
<span data-ttu-id="df5b0-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="df5b0-138">Here is an example of the request.</span></span>

``` http
POST https://graph.microsoft.com/beta/users/{usersId}/wipeManagedAppRegistrationsByDeviceTag

Content-type: application/json
Content-length: 39

{
  "deviceTag": "Device Tag value"
}
```

### <a name="response"></a><span data-ttu-id="df5b0-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="df5b0-139">Response</span></span>
<span data-ttu-id="df5b0-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="df5b0-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 204 No Content
```



