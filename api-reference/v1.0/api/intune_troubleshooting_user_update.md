# <a name="update-user"></a><span data-ttu-id="cd0e8-101">Actualizar usuario</span><span class="sxs-lookup"><span data-stu-id="cd0e8-101">Update user</span></span>

> <span data-ttu-id="cd0e8-102">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cd0e8-102">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cd0e8-103">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cd0e8-103">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cd0e8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cd0e8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cd0e8-105">Actualice las propiedades de un objeto [user](../resources/intune_troubleshooting_user.md).</span><span class="sxs-lookup"><span data-stu-id="cd0e8-105">Update the properties of a [user](../resources/intune_troubleshooting_user.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cd0e8-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cd0e8-106">Prerequisites</span></span>
<span data-ttu-id="cd0e8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="cd0e8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="cd0e8-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cd0e8-109">Permission type</span></span>|<span data-ttu-id="cd0e8-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cd0e8-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cd0e8-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cd0e8-111">Delegated (work or school account)</span></span>|<span data-ttu-id="cd0e8-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cd0e8-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="cd0e8-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cd0e8-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cd0e8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cd0e8-114">Not supported.</span></span>|
|<span data-ttu-id="cd0e8-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cd0e8-115">Application</span></span>|<span data-ttu-id="cd0e8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cd0e8-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cd0e8-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cd0e8-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /users/{usersId}
```

## <a name="request-headers"></a><span data-ttu-id="cd0e8-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cd0e8-118">Request headers</span></span>
|<span data-ttu-id="cd0e8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd0e8-119">Header</span></span>|<span data-ttu-id="cd0e8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cd0e8-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cd0e8-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="cd0e8-121">Authorization</span></span>|<span data-ttu-id="cd0e8-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cd0e8-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cd0e8-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cd0e8-123">Accept</span></span>|<span data-ttu-id="cd0e8-124">application/json</span><span class="sxs-lookup"><span data-stu-id="cd0e8-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cd0e8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cd0e8-125">Request body</span></span>
<span data-ttu-id="cd0e8-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [user](../resources/intune_troubleshooting_user.md).</span><span class="sxs-lookup"><span data-stu-id="cd0e8-126">In the request body, supply a JSON representation for the [user](../resources/intune_troubleshooting_user.md) object.</span></span>

<span data-ttu-id="cd0e8-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [user](../resources/intune_troubleshooting_user.md).</span><span class="sxs-lookup"><span data-stu-id="cd0e8-127">The following table shows the properties that are required when you create the [user](../resources/intune_troubleshooting_user.md).</span></span>

|<span data-ttu-id="cd0e8-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cd0e8-128">Property</span></span>|<span data-ttu-id="cd0e8-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd0e8-129">Type</span></span>|<span data-ttu-id="cd0e8-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd0e8-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cd0e8-131">id</span><span class="sxs-lookup"><span data-stu-id="cd0e8-131">id</span></span>|<span data-ttu-id="cd0e8-132">String</span><span class="sxs-lookup"><span data-stu-id="cd0e8-132">String</span></span>|<span data-ttu-id="cd0e8-133">Identificador único del usuario</span><span class="sxs-lookup"><span data-stu-id="cd0e8-133">Unique Identifier for the user</span></span>|



## <a name="response"></a><span data-ttu-id="cd0e8-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd0e8-134">Response</span></span>
<span data-ttu-id="cd0e8-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [user](../resources/intune_troubleshooting_user.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cd0e8-135">If successful, this method returns a `200 OK` response code and an updated [user](../resources/intune_troubleshooting_user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cd0e8-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd0e8-136">Example</span></span>
### <a name="request"></a><span data-ttu-id="cd0e8-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cd0e8-137">Request</span></span>
<span data-ttu-id="cd0e8-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cd0e8-138">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/users/{usersId}
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a><span data-ttu-id="cd0e8-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd0e8-139">Response</span></span>
<span data-ttu-id="cd0e8-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cd0e8-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 95

{
  "@odata.type": "#microsoft.graph.user",
  "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
}
```



