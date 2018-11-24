# <a name="syncmicrosoftstoreforbusinessapps-action"></a><span data-ttu-id="e229a-101">Acción syncMicrosoftStoreForBusinessApps</span><span class="sxs-lookup"><span data-stu-id="e229a-101">syncMicrosoftStoreForBusinessApps action</span></span>

> <span data-ttu-id="e229a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e229a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e229a-103">Sincroniza la cuenta de Intune con Microsoft Store para Empresas</span><span class="sxs-lookup"><span data-stu-id="e229a-103">Syncs Intune account with Microsoft Store For Business</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e229a-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e229a-104">Prerequisites</span></span>
<span data-ttu-id="e229a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e229a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e229a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e229a-107">Permission type</span></span>|<span data-ttu-id="e229a-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e229a-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e229a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e229a-109">Delegated (work or school account)</span></span>| 
| <span data-ttu-id="e229a-110">&nbsp;&nbsp; _Incorporación_</span><span class="sxs-lookup"><span data-stu-id="e229a-110">&nbsp; &nbsp; _Onboarding_</span></span> | <span data-ttu-id="e229a-111">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e229a-111">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="e229a-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e229a-112">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e229a-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e229a-113">Not supported.</span></span>|
|<span data-ttu-id="e229a-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e229a-114">Application</span></span>|<span data-ttu-id="e229a-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e229a-115">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e229a-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e229a-116">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/syncMicrosoftStoreForBusinessApps
```

## <a name="request-headers"></a><span data-ttu-id="e229a-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e229a-117">Request headers</span></span>
|<span data-ttu-id="e229a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e229a-118">Header</span></span>|<span data-ttu-id="e229a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e229a-119">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e229a-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="e229a-120">Authorization</span></span>|<span data-ttu-id="e229a-121">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e229a-121">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e229a-122">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e229a-122">Accept</span></span>|<span data-ttu-id="e229a-123">application/json</span><span class="sxs-lookup"><span data-stu-id="e229a-123">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e229a-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e229a-124">Request body</span></span>
<span data-ttu-id="e229a-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e229a-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e229a-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e229a-126">Response</span></span>
<span data-ttu-id="e229a-127">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="e229a-127">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example-request"></a><span data-ttu-id="e229a-128">Ejemplo de solicitud</span><span class="sxs-lookup"><span data-stu-id="e229a-128">Example request</span></span>

``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/syncMicrosoftStoreForBusinessApps
```

### <a name="response"></a><span data-ttu-id="e229a-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e229a-129">Response</span></span>

<span data-ttu-id="e229a-130">El objeto de respuesta que se muestra aquí es posible que esté truncado por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="e229a-130">The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="e229a-131">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e229a-131">All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 204 No Content
```



