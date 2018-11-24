# <a name="create-auditevent"></a><span data-ttu-id="d7761-101">Crear auditEvent</span><span class="sxs-lookup"><span data-stu-id="d7761-101">Create auditEvent</span></span>

> <span data-ttu-id="d7761-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d7761-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d7761-103">Cree un objeto [auditEvent](../resources/intune_auditing_auditevent.md).</span><span class="sxs-lookup"><span data-stu-id="d7761-103">Create a new [auditEvent](../resources/intune_auditing_auditevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d7761-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d7761-104">Prerequisites</span></span>
<span data-ttu-id="d7761-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d7761-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d7761-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d7761-107">Permission type</span></span>|<span data-ttu-id="d7761-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d7761-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d7761-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d7761-109">Delegated (work or school account)</span></span>|<span data-ttu-id="d7761-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d7761-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="d7761-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d7761-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d7761-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d7761-112">Not supported.</span></span>|
|<span data-ttu-id="d7761-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d7761-113">Application</span></span>|<span data-ttu-id="d7761-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d7761-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d7761-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d7761-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/auditEvents
```

## <a name="request-headers"></a><span data-ttu-id="d7761-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d7761-116">Request headers</span></span>
|<span data-ttu-id="d7761-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7761-117">Header</span></span>|<span data-ttu-id="d7761-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d7761-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d7761-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="d7761-119">Authorization</span></span>|<span data-ttu-id="d7761-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d7761-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d7761-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d7761-121">Accept</span></span>|<span data-ttu-id="d7761-122">application/json</span><span class="sxs-lookup"><span data-stu-id="d7761-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d7761-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d7761-123">Request body</span></span>
<span data-ttu-id="d7761-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto auditEvent.</span><span class="sxs-lookup"><span data-stu-id="d7761-124">In the request body, supply a JSON representation for the auditEvent object.</span></span>

<span data-ttu-id="d7761-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto auditEvent.</span><span class="sxs-lookup"><span data-stu-id="d7761-125">The following table shows the properties that are required when you create the auditEvent.</span></span>

|<span data-ttu-id="d7761-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d7761-126">Property</span></span>|<span data-ttu-id="d7761-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="d7761-127">Type</span></span>|<span data-ttu-id="d7761-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7761-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d7761-129">id</span><span class="sxs-lookup"><span data-stu-id="d7761-129">id</span></span>|<span data-ttu-id="d7761-130">String</span><span class="sxs-lookup"><span data-stu-id="d7761-130">String</span></span>|<span data-ttu-id="d7761-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d7761-131">Key of the entity.</span></span>|
|<span data-ttu-id="d7761-132">displayName</span><span class="sxs-lookup"><span data-stu-id="d7761-132">displayName</span></span>|<span data-ttu-id="d7761-133">String</span><span class="sxs-lookup"><span data-stu-id="d7761-133">String</span></span>|<span data-ttu-id="d7761-134">Nombre para mostrar del evento.</span><span class="sxs-lookup"><span data-stu-id="d7761-134">Event display name.</span></span>|
|<span data-ttu-id="d7761-135">componentName</span><span class="sxs-lookup"><span data-stu-id="d7761-135">componentName</span></span>|<span data-ttu-id="d7761-136">String</span><span class="sxs-lookup"><span data-stu-id="d7761-136">String</span></span>|<span data-ttu-id="d7761-137">Nombre del componente.</span><span class="sxs-lookup"><span data-stu-id="d7761-137">Component name.</span></span>|
|<span data-ttu-id="d7761-138">actor</span><span class="sxs-lookup"><span data-stu-id="d7761-138">actor</span></span>|[<span data-ttu-id="d7761-139">auditActor</span><span class="sxs-lookup"><span data-stu-id="d7761-139">auditActor</span></span>](../resources/intune_auditing_auditactor.md)|<span data-ttu-id="d7761-140">Usuario y aplicación de AAD que están asociados al evento de auditoría.</span><span class="sxs-lookup"><span data-stu-id="d7761-140">AAD user and application that are associated with the audit event.</span></span>|
|<span data-ttu-id="d7761-141">actividad</span><span class="sxs-lookup"><span data-stu-id="d7761-141">activity</span></span>|<span data-ttu-id="d7761-142">String</span><span class="sxs-lookup"><span data-stu-id="d7761-142">String</span></span>|<span data-ttu-id="d7761-143">Nombre descriptivo de la actividad.</span><span class="sxs-lookup"><span data-stu-id="d7761-143">Friendly name of the activity.</span></span>|
|<span data-ttu-id="d7761-144">activityDateTime</span><span class="sxs-lookup"><span data-stu-id="d7761-144">activityDateTime</span></span>|<span data-ttu-id="d7761-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d7761-145">DateTimeOffset</span></span>|<span data-ttu-id="d7761-146">La fecha y hora en UTC a la que se realizó la actividad.</span><span class="sxs-lookup"><span data-stu-id="d7761-146">The date time in UTC when the activity was performed.</span></span>|
|<span data-ttu-id="d7761-147">activityType</span><span class="sxs-lookup"><span data-stu-id="d7761-147">activityType</span></span>|<span data-ttu-id="d7761-148">String</span><span class="sxs-lookup"><span data-stu-id="d7761-148">String</span></span>|<span data-ttu-id="d7761-149">El tipo de actividad que se realizó.</span><span class="sxs-lookup"><span data-stu-id="d7761-149">The type of activity that was being performed.</span></span>|
|<span data-ttu-id="d7761-150">activityOperationType</span><span class="sxs-lookup"><span data-stu-id="d7761-150">activityOperationType</span></span>|<span data-ttu-id="d7761-151">String</span><span class="sxs-lookup"><span data-stu-id="d7761-151">String</span></span>|<span data-ttu-id="d7761-152">El tipo de operación HTTP de la actividad.</span><span class="sxs-lookup"><span data-stu-id="d7761-152">The HTTP operation type of the activity.</span></span>|
|<span data-ttu-id="d7761-153">activityResult</span><span class="sxs-lookup"><span data-stu-id="d7761-153">activityResult</span></span>|<span data-ttu-id="d7761-154">String</span><span class="sxs-lookup"><span data-stu-id="d7761-154">String</span></span>|<span data-ttu-id="d7761-155">El resultado de la actividad.</span><span class="sxs-lookup"><span data-stu-id="d7761-155">The result of the activity.</span></span>|
|<span data-ttu-id="d7761-156">correlationId</span><span class="sxs-lookup"><span data-stu-id="d7761-156">correlationId</span></span>|<span data-ttu-id="d7761-157">Guid</span><span class="sxs-lookup"><span data-stu-id="d7761-157">Guid</span></span>|<span data-ttu-id="d7761-158">El identificador de la solicitud de cliente que se usa para correlacionar las actividades dentro del sistema.</span><span class="sxs-lookup"><span data-stu-id="d7761-158">The client request Id that is used to correlate activity within the system.</span></span>|
|<span data-ttu-id="d7761-159">recursos</span><span class="sxs-lookup"><span data-stu-id="d7761-159">resources</span></span>|<span data-ttu-id="d7761-160">Colección [auditResource](../resources/intune_auditing_auditresource.md)</span><span class="sxs-lookup"><span data-stu-id="d7761-160">[auditResource](../resources/intune_auditing_auditresource.md) collection</span></span>|<span data-ttu-id="d7761-161">Recursos que se están modificando.</span><span class="sxs-lookup"><span data-stu-id="d7761-161">Resources being modified.</span></span>|
|<span data-ttu-id="d7761-162">categoría</span><span class="sxs-lookup"><span data-stu-id="d7761-162">category</span></span>|<span data-ttu-id="d7761-163">String</span><span class="sxs-lookup"><span data-stu-id="d7761-163">String</span></span>|<span data-ttu-id="d7761-164">Categoría de auditoría.</span><span class="sxs-lookup"><span data-stu-id="d7761-164">Audit category.</span></span>|



## <a name="response"></a><span data-ttu-id="d7761-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7761-165">Response</span></span>
<span data-ttu-id="d7761-166">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [auditEvent](../resources/intune_auditing_auditevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d7761-166">If successful, this method returns a `201 Created` response code and a [auditEvent](../resources/intune_auditing_auditevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d7761-167">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d7761-167">Example</span></span>
### <a name="request"></a><span data-ttu-id="d7761-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d7761-168">Request</span></span>
<span data-ttu-id="d7761-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d7761-169">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/auditEvents
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

### <a name="response"></a><span data-ttu-id="d7761-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7761-170">Response</span></span>
<span data-ttu-id="d7761-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d7761-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



