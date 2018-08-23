# <a name="delete-user"></a><span data-ttu-id="88004-101">Eliminar usuario</span><span class="sxs-lookup"><span data-stu-id="88004-101">Delete user</span></span>

> <span data-ttu-id="88004-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="88004-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="88004-103">Elimina un [user](../resources/intune_shared_user.md).</span><span class="sxs-lookup"><span data-stu-id="88004-103">Deletes a [user](../resources/intune_shared_user.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="88004-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="88004-104">Prerequisites</span></span>
<span data-ttu-id="88004-105">Se requiere uno de los siguientes permisos para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="88004-105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see Permissions.</span></span> <span data-ttu-id="88004-106">Para obtener más información, incluso sobre cómo elegir permisos, consulte [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="88004-106">To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>  <span data-ttu-id="88004-107">Según el contexto, se le requerirá un permiso específico.</span><span class="sxs-lookup"><span data-stu-id="88004-107">The specific permission required depends on context.</span></span>

|<span data-ttu-id="88004-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="88004-108">Permission type</span></span>|<span data-ttu-id="88004-109">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="88004-109">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="88004-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="88004-110">Delegated (work or school account)</span></span>| <span data-ttu-id="88004-111">_varía según el contexto_</span><span class="sxs-lookup"><span data-stu-id="88004-111">_varies by context_</span></span>|
| <span data-ttu-id="88004-112">&nbsp; &nbsp; Dispositivos</span><span class="sxs-lookup"><span data-stu-id="88004-112">&nbsp;&nbsp;</span></span> | <span data-ttu-id="88004-113">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="88004-113">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
| <span data-ttu-id="88004-114">&nbsp; &nbsp; MAM</span><span class="sxs-lookup"><span data-stu-id="88004-114">.mam</span></span> | <span data-ttu-id="88004-115">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="88004-115">DeviceManagementApps.ReadWrite.All</span></span> |
| <span data-ttu-id="88004-116">&nbsp; &nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="88004-116">&nbsp; &nbsp; On-boarding</span></span> | <span data-ttu-id="88004-117">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="88004-117">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="88004-118">&nbsp; &nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="88004-118">&nbsp; &nbsp;Troubleshooting</span></span> | <span data-ttu-id="88004-119">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="88004-119">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
|<span data-ttu-id="88004-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="88004-120">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="88004-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="88004-121">Not supported.</span></span>|
|<span data-ttu-id="88004-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="88004-122">Application</span></span>|<span data-ttu-id="88004-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="88004-123">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="88004-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="88004-124">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /users/{usersId}
```

## <a name="request-headers"></a><span data-ttu-id="88004-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="88004-125">Request headers</span></span>
|<span data-ttu-id="88004-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88004-126">Header</span></span>|<span data-ttu-id="88004-127">Valor</span><span class="sxs-lookup"><span data-stu-id="88004-127">Value</span></span>|
|:---|:---|
|<span data-ttu-id="88004-128">Autorización</span><span class="sxs-lookup"><span data-stu-id="88004-128">Authorization</span></span>|<span data-ttu-id="88004-129">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="88004-129">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="88004-130">Aceptar</span><span class="sxs-lookup"><span data-stu-id="88004-130">Accept</span></span>|<span data-ttu-id="88004-131">application/json</span><span class="sxs-lookup"><span data-stu-id="88004-131">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="88004-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="88004-132">Request body</span></span>
<span data-ttu-id="88004-133">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="88004-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="88004-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88004-134">Response</span></span>
<span data-ttu-id="88004-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="88004-135">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="88004-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="88004-136">Example</span></span>

### <a name="request"></a><span data-ttu-id="88004-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="88004-137">Request</span></span>
<span data-ttu-id="88004-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="88004-138">Here is an example of the request.</span></span>

``` http
DELETE https://graph.microsoft.com/v1.0/users/{usersId}
```

### <a name="response"></a><span data-ttu-id="88004-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88004-139">Response</span></span>
<span data-ttu-id="88004-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="88004-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 204 No Content
```



