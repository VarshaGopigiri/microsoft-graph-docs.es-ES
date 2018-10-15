# <a name="update-devicecomplianceactionitem"></a><span data-ttu-id="605c6-101">Actualizar deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="605c6-101">Update deviceComplianceActionItem</span></span>

> <span data-ttu-id="605c6-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="605c6-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="605c6-103">Actualice las propiedades de un objeto [deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="605c6-103">Update the properties of a [deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="605c6-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="605c6-104">Prerequisites</span></span>
<span data-ttu-id="605c6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="605c6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="605c6-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="605c6-107">Permission type</span></span>|<span data-ttu-id="605c6-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="605c6-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="605c6-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="605c6-109">Delegated (work or school account)</span></span>|<span data-ttu-id="605c6-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="605c6-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="605c6-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="605c6-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="605c6-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="605c6-112">Not supported.</span></span>|
|<span data-ttu-id="605c6-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="605c6-113">Application</span></span>|<span data-ttu-id="605c6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="605c6-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="605c6-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="605c6-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}/scheduledActionConfigurations/{deviceComplianceActionItemId}
```

## <a name="request-headers"></a><span data-ttu-id="605c6-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="605c6-116">Request headers</span></span>
|<span data-ttu-id="605c6-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="605c6-117">Header</span></span>|<span data-ttu-id="605c6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="605c6-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="605c6-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="605c6-119">Authorization</span></span>|<span data-ttu-id="605c6-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="605c6-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="605c6-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="605c6-121">Accept</span></span>|<span data-ttu-id="605c6-122">aplicación/json</span><span class="sxs-lookup"><span data-stu-id="605c6-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="605c6-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="605c6-123">Request body</span></span>
<span data-ttu-id="605c6-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="605c6-124">In the request body, supply a JSON representation for the [deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md) object.</span></span>

<span data-ttu-id="605c6-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="605c6-125">The following table shows the properties that are required when you create the [deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md).</span></span>

|<span data-ttu-id="605c6-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="605c6-126">Property</span></span>|<span data-ttu-id="605c6-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="605c6-127">Type</span></span>|<span data-ttu-id="605c6-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="605c6-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="605c6-129">id.</span><span class="sxs-lookup"><span data-stu-id="605c6-129">id</span></span>|<span data-ttu-id="605c6-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="605c6-130">String</span></span>|<span data-ttu-id="605c6-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="605c6-131">Key of the entity.</span></span>|
|<span data-ttu-id="605c6-132">gracePeriodHours</span><span class="sxs-lookup"><span data-stu-id="605c6-132">gracePeriodHours</span></span>|<span data-ttu-id="605c6-133">Int32</span><span class="sxs-lookup"><span data-stu-id="605c6-133">Int32</span></span>|<span data-ttu-id="605c6-134">Número de horas de espera hasta que se aplica la acción.</span><span class="sxs-lookup"><span data-stu-id="605c6-134">Number of hours to wait till the action will be enforced.</span></span> <span data-ttu-id="605c6-135">Valores válidos de 0 a 8760</span><span class="sxs-lookup"><span data-stu-id="605c6-135">Valid values 0 to 8760</span></span>|
|<span data-ttu-id="605c6-136">actionType</span><span class="sxs-lookup"><span data-stu-id="605c6-136">actionType</span></span>|[<span data-ttu-id="605c6-137">deviceComplianceActionType</span><span class="sxs-lookup"><span data-stu-id="605c6-137">deviceComplianceActionType</span></span>](../resources/intune_deviceconfig_devicecomplianceactiontype.md)|<span data-ttu-id="605c6-p103">Qué acción realizar. Los valores posibles son: `noAction`, `notification`, `block`, `retire`, `wipe`, `removeResourceAccessProfiles`, `pushNotification`.</span><span class="sxs-lookup"><span data-stu-id="605c6-p103">What action to take Possible values are: `noAction`, `notification`, `block`, `retire`, `wipe`, `removeResourceAccessProfiles`.</span></span>|
|<span data-ttu-id="605c6-140">notificationTemplateId</span><span class="sxs-lookup"><span data-stu-id="605c6-140">notificationTemplateId</span></span>|<span data-ttu-id="605c6-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="605c6-141">String</span></span>|<span data-ttu-id="605c6-142">Qué plantilla de mensaje de notificación usar</span><span class="sxs-lookup"><span data-stu-id="605c6-142">What notification Message template to use</span></span>|
|<span data-ttu-id="605c6-143">notificationMessageCCList</span><span class="sxs-lookup"><span data-stu-id="605c6-143">notificationMessageCCList</span></span>|<span data-ttu-id="605c6-144">Colección string</span><span class="sxs-lookup"><span data-stu-id="605c6-144">String collection</span></span>|<span data-ttu-id="605c6-145">Una lista de identificadores de grupo para especificar a quién enviar este mensaje de notificación.</span><span class="sxs-lookup"><span data-stu-id="605c6-145">A list of group IDs to speicify who to CC this notification message to.</span></span>|



## <a name="response"></a><span data-ttu-id="605c6-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="605c6-146">Response</span></span>
<span data-ttu-id="605c6-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="605c6-147">If successful, this method returns a `200 OK` response code and an updated [deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="605c6-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="605c6-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="605c6-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="605c6-149">Request</span></span>
<span data-ttu-id="605c6-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="605c6-150">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}/scheduledActionConfigurations/{deviceComplianceActionItemId}
Content-type: application/json
Content-length: 206

{
  "gracePeriodHours": 0,
  "actionType": "notification",
  "notificationTemplateId": "Notification Template Id value",
  "notificationMessageCCList": [
    "Notification Message CCList value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="605c6-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="605c6-151">Response</span></span>
<span data-ttu-id="605c6-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="605c6-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 320

{
  "@odata.type": "#microsoft.graph.deviceComplianceActionItem",
  "id": "e01a1893-1893-e01a-9318-1ae093181ae0",
  "gracePeriodHours": 0,
  "actionType": "notification",
  "notificationTemplateId": "Notification Template Id value",
  "notificationMessageCCList": [
    "Notification Message CCList value"
  ]
}
```








