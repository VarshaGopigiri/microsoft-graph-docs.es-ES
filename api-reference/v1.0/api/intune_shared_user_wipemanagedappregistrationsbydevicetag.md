# <a name="wipemanagedappregistrationsbydevicetag-action"></a><span data-ttu-id="db878-101">Acción wipeManagedAppRegistrationsByDeviceTag</span><span class="sxs-lookup"><span data-stu-id="db878-101">wipeManagedAppRegistrationsByDeviceTag action</span></span>

> <span data-ttu-id="db878-102">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="db878-102">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="db878-103">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="db878-103">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="db878-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="db878-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="db878-105">Emite una operación de borrado en un registro de la aplicación con la etiqueta del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="db878-105">Issues a wipe operation on an app registration with specified device tag.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="db878-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="db878-106">Prerequisites</span></span>
<span data-ttu-id="db878-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="db878-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="db878-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="db878-109">Permission type</span></span>|<span data-ttu-id="db878-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="db878-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="db878-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="db878-111">Delegated (work or school account)</span></span>| <span data-ttu-id="db878-112">_varía según el contexto_</span><span class="sxs-lookup"><span data-stu-id="db878-112">_varies by context_</span></span> |
| <span data-ttu-id="db878-113">&nbsp; &nbsp; MAM</span><span class="sxs-lookup"><span data-stu-id="db878-113">.mam</span></span> | <span data-ttu-id="db878-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="db878-114">DeviceManagementApps.ReadWrite.All</span></span> |
|<span data-ttu-id="db878-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="db878-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="db878-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="db878-116">Not supported.</span></span>|
|<span data-ttu-id="db878-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="db878-117">Application</span></span>|<span data-ttu-id="db878-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="db878-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="db878-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="db878-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/wipeManagedAppRegistrationsByDeviceTag
```

## <a name="request-headers"></a><span data-ttu-id="db878-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="db878-120">Request headers</span></span>
|<span data-ttu-id="db878-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db878-121">Header</span></span>|<span data-ttu-id="db878-122">Valor</span><span class="sxs-lookup"><span data-stu-id="db878-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="db878-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="db878-123">Authorization</span></span>|<span data-ttu-id="db878-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="db878-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="db878-125">Accept</span><span class="sxs-lookup"><span data-stu-id="db878-125">Accept</span></span>|<span data-ttu-id="db878-126">application/json</span><span class="sxs-lookup"><span data-stu-id="db878-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="db878-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="db878-127">Request body</span></span>
<span data-ttu-id="db878-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="db878-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="db878-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="db878-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="db878-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="db878-130">Property</span></span>|<span data-ttu-id="db878-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="db878-131">Type</span></span>|<span data-ttu-id="db878-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="db878-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="db878-133">deviceTag</span><span class="sxs-lookup"><span data-stu-id="db878-133">deviceTag</span></span>|<span data-ttu-id="db878-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="db878-134">String</span></span>|<span data-ttu-id="db878-135">etiqueta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="db878-135">device tag</span></span>|

## <a name="response"></a><span data-ttu-id="db878-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="db878-136">Response</span></span>
<span data-ttu-id="db878-137">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="db878-137">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="db878-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="db878-138">Example</span></span>

### <a name="request"></a><span data-ttu-id="db878-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="db878-139">Request</span></span>
<span data-ttu-id="db878-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="db878-140">Here is an example of the request.</span></span>

``` http
POST https://graph.microsoft.com/beta/users/{usersId}/wipeManagedAppRegistrationsByDeviceTag

Content-type: application/json
Content-length: 39

{
  "deviceTag": "Device Tag value"
}
```

### <a name="response"></a><span data-ttu-id="db878-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="db878-141">Response</span></span>
<span data-ttu-id="db878-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="db878-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 204 No Content
```



