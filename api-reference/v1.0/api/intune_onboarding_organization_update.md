# <a name="update-organization"></a><span data-ttu-id="a4ac6-101">Actualizar organización</span><span class="sxs-lookup"><span data-stu-id="a4ac6-101">Update organization</span></span>

> <span data-ttu-id="a4ac6-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a4ac6-103">Actualice las propiedades de un objeto [organization](../resources/intune_onboarding_organization.md).</span><span class="sxs-lookup"><span data-stu-id="a4ac6-103">Update the properties of a [organization](../resources/intune_onboarding_organization.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a4ac6-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a4ac6-104">Prerequisites</span></span>
<span data-ttu-id="a4ac6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a4ac6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a4ac6-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a4ac6-107">Permission type</span></span>|<span data-ttu-id="a4ac6-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a4ac6-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a4ac6-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a4ac6-109">Delegated (work or school account)</span></span>|<span data-ttu-id="a4ac6-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a4ac6-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="a4ac6-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a4ac6-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a4ac6-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-112">Not supported.</span></span>|
|<span data-ttu-id="a4ac6-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a4ac6-113">Application</span></span>|<span data-ttu-id="a4ac6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a4ac6-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a4ac6-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /organization/{organizationId}
```

## <a name="request-headers"></a><span data-ttu-id="a4ac6-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a4ac6-116">Request headers</span></span>
|<span data-ttu-id="a4ac6-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4ac6-117">Header</span></span>|<span data-ttu-id="a4ac6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a4ac6-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a4ac6-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="a4ac6-119">Authorization</span></span>|<span data-ttu-id="a4ac6-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a4ac6-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a4ac6-121">Accept</span></span>|<span data-ttu-id="a4ac6-122">application/json</span><span class="sxs-lookup"><span data-stu-id="a4ac6-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a4ac6-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a4ac6-123">Request body</span></span>
<span data-ttu-id="a4ac6-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [organization](../resources/intune_onboarding_organization.md).</span><span class="sxs-lookup"><span data-stu-id="a4ac6-124">In the request body, supply a JSON representation for the [organization](../resources/intune_onboarding_organization.md) object.</span></span>

<span data-ttu-id="a4ac6-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [organization](../resources/intune_onboarding_organization.md).</span><span class="sxs-lookup"><span data-stu-id="a4ac6-125">The following table shows the properties that are required when you create the [organization](../resources/intune_onboarding_organization.md).</span></span>

|<span data-ttu-id="a4ac6-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a4ac6-126">Property</span></span>|<span data-ttu-id="a4ac6-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="a4ac6-127">Type</span></span>|<span data-ttu-id="a4ac6-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4ac6-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a4ac6-129">id</span><span class="sxs-lookup"><span data-stu-id="a4ac6-129">id</span></span>|<span data-ttu-id="a4ac6-130">String</span><span class="sxs-lookup"><span data-stu-id="a4ac6-130">String</span></span>|<span data-ttu-id="a4ac6-131">El GUID para el objeto.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-131">The GUID for the object.</span></span>|
|<span data-ttu-id="a4ac6-132">mobileDeviceManagementAuthority</span><span class="sxs-lookup"><span data-stu-id="a4ac6-132">mobileDeviceManagementAuthority</span></span>|[<span data-ttu-id="a4ac6-133">mdmAuthority</span><span class="sxs-lookup"><span data-stu-id="a4ac6-133">mdmAuthority</span></span>](../resources/intune_onboarding_mdmauthority.md)|<span data-ttu-id="a4ac6-134">Entidad de administración de dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-134">Mobile device management authority.</span></span> <span data-ttu-id="a4ac6-135">Los valores posibles son: `unknown`, `intune`, `sccm` y `office365`.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-135">Possible values are: `unknown`, `intune`, `sccm`, `office365`.</span></span>|



## <a name="response"></a><span data-ttu-id="a4ac6-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4ac6-136">Response</span></span>
<span data-ttu-id="a4ac6-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [organization](../resources/intune_onboarding_organization.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-137">If successful, this method returns a `200 OK` response code and an updated [organization](../resources/intune_onboarding_organization.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a4ac6-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a4ac6-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="a4ac6-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a4ac6-139">Request</span></span>
<span data-ttu-id="a4ac6-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-140">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/organization/{organizationId}
Content-type: application/json
Content-length: 102

{
  "@odata.type": "#microsoft.graph.organization",
  "mobileDeviceManagementAuthority": "intune"
}
```

### <a name="response"></a><span data-ttu-id="a4ac6-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4ac6-141">Response</span></span>
<span data-ttu-id="a4ac6-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 151

{
  "@odata.type": "#microsoft.graph.organization",
  "id": "9efe224a-224a-9efe-4a22-fe9e4a22fe9e",
  "mobileDeviceManagementAuthority": "intune"
}
```



