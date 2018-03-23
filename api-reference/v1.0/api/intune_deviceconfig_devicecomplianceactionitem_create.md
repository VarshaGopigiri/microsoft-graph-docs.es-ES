# <a name="create-devicecomplianceactionitem"></a><span data-ttu-id="47f10-101">Crear deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="47f10-101">Create deviceComplianceActionItem</span></span>

> <span data-ttu-id="47f10-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="47f10-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="47f10-103">Cree un objeto [deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="47f10-103">Create a new [plannerBucket](../resources/intune_deviceconfig_devicecomplianceactionitem.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="47f10-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="47f10-104">Prerequisites</span></span>
<span data-ttu-id="47f10-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="47f10-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="47f10-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="47f10-107">Permission type</span></span>|<span data-ttu-id="47f10-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="47f10-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="47f10-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="47f10-109">Delegated (work or school account)</span></span>|<span data-ttu-id="47f10-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="47f10-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="47f10-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="47f10-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="47f10-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="47f10-112">Not supported.</span></span>|
|<span data-ttu-id="47f10-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="47f10-113">Application</span></span>|<span data-ttu-id="47f10-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="47f10-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="47f10-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="47f10-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}/scheduledActionConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="47f10-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="47f10-116">Request headers</span></span>
|<span data-ttu-id="47f10-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47f10-117">Header</span></span>|<span data-ttu-id="47f10-118">Valor</span><span class="sxs-lookup"><span data-stu-id="47f10-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="47f10-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="47f10-119">Authorization</span></span>|<span data-ttu-id="47f10-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="47f10-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="47f10-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="47f10-121">Accept</span></span>|<span data-ttu-id="47f10-122">application/json</span><span class="sxs-lookup"><span data-stu-id="47f10-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="47f10-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="47f10-123">Request body</span></span>
<span data-ttu-id="47f10-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceComplianceActionItem.</span><span class="sxs-lookup"><span data-stu-id="47f10-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="47f10-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceComplianceActionItem.</span><span class="sxs-lookup"><span data-stu-id="47f10-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="47f10-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="47f10-126">Property</span></span>|<span data-ttu-id="47f10-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="47f10-127">Type</span></span>|<span data-ttu-id="47f10-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="47f10-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="47f10-129">id</span><span class="sxs-lookup"><span data-stu-id="47f10-129">id</span></span>|<span data-ttu-id="47f10-130">String</span><span class="sxs-lookup"><span data-stu-id="47f10-130">String</span></span>|<span data-ttu-id="47f10-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="47f10-131">Key of the setting.</span></span>|
|<span data-ttu-id="47f10-132">gracePeriodHours</span><span class="sxs-lookup"><span data-stu-id="47f10-132">gracePeriodHours</span></span>|<span data-ttu-id="47f10-133">Int32</span><span class="sxs-lookup"><span data-stu-id="47f10-133">Int32</span></span>|<span data-ttu-id="47f10-134">Número de horas de espera hasta que se aplica la acción.</span><span class="sxs-lookup"><span data-stu-id="47f10-134">Number of hours to wait till the action will be enforced.</span></span> <span data-ttu-id="47f10-135">Valores válidos de 0 a 8760</span><span class="sxs-lookup"><span data-stu-id="47f10-135">Valid values 0 to 8760</span></span>|
|<span data-ttu-id="47f10-136">actionType</span><span class="sxs-lookup"><span data-stu-id="47f10-136">actionType</span></span>|<span data-ttu-id="47f10-137">String</span><span class="sxs-lookup"><span data-stu-id="47f10-137">String</span></span>|<span data-ttu-id="47f10-138">Qué acción tomar. Los valores posibles son: `noAction`, `notification`, `block`, `retire`, `wipe` y `removeResourceAccessProfiles`.</span><span class="sxs-lookup"><span data-stu-id="47f10-138">What action to take Possible values are: `noAction`, `notification`, `block`, `retire`, `wipe`, `removeResourceAccessProfiles`.</span></span>|
|<span data-ttu-id="47f10-139">notificationTemplateId</span><span class="sxs-lookup"><span data-stu-id="47f10-139">notificationTemplateId</span></span>|<span data-ttu-id="47f10-140">String</span><span class="sxs-lookup"><span data-stu-id="47f10-140">String</span></span>|<span data-ttu-id="47f10-141">Qué plantilla de mensaje de notificación usar</span><span class="sxs-lookup"><span data-stu-id="47f10-141">What notification Message template to use</span></span>|
|<span data-ttu-id="47f10-142">notificationMessageCCList</span><span class="sxs-lookup"><span data-stu-id="47f10-142">notificationMessageCCList</span></span>|<span data-ttu-id="47f10-143">Colección string</span><span class="sxs-lookup"><span data-stu-id="47f10-143">String collection</span></span>|<span data-ttu-id="47f10-144">Una lista de identificadores de grupo para especificar a quién enviar este mensaje de notificación.</span><span class="sxs-lookup"><span data-stu-id="47f10-144">A list of group IDs to speicify who to CC this notification message to.</span></span>|



## <a name="response"></a><span data-ttu-id="47f10-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="47f10-145">Response</span></span>
<span data-ttu-id="47f10-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="47f10-146">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_deviceconfig_devicecomplianceactionitem.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="47f10-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="47f10-147">Example</span></span>
### <a name="request"></a><span data-ttu-id="47f10-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="47f10-148">Request</span></span>
<span data-ttu-id="47f10-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="47f10-149">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}/scheduledActionConfigurations
Content-type: application/json
Content-length: 271

{
  "@odata.type": "#microsoft.graph.deviceComplianceActionItem",
  "gracePeriodHours": 0,
  "actionType": "notification",
  "notificationTemplateId": "Notification Template Id value",
  "notificationMessageCCList": [
    "Notification Message CCList value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="47f10-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="47f10-150">Response</span></span>
<span data-ttu-id="47f10-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="47f10-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



