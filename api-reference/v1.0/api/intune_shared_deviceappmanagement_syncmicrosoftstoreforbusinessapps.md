# <a name="syncmicrosoftstoreforbusinessapps-action"></a><span data-ttu-id="6e2cb-101">Acción syncMicrosoftStoreForBusinessApps</span><span class="sxs-lookup"><span data-stu-id="6e2cb-101">syncMicrosoftStoreForBusinessApps action</span></span>

> <span data-ttu-id="6e2cb-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6e2cb-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6e2cb-103">Sincroniza la cuenta de Intune con Microsoft Store para Empresas</span><span class="sxs-lookup"><span data-stu-id="6e2cb-103">Syncs Intune account with Microsoft Store For Business</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6e2cb-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6e2cb-104">Prerequisites</span></span>
<span data-ttu-id="6e2cb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6e2cb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6e2cb-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6e2cb-107">Permission type</span></span>|<span data-ttu-id="6e2cb-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6e2cb-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6e2cb-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6e2cb-109">Delegated (work or school account)</span></span>| 
| <span data-ttu-id="6e2cb-110">&nbsp; &nbsp; _Incorporación_</span><span class="sxs-lookup"><span data-stu-id="6e2cb-110">&nbsp; &nbsp; _On-boarding_</span></span> | <span data-ttu-id="6e2cb-111">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6e2cb-111">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="6e2cb-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6e2cb-112">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6e2cb-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6e2cb-113">Not supported.</span></span>|
|<span data-ttu-id="6e2cb-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6e2cb-114">Application</span></span>|<span data-ttu-id="6e2cb-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6e2cb-115">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6e2cb-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6e2cb-116">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/syncMicrosoftStoreForBusinessApps
```

## <a name="request-headers"></a><span data-ttu-id="6e2cb-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6e2cb-117">Request headers</span></span>
|<span data-ttu-id="6e2cb-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e2cb-118">Header</span></span>|<span data-ttu-id="6e2cb-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6e2cb-119">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6e2cb-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="6e2cb-120">Authorization</span></span>|<span data-ttu-id="6e2cb-121">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6e2cb-121">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6e2cb-122">Accept</span><span class="sxs-lookup"><span data-stu-id="6e2cb-122">Accept</span></span>|<span data-ttu-id="6e2cb-123">application/json</span><span class="sxs-lookup"><span data-stu-id="6e2cb-123">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6e2cb-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6e2cb-124">Request body</span></span>
<span data-ttu-id="6e2cb-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6e2cb-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6e2cb-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6e2cb-126">Response</span></span>
<span data-ttu-id="6e2cb-127">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="6e2cb-127">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example-request"></a><span data-ttu-id="6e2cb-128">Ejemplo de solicitud</span><span class="sxs-lookup"><span data-stu-id="6e2cb-128">Example request</span></span>

``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/syncMicrosoftStoreForBusinessApps
```

### <a name="response"></a><span data-ttu-id="6e2cb-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6e2cb-129">Response</span></span>

<span data-ttu-id="6e2cb-130">Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="6e2cb-130">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="6e2cb-131">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6e2cb-131">All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 204 No Content
```



