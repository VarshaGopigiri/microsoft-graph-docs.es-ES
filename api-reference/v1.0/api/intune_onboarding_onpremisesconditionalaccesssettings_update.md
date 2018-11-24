# <a name="update-onpremisesconditionalaccesssettings"></a><span data-ttu-id="b34ff-101">Actualizar onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="b34ff-101">Update onPremisesConditionalAccessSettings</span></span>

> <span data-ttu-id="b34ff-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b34ff-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b34ff-103">Actualice las propiedades de un objeto [onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md).</span><span class="sxs-lookup"><span data-stu-id="b34ff-103">Update the properties of a [onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b34ff-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b34ff-104">Prerequisites</span></span>
<span data-ttu-id="b34ff-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b34ff-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b34ff-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b34ff-107">Permission type</span></span>|<span data-ttu-id="b34ff-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b34ff-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b34ff-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b34ff-109">Delegated (work or school account)</span></span>|<span data-ttu-id="b34ff-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b34ff-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="b34ff-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b34ff-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b34ff-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b34ff-112">Not supported.</span></span>|
|<span data-ttu-id="b34ff-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b34ff-113">Application</span></span>|<span data-ttu-id="b34ff-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b34ff-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b34ff-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b34ff-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/conditionalAccessSettings
```

## <a name="request-headers"></a><span data-ttu-id="b34ff-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b34ff-116">Request headers</span></span>
|<span data-ttu-id="b34ff-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b34ff-117">Header</span></span>|<span data-ttu-id="b34ff-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b34ff-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b34ff-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="b34ff-119">Authorization</span></span>|<span data-ttu-id="b34ff-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b34ff-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b34ff-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b34ff-121">Accept</span></span>|<span data-ttu-id="b34ff-122">application/json</span><span class="sxs-lookup"><span data-stu-id="b34ff-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b34ff-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b34ff-123">Request body</span></span>
<span data-ttu-id="b34ff-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md).</span><span class="sxs-lookup"><span data-stu-id="b34ff-124">In the request body, supply a JSON representation for the [onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md) object.</span></span>

<span data-ttu-id="b34ff-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md).</span><span class="sxs-lookup"><span data-stu-id="b34ff-125">The following table shows the properties that are required when you create the [onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md).</span></span>

|<span data-ttu-id="b34ff-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b34ff-126">Property</span></span>|<span data-ttu-id="b34ff-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="b34ff-127">Type</span></span>|<span data-ttu-id="b34ff-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="b34ff-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b34ff-129">id</span><span class="sxs-lookup"><span data-stu-id="b34ff-129">id</span></span>|<span data-ttu-id="b34ff-130">String</span><span class="sxs-lookup"><span data-stu-id="b34ff-130">String</span></span>|<span data-ttu-id="b34ff-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b34ff-131">Not yet documented</span></span>|
|<span data-ttu-id="b34ff-132">enabled</span><span class="sxs-lookup"><span data-stu-id="b34ff-132">enabled</span></span>|<span data-ttu-id="b34ff-133">Booleano</span><span class="sxs-lookup"><span data-stu-id="b34ff-133">Boolean</span></span>|<span data-ttu-id="b34ff-134">Indica si está habilitado el acceso condicional local para esta organización</span><span class="sxs-lookup"><span data-stu-id="b34ff-134">Indicates if on premises conditional access is enabled for this organization</span></span>|
|<span data-ttu-id="b34ff-135">includedGroups</span><span class="sxs-lookup"><span data-stu-id="b34ff-135">includedGroups</span></span>|<span data-ttu-id="b34ff-136">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="b34ff-136">Guid collection</span></span>|<span data-ttu-id="b34ff-137">Grupos de usuarios a los que se dirigirá el acceso condicional local.</span><span class="sxs-lookup"><span data-stu-id="b34ff-137">User groups that will be targeted by on premises conditional access.</span></span> <span data-ttu-id="b34ff-138">Todos los usuarios de estos grupos deberán tener dispositivos móviles administrados y compatibles para tener acceso al correo.</span><span class="sxs-lookup"><span data-stu-id="b34ff-138">All users in these groups will be required to have mobile device managed and compliant for mail access.</span></span>|
|<span data-ttu-id="b34ff-139">excludedGroups</span><span class="sxs-lookup"><span data-stu-id="b34ff-139">excludedGroups</span></span>|<span data-ttu-id="b34ff-140">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="b34ff-140">Guid collection</span></span>|<span data-ttu-id="b34ff-141">Grupos de usuarios que estarán exentos del acceso condicional local.</span><span class="sxs-lookup"><span data-stu-id="b34ff-141">User groups that will be exempt by on premises conditional access.</span></span> <span data-ttu-id="b34ff-142">Todos los usuarios de estos grupos estarán exentos de la directiva de acceso condicional.</span><span class="sxs-lookup"><span data-stu-id="b34ff-142">All users in these groups will be exempt from the conditional access policy.</span></span>|
|<span data-ttu-id="b34ff-143">overrideDefaultRule</span><span class="sxs-lookup"><span data-stu-id="b34ff-143">overrideDefaultRule</span></span>|<span data-ttu-id="b34ff-144">Booleano</span><span class="sxs-lookup"><span data-stu-id="b34ff-144">Boolean</span></span>|<span data-ttu-id="b34ff-145">Anular la regla de acceso predeterminada al permitir que un dispositivo garantice que se concede el acceso.</span><span class="sxs-lookup"><span data-stu-id="b34ff-145">Override the default access rule when allowing a device to ensure access is granted.</span></span>|



## <a name="response"></a><span data-ttu-id="b34ff-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b34ff-146">Response</span></span>
<span data-ttu-id="b34ff-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b34ff-147">If successful, this method returns a `200 OK` response code and an updated [onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b34ff-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b34ff-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="b34ff-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b34ff-149">Request</span></span>
<span data-ttu-id="b34ff-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b34ff-150">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/conditionalAccessSettings
Content-type: application/json
Content-length: 275

{
  "@odata.type": "#microsoft.graph.onPremisesConditionalAccessSettings",
  "enabled": true,
  "includedGroups": [
    "77c9d466-d466-77c9-66d4-c97766d4c977"
  ],
  "excludedGroups": [
    "2a0afae4-fae4-2a0a-e4fa-0a2ae4fa0a2a"
  ],
  "overrideDefaultRule": true
}
```

### <a name="response"></a><span data-ttu-id="b34ff-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b34ff-151">Response</span></span>
<span data-ttu-id="b34ff-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b34ff-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 324

{
  "@odata.type": "#microsoft.graph.onPremisesConditionalAccessSettings",
  "id": "a0efde21-de21-a0ef-21de-efa021deefa0",
  "enabled": true,
  "includedGroups": [
    "77c9d466-d466-77c9-66d4-c97766d4c977"
  ],
  "excludedGroups": [
    "2a0afae4-fae4-2a0a-e4fa-0a2ae4fa0a2a"
  ],
  "overrideDefaultRule": true
}
```



