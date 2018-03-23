# <a name="create-user"></a><span data-ttu-id="ec042-101">Crear usuario</span><span class="sxs-lookup"><span data-stu-id="ec042-101">Create User</span></span>

> <span data-ttu-id="ec042-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ec042-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ec042-103">Cree un objeto [user](../resources/intune_troubleshooting_user.md).</span><span class="sxs-lookup"><span data-stu-id="ec042-103">Create a new user object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ec042-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ec042-104">Prerequisites</span></span>
<span data-ttu-id="ec042-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ec042-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ec042-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ec042-107">Permission type</span></span>|<span data-ttu-id="ec042-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ec042-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ec042-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ec042-109">Delegated (work or school account)</span></span>|<span data-ttu-id="ec042-110">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ec042-110">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="ec042-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ec042-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ec042-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ec042-112">Not supported.</span></span>|
|<span data-ttu-id="ec042-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ec042-113">Application</span></span>|<span data-ttu-id="ec042-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ec042-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ec042-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ec042-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users
```

## <a name="request-headers"></a><span data-ttu-id="ec042-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ec042-116">Request headers</span></span>
|<span data-ttu-id="ec042-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec042-117">Header</span></span>|<span data-ttu-id="ec042-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ec042-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ec042-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="ec042-119">Authorization</span></span>|<span data-ttu-id="ec042-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ec042-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="ec042-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ec042-121">Accept</span></span>|<span data-ttu-id="ec042-122">application/json</span><span class="sxs-lookup"><span data-stu-id="ec042-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ec042-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ec042-123">Request body</span></span>
<span data-ttu-id="ec042-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto user.</span><span class="sxs-lookup"><span data-stu-id="ec042-124">In the request body, supply a JSON representation of user object.</span></span>

<span data-ttu-id="ec042-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto user.</span><span class="sxs-lookup"><span data-stu-id="ec042-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="ec042-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ec042-126">Property</span></span>|<span data-ttu-id="ec042-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="ec042-127">Type</span></span>|<span data-ttu-id="ec042-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec042-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ec042-129">id</span><span class="sxs-lookup"><span data-stu-id="ec042-129">id</span></span>|<span data-ttu-id="ec042-130">String</span><span class="sxs-lookup"><span data-stu-id="ec042-130">String</span></span>|<span data-ttu-id="ec042-131">Identificador único del usuario</span><span class="sxs-lookup"><span data-stu-id="ec042-131">Unique identifier for the lab user.</span></span>|



## <a name="response"></a><span data-ttu-id="ec042-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ec042-132">Response</span></span>
<span data-ttu-id="ec042-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [user](../resources/intune_troubleshooting_user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ec042-133">If successful, this method returns a `201 Created` response code and [user](../resources/intune_troubleshooting_user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ec042-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ec042-134">Example</span></span>
### <a name="request"></a><span data-ttu-id="ec042-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ec042-135">Request</span></span>
<span data-ttu-id="ec042-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ec042-136">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/users
Content-type: application/json
Content-length: 46

{
  "@odata.type": "#microsoft.graph.user"
}
```

### <a name="response"></a><span data-ttu-id="ec042-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ec042-137">Response</span></span>
<span data-ttu-id="ec042-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ec042-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 95

{
  "@odata.type": "#microsoft.graph.user",
  "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
}
```



