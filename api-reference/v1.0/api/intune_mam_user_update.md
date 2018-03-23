# <a name="update-user"></a><span data-ttu-id="48d59-101">Actualizar usuario</span><span class="sxs-lookup"><span data-stu-id="48d59-101">Update user</span></span>

> <span data-ttu-id="48d59-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="48d59-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="48d59-103">Actualice las propiedades de un objeto [user](../resources/intune_mam_user.md).</span><span class="sxs-lookup"><span data-stu-id="48d59-103">Update the properties of a user object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="48d59-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="48d59-104">Prerequisites</span></span>
<span data-ttu-id="48d59-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="48d59-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="48d59-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="48d59-107">Permission type</span></span>|<span data-ttu-id="48d59-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="48d59-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="48d59-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="48d59-109">Delegated (work or school account)</span></span>|<span data-ttu-id="48d59-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="48d59-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="48d59-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="48d59-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="48d59-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="48d59-112">Not supported.</span></span>|
|<span data-ttu-id="48d59-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="48d59-113">Application</span></span>|<span data-ttu-id="48d59-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="48d59-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="48d59-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="48d59-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /users/{usersId}
```

## <a name="request-headers"></a><span data-ttu-id="48d59-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="48d59-116">Request headers</span></span>
|<span data-ttu-id="48d59-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48d59-117">Header</span></span>|<span data-ttu-id="48d59-118">Valor</span><span class="sxs-lookup"><span data-stu-id="48d59-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="48d59-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="48d59-119">Authorization</span></span>|<span data-ttu-id="48d59-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="48d59-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="48d59-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="48d59-121">Accept</span></span>|<span data-ttu-id="48d59-122">application/json</span><span class="sxs-lookup"><span data-stu-id="48d59-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="48d59-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="48d59-123">Request body</span></span>
<span data-ttu-id="48d59-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [user](../resources/intune_mam_user.md).</span><span class="sxs-lookup"><span data-stu-id="48d59-124">In the request body, supply a JSON representation of [user](../resources/intune_mam_user.md) object.</span></span>

<span data-ttu-id="48d59-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [user](../resources/intune_mam_user.md).</span><span class="sxs-lookup"><span data-stu-id="48d59-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="48d59-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="48d59-126">Property</span></span>|<span data-ttu-id="48d59-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="48d59-127">Type</span></span>|<span data-ttu-id="48d59-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="48d59-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="48d59-129">id</span><span class="sxs-lookup"><span data-stu-id="48d59-129">id</span></span>|<span data-ttu-id="48d59-130">String</span><span class="sxs-lookup"><span data-stu-id="48d59-130">String</span></span>|<span data-ttu-id="48d59-131">El identificador de usuario.</span><span class="sxs-lookup"><span data-stu-id="48d59-131">The user identifier.</span></span>|



## <a name="response"></a><span data-ttu-id="48d59-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48d59-132">Response</span></span>
<span data-ttu-id="48d59-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [user](../resources/intune_mam_user.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="48d59-133">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_mam_user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="48d59-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="48d59-134">Example</span></span>
### <a name="request"></a><span data-ttu-id="48d59-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48d59-135">Request</span></span>
<span data-ttu-id="48d59-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="48d59-136">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/users/{usersId}
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a><span data-ttu-id="48d59-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48d59-137">Response</span></span>
<span data-ttu-id="48d59-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="48d59-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 95

{
  "@odata.type": "#microsoft.graph.user",
  "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
}
```



