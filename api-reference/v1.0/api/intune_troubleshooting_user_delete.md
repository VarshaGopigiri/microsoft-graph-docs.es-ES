# <a name="delete-user"></a><span data-ttu-id="79bea-101">Eliminar usuario</span><span class="sxs-lookup"><span data-stu-id="79bea-101">Delete user</span></span>

> <span data-ttu-id="79bea-102">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="79bea-102">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="79bea-103">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="79bea-103">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="79bea-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="79bea-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="79bea-105">Elimina un [user](../resources/intune_troubleshooting_user.md).</span><span class="sxs-lookup"><span data-stu-id="79bea-105">Deletes a [user](../resources/intune_troubleshooting_user.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="79bea-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="79bea-106">Prerequisites</span></span>
<span data-ttu-id="79bea-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="79bea-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="79bea-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="79bea-109">Permission type</span></span>|<span data-ttu-id="79bea-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="79bea-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="79bea-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="79bea-111">Delegated (work or school account)</span></span>|<span data-ttu-id="79bea-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="79bea-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="79bea-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="79bea-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="79bea-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="79bea-114">Not supported.</span></span>|
|<span data-ttu-id="79bea-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="79bea-115">Application</span></span>|<span data-ttu-id="79bea-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="79bea-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="79bea-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="79bea-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /users/{usersId}
```

## <a name="request-headers"></a><span data-ttu-id="79bea-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="79bea-118">Request headers</span></span>
|<span data-ttu-id="79bea-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79bea-119">Header</span></span>|<span data-ttu-id="79bea-120">Valor</span><span class="sxs-lookup"><span data-stu-id="79bea-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="79bea-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="79bea-121">Authorization</span></span>|<span data-ttu-id="79bea-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="79bea-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="79bea-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="79bea-123">Accept</span></span>|<span data-ttu-id="79bea-124">application/json</span><span class="sxs-lookup"><span data-stu-id="79bea-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="79bea-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="79bea-125">Request body</span></span>
<span data-ttu-id="79bea-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="79bea-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="79bea-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79bea-127">Response</span></span>
<span data-ttu-id="79bea-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="79bea-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="79bea-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="79bea-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="79bea-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="79bea-130">Request</span></span>
<span data-ttu-id="79bea-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="79bea-131">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/beta/users/{usersId}
```

### <a name="response"></a><span data-ttu-id="79bea-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79bea-132">Response</span></span>
<span data-ttu-id="79bea-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="79bea-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



