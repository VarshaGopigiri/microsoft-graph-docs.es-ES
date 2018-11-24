# <a name="update-auditevent"></a><span data-ttu-id="0a108-101">Actualizar auditEvent</span><span class="sxs-lookup"><span data-stu-id="0a108-101">Update auditEvent</span></span>

> <span data-ttu-id="0a108-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0a108-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0a108-103">Actualice las propiedades de un objeto [auditEvent](../resources/intune_auditing_auditevent.md).</span><span class="sxs-lookup"><span data-stu-id="0a108-103">Update the properties of a [auditEvent](../resources/intune_auditing_auditevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0a108-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0a108-104">Prerequisites</span></span>
<span data-ttu-id="0a108-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0a108-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="0a108-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0a108-107">Permission type</span></span>|<span data-ttu-id="0a108-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0a108-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0a108-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0a108-109">Delegated (work or school account)</span></span>|<span data-ttu-id="0a108-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0a108-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="0a108-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0a108-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0a108-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0a108-112">Not supported.</span></span>|
|<span data-ttu-id="0a108-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0a108-113">Application</span></span>|<span data-ttu-id="0a108-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0a108-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0a108-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0a108-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/auditEvents/{auditEventId}
```

## <a name="request-headers"></a><span data-ttu-id="0a108-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0a108-116">Request headers</span></span>
|<span data-ttu-id="0a108-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a108-117">Header</span></span>|<span data-ttu-id="0a108-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0a108-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0a108-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="0a108-119">Authorization</span></span>|<span data-ttu-id="0a108-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0a108-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0a108-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0a108-121">Accept</span></span>|<span data-ttu-id="0a108-122">application/json</span><span class="sxs-lookup"><span data-stu-id="0a108-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0a108-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0a108-123">Request body</span></span>
<span data-ttu-id="0a108-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [auditEvent](../resources/intune_auditing_auditevent.md).</span><span class="sxs-lookup"><span data-stu-id="0a108-124">In the request body, supply a JSON representation for the [auditEvent](../resources/intune_auditing_auditevent.md) object.</span></span>

<span data-ttu-id="0a108-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [auditEvent](../resources/intune_auditing_auditevent.md).</span><span class="sxs-lookup"><span data-stu-id="0a108-125">The following table shows the properties that are required when you create the [auditEvent](../resources/intune_auditing_auditevent.md).</span></span>

|<span data-ttu-id="0a108-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0a108-126">Property</span></span>|<span data-ttu-id="0a108-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="0a108-127">Type</span></span>|<span data-ttu-id="0a108-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a108-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0a108-129">id</span><span class="sxs-lookup"><span data-stu-id="0a108-129">id</span></span>|<span data-ttu-id="0a108-130">String</span><span class="sxs-lookup"><span data-stu-id="0a108-130">String</span></span>|<span data-ttu-id="0a108-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="0a108-131">Key of the entity.</span></span>|
|<span data-ttu-id="0a108-132">displayName</span><span class="sxs-lookup"><span data-stu-id="0a108-132">displayName</span></span>|<span data-ttu-id="0a108-133">String</span><span class="sxs-lookup"><span data-stu-id="0a108-133">String</span></span>|<span data-ttu-id="0a108-134">Nombre para mostrar del evento.</span><span class="sxs-lookup"><span data-stu-id="0a108-134">Event display name.</span></span>|
|<span data-ttu-id="0a108-135">componentName</span><span class="sxs-lookup"><span data-stu-id="0a108-135">componentName</span></span>|<span data-ttu-id="0a108-136">String</span><span class="sxs-lookup"><span data-stu-id="0a108-136">String</span></span>|<span data-ttu-id="0a108-137">Nombre del componente.</span><span class="sxs-lookup"><span data-stu-id="0a108-137">Component name.</span></span>|
|<span data-ttu-id="0a108-138">actor</span><span class="sxs-lookup"><span data-stu-id="0a108-138">actor</span></span>|[<span data-ttu-id="0a108-139">auditActor</span><span class="sxs-lookup"><span data-stu-id="0a108-139">auditActor</span></span>](../resources/intune_auditing_auditactor.md)|<span data-ttu-id="0a108-140">Usuario y aplicación de AAD que están asociados al evento de auditoría.</span><span class="sxs-lookup"><span data-stu-id="0a108-140">AAD user and application that are associated with the audit event.</span></span>|
|<span data-ttu-id="0a108-141">actividad</span><span class="sxs-lookup"><span data-stu-id="0a108-141">activity</span></span>|<span data-ttu-id="0a108-142">String</span><span class="sxs-lookup"><span data-stu-id="0a108-142">String</span></span>|<span data-ttu-id="0a108-143">Nombre descriptivo de la actividad.</span><span class="sxs-lookup"><span data-stu-id="0a108-143">Friendly name of the activity.</span></span>|
|<span data-ttu-id="0a108-144">activityDateTime</span><span class="sxs-lookup"><span data-stu-id="0a108-144">activityDateTime</span></span>|<span data-ttu-id="0a108-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0a108-145">DateTimeOffset</span></span>|<span data-ttu-id="0a108-146">La fecha y hora en UTC a la que se realizó la actividad.</span><span class="sxs-lookup"><span data-stu-id="0a108-146">The date time in UTC when the activity was performed.</span></span>|
|<span data-ttu-id="0a108-147">activityType</span><span class="sxs-lookup"><span data-stu-id="0a108-147">activityType</span></span>|<span data-ttu-id="0a108-148">String</span><span class="sxs-lookup"><span data-stu-id="0a108-148">String</span></span>|<span data-ttu-id="0a108-149">El tipo de actividad que se realizó.</span><span class="sxs-lookup"><span data-stu-id="0a108-149">The type of activity that was being performed.</span></span>|
|<span data-ttu-id="0a108-150">activityOperationType</span><span class="sxs-lookup"><span data-stu-id="0a108-150">activityOperationType</span></span>|<span data-ttu-id="0a108-151">String</span><span class="sxs-lookup"><span data-stu-id="0a108-151">String</span></span>|<span data-ttu-id="0a108-152">El tipo de operación HTTP de la actividad.</span><span class="sxs-lookup"><span data-stu-id="0a108-152">The HTTP operation type of the activity.</span></span>|
|<span data-ttu-id="0a108-153">activityResult</span><span class="sxs-lookup"><span data-stu-id="0a108-153">activityResult</span></span>|<span data-ttu-id="0a108-154">String</span><span class="sxs-lookup"><span data-stu-id="0a108-154">String</span></span>|<span data-ttu-id="0a108-155">El resultado de la actividad.</span><span class="sxs-lookup"><span data-stu-id="0a108-155">The result of the activity.</span></span>|
|<span data-ttu-id="0a108-156">correlationId</span><span class="sxs-lookup"><span data-stu-id="0a108-156">correlationId</span></span>|<span data-ttu-id="0a108-157">Guid</span><span class="sxs-lookup"><span data-stu-id="0a108-157">Guid</span></span>|<span data-ttu-id="0a108-158">El identificador de la solicitud de cliente que se usa para correlacionar las actividades dentro del sistema.</span><span class="sxs-lookup"><span data-stu-id="0a108-158">The client request Id that is used to correlate activity within the system.</span></span>|
|<span data-ttu-id="0a108-159">recursos</span><span class="sxs-lookup"><span data-stu-id="0a108-159">resources</span></span>|<span data-ttu-id="0a108-160">Colección [auditResource](../resources/intune_auditing_auditresource.md)</span><span class="sxs-lookup"><span data-stu-id="0a108-160">[auditResource](../resources/intune_auditing_auditresource.md) collection</span></span>|<span data-ttu-id="0a108-161">Recursos que se están modificando.</span><span class="sxs-lookup"><span data-stu-id="0a108-161">Resources being modified.</span></span>|
|<span data-ttu-id="0a108-162">.</span><span class="sxs-lookup"><span data-stu-id="0a108-162">category</span></span>|<span data-ttu-id="0a108-163">String</span><span class="sxs-lookup"><span data-stu-id="0a108-163">String</span></span>|<span data-ttu-id="0a108-164">Categoría de auditoría.</span><span class="sxs-lookup"><span data-stu-id="0a108-164">Audit category.</span></span>|



## <a name="response"></a><span data-ttu-id="0a108-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0a108-165">Response</span></span>
<span data-ttu-id="0a108-166">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [auditEvent](../resources/intune_auditing_auditevent.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0a108-166">If successful, this method returns a `200 OK` response code and an updated [auditEvent](../resources/intune_auditing_auditevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0a108-167">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0a108-167">Example</span></span>
### <a name="request"></a><span data-ttu-id="0a108-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0a108-168">Request</span></span>
<span data-ttu-id="0a108-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0a108-169">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/auditEvents/{auditEventId}
Content-type: application/json
Content-length: 1390

{
  "@odata.type": "#microsoft.graph.auditEvent",
  "displayName": "Display Name value",
  "componentName": "Component Name value",
  "actor": {
    "@odata.type": "microsoft.graph.auditActor",
    "type": "Type value",
    "userPermissions": [
      "User Permissions value"
    ],
    "applicationId": "Application Id value",
    "applicationDisplayName": "Application Display Name value",
    "userPrincipalName": "User Principal Name value",
    "servicePrincipalName": "Service Principal Name value",
    "ipAddress": "Ip Address value",
    "userId": "User Id value"
  },
  "activity": "Activity value",
  "activityDateTime": "2016-12-31T23:59:51.6363086-08:00",
  "activityType": "Activity Type value",
  "activityOperationType": "Activity Operation Type value",
  "activityResult": "Activity Result value",
  "correlationId": "52effe71-fe71-52ef-71fe-ef5271feef52",
  "resources": [
    {
      "@odata.type": "microsoft.graph.auditResource",
      "displayName": "Display Name value",
      "modifiedProperties": [
        {
          "@odata.type": "microsoft.graph.auditProperty",
          "displayName": "Display Name value",
          "oldValue": "Old Value value",
          "newValue": "New Value value"
        }
      ],
      "type": "Type value",
      "resourceId": "Resource Id value"
    }
  ],
  "category": "Category value"
}
```

### <a name="response"></a><span data-ttu-id="0a108-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0a108-170">Response</span></span>
<span data-ttu-id="0a108-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0a108-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1439

{
  "@odata.type": "#microsoft.graph.auditEvent",
  "id": "59653ce8-3ce8-5965-e83c-6559e83c6559",
  "displayName": "Display Name value",
  "componentName": "Component Name value",
  "actor": {
    "@odata.type": "microsoft.graph.auditActor",
    "type": "Type value",
    "userPermissions": [
      "User Permissions value"
    ],
    "applicationId": "Application Id value",
    "applicationDisplayName": "Application Display Name value",
    "userPrincipalName": "User Principal Name value",
    "servicePrincipalName": "Service Principal Name value",
    "ipAddress": "Ip Address value",
    "userId": "User Id value"
  },
  "activity": "Activity value",
  "activityDateTime": "2016-12-31T23:59:51.6363086-08:00",
  "activityType": "Activity Type value",
  "activityOperationType": "Activity Operation Type value",
  "activityResult": "Activity Result value",
  "correlationId": "52effe71-fe71-52ef-71fe-ef5271feef52",
  "resources": [
    {
      "@odata.type": "microsoft.graph.auditResource",
      "displayName": "Display Name value",
      "modifiedProperties": [
        {
          "@odata.type": "microsoft.graph.auditProperty",
          "displayName": "Display Name value",
          "oldValue": "Old Value value",
          "newValue": "New Value value"
        }
      ],
      "type": "Type value",
      "resourceId": "Resource Id value"
    }
  ],
  "category": "Category value"
}
```



