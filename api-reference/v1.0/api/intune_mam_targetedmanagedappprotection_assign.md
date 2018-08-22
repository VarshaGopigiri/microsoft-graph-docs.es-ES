# <a name="assign-action"></a><span data-ttu-id="3bca6-101">asignar acción</span><span class="sxs-lookup"><span data-stu-id="3bca6-101">assign action</span></span>

> <span data-ttu-id="3bca6-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3bca6-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3bca6-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3bca6-103">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3bca6-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3bca6-104">Prerequisites</span></span>
<span data-ttu-id="3bca6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3bca6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="3bca6-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3bca6-107">Permission type</span></span>|<span data-ttu-id="3bca6-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3bca6-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3bca6-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3bca6-109">Delegated (work or school account)</span></span>|<span data-ttu-id="3bca6-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3bca6-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="3bca6-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3bca6-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3bca6-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3bca6-112">Not supported.</span></span>|
|<span data-ttu-id="3bca6-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3bca6-113">Application</span></span>|<span data-ttu-id="3bca6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3bca6-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3bca6-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3bca6-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedAppPolicies/{managedAppPolicyId}/assign
POST /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/appliedPolicies/{managedAppPolicyId}/assign
POST /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/intendedPolicies/{managedAppPolicyId}/assign
```

## <a name="request-headers"></a><span data-ttu-id="3bca6-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3bca6-116">Request headers</span></span>
|<span data-ttu-id="3bca6-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3bca6-117">Header</span></span>|<span data-ttu-id="3bca6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3bca6-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3bca6-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="3bca6-119">Authorization</span></span>|<span data-ttu-id="3bca6-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3bca6-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3bca6-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3bca6-121">Accept</span></span>|<span data-ttu-id="3bca6-122">application/json</span><span class="sxs-lookup"><span data-stu-id="3bca6-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3bca6-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3bca6-123">Request body</span></span>
<span data-ttu-id="3bca6-124">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="3bca6-124">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="3bca6-125">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="3bca6-125">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="3bca6-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3bca6-126">Property</span></span>|<span data-ttu-id="3bca6-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="3bca6-127">Type</span></span>|<span data-ttu-id="3bca6-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="3bca6-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3bca6-129">asignaciones</span><span class="sxs-lookup"><span data-stu-id="3bca6-129">assignments</span></span>|<span data-ttu-id="3bca6-130">Colección [targetedManagedAppPolicyAssignment](../resources/intune_mam_targetedmanagedapppolicyassignment.md)</span><span class="sxs-lookup"><span data-stu-id="3bca6-130">[targetedManagedAppPolicyAssignment](../resources/intune_mam_targetedmanagedapppolicyassignment.md) collection</span></span>|<span data-ttu-id="3bca6-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3bca6-131">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="3bca6-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3bca6-132">Response</span></span>
<span data-ttu-id="3bca6-133">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="3bca6-133">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="3bca6-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3bca6-134">Example</span></span>
### <a name="request"></a><span data-ttu-id="3bca6-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3bca6-135">Request</span></span>
<span data-ttu-id="3bca6-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3bca6-136">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppPolicies/{managedAppPolicyId}/assign

Content-type: application/json
Content-length: 282

{
  "assignments": [
    {
      "@odata.type": "#microsoft.graph.targetedManagedAppPolicyAssignment",
      "id": "8b68c4a6-c4a6-8b68-a6c4-688ba6c4688b",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="3bca6-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3bca6-137">Response</span></span>
<span data-ttu-id="3bca6-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3bca6-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



