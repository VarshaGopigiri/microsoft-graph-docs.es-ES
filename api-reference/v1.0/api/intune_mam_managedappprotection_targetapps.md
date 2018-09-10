# <a name="targetapps-action"></a><span data-ttu-id="84060-101">Acción targetApps</span><span class="sxs-lookup"><span data-stu-id="84060-101">targetApps action</span></span>

> <span data-ttu-id="84060-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="84060-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="84060-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="84060-103">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="84060-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="84060-104">Prerequisites</span></span>
<span data-ttu-id="84060-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="84060-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="84060-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="84060-107">Permission type</span></span>|<span data-ttu-id="84060-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="84060-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="84060-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="84060-109">Delegated (work or school account)</span></span>|<span data-ttu-id="84060-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="84060-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="84060-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="84060-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="84060-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="84060-112">Not supported.</span></span>|
|<span data-ttu-id="84060-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="84060-113">Application</span></span>|<span data-ttu-id="84060-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="84060-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="84060-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="84060-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedAppPolicies/{managedAppPolicyId}/targetApps
POST /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/appliedPolicies/{managedAppPolicyId}/targetApps
POST /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/intendedPolicies/{managedAppPolicyId}/targetApps
```

## <a name="request-headers"></a><span data-ttu-id="84060-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="84060-116">Request headers</span></span>
|<span data-ttu-id="84060-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84060-117">Header</span></span>|<span data-ttu-id="84060-118">Valor</span><span class="sxs-lookup"><span data-stu-id="84060-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="84060-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="84060-119">Authorization</span></span>|<span data-ttu-id="84060-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="84060-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="84060-121">Accept</span><span class="sxs-lookup"><span data-stu-id="84060-121">Accept</span></span>|<span data-ttu-id="84060-122">application/json</span><span class="sxs-lookup"><span data-stu-id="84060-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="84060-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="84060-123">Request body</span></span>
<span data-ttu-id="84060-124">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="84060-124">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="84060-125">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="84060-125">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="84060-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="84060-126">Property</span></span>|<span data-ttu-id="84060-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="84060-127">Type</span></span>|<span data-ttu-id="84060-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="84060-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="84060-129">apps</span><span class="sxs-lookup"><span data-stu-id="84060-129">apps</span></span>|<span data-ttu-id="84060-130">Colección [managedMobileApp](../resources/intune_mam_managedmobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="84060-130">[managedMobileApp](../resources/intune_mam_managedmobileapp.md) collection</span></span>|<span data-ttu-id="84060-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="84060-131">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="84060-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="84060-132">Response</span></span>
<span data-ttu-id="84060-133">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="84060-133">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="84060-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84060-134">Example</span></span>
### <a name="request"></a><span data-ttu-id="84060-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="84060-135">Request</span></span>
<span data-ttu-id="84060-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="84060-136">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppPolicies/{managedAppPolicyId}/targetApps

Content-type: application/json
Content-length: 286

{
  "apps": [
    {
      "@odata.type": "#microsoft.graph.managedMobileApp",
      "mobileAppIdentifier": {
        "@odata.type": "microsoft.graph.mobileAppIdentifier"
      },
      "id": "0a129715-9715-0a12-1597-120a1597120a",
      "version": "Version value"
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="84060-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="84060-137">Response</span></span>
<span data-ttu-id="84060-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="84060-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```








