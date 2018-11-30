---
title: Crear auditEvent
description: Cree un objeto auditEvent.
ms.openlocfilehash: b26b9fda355cda5b72133bc5257c0606a84de9a6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030563"
---
# <a name="create-auditevent"></a><span data-ttu-id="d8b24-103">Crear auditEvent</span><span class="sxs-lookup"><span data-stu-id="d8b24-103">Create auditEvent</span></span>

> <span data-ttu-id="d8b24-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d8b24-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d8b24-105">Cree un objeto [auditEvent](../resources/intune-auditing-auditevent.md).</span><span class="sxs-lookup"><span data-stu-id="d8b24-105">Create a new [auditEvent](../resources/intune-auditing-auditevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d8b24-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d8b24-106">Prerequisites</span></span>
<span data-ttu-id="d8b24-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d8b24-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d8b24-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d8b24-109">Permission type</span></span>|<span data-ttu-id="d8b24-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d8b24-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d8b24-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d8b24-111">Delegated (work or school account)</span></span>|<span data-ttu-id="d8b24-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d8b24-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="d8b24-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d8b24-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d8b24-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d8b24-114">Not supported.</span></span>|
|<span data-ttu-id="d8b24-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d8b24-115">Application</span></span>|<span data-ttu-id="d8b24-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d8b24-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d8b24-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d8b24-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/auditEvents
```

## <a name="request-headers"></a><span data-ttu-id="d8b24-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d8b24-118">Request headers</span></span>
|<span data-ttu-id="d8b24-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8b24-119">Header</span></span>|<span data-ttu-id="d8b24-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d8b24-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d8b24-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="d8b24-121">Authorization</span></span>|<span data-ttu-id="d8b24-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d8b24-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d8b24-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d8b24-123">Accept</span></span>|<span data-ttu-id="d8b24-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d8b24-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d8b24-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d8b24-125">Request body</span></span>
<span data-ttu-id="d8b24-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto auditEvent.</span><span class="sxs-lookup"><span data-stu-id="d8b24-126">In the request body, supply a JSON representation for the auditEvent object.</span></span>

<span data-ttu-id="d8b24-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto auditEvent.</span><span class="sxs-lookup"><span data-stu-id="d8b24-127">The following table shows the properties that are required when you create the auditEvent.</span></span>

|<span data-ttu-id="d8b24-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d8b24-128">Property</span></span>|<span data-ttu-id="d8b24-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="d8b24-129">Type</span></span>|<span data-ttu-id="d8b24-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8b24-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d8b24-131">id</span><span class="sxs-lookup"><span data-stu-id="d8b24-131">id</span></span>|<span data-ttu-id="d8b24-132">String</span><span class="sxs-lookup"><span data-stu-id="d8b24-132">String</span></span>|<span data-ttu-id="d8b24-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d8b24-133">Key of the entity.</span></span>|
|<span data-ttu-id="d8b24-134">displayName</span><span class="sxs-lookup"><span data-stu-id="d8b24-134">displayName</span></span>|<span data-ttu-id="d8b24-135">String</span><span class="sxs-lookup"><span data-stu-id="d8b24-135">String</span></span>|<span data-ttu-id="d8b24-136">Nombre para mostrar del evento.</span><span class="sxs-lookup"><span data-stu-id="d8b24-136">Event display name.</span></span>|
|<span data-ttu-id="d8b24-137">componentName</span><span class="sxs-lookup"><span data-stu-id="d8b24-137">componentName</span></span>|<span data-ttu-id="d8b24-138">String</span><span class="sxs-lookup"><span data-stu-id="d8b24-138">String</span></span>|<span data-ttu-id="d8b24-139">Nombre del componente.</span><span class="sxs-lookup"><span data-stu-id="d8b24-139">Component name.</span></span>|
|<span data-ttu-id="d8b24-140">actor</span><span class="sxs-lookup"><span data-stu-id="d8b24-140">actor</span></span>|[<span data-ttu-id="d8b24-141">auditActor</span><span class="sxs-lookup"><span data-stu-id="d8b24-141">auditActor</span></span>](../resources/intune-auditing-auditactor.md)|<span data-ttu-id="d8b24-142">Usuario y aplicación de AAD que están asociados al evento de auditoría.</span><span class="sxs-lookup"><span data-stu-id="d8b24-142">AAD user and application that are associated with the audit event.</span></span>|
|<span data-ttu-id="d8b24-143">actividad</span><span class="sxs-lookup"><span data-stu-id="d8b24-143">activity</span></span>|<span data-ttu-id="d8b24-144">String</span><span class="sxs-lookup"><span data-stu-id="d8b24-144">String</span></span>|<span data-ttu-id="d8b24-145">Nombre descriptivo de la actividad.</span><span class="sxs-lookup"><span data-stu-id="d8b24-145">Friendly name of the activity.</span></span>|
|<span data-ttu-id="d8b24-146">activityDateTime</span><span class="sxs-lookup"><span data-stu-id="d8b24-146">activityDateTime</span></span>|<span data-ttu-id="d8b24-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d8b24-147">DateTimeOffset</span></span>|<span data-ttu-id="d8b24-148">La fecha y hora en UTC a la que se realizó la actividad.</span><span class="sxs-lookup"><span data-stu-id="d8b24-148">The date time in UTC when the activity was performed.</span></span>|
|<span data-ttu-id="d8b24-149">activityType</span><span class="sxs-lookup"><span data-stu-id="d8b24-149">activityType</span></span>|<span data-ttu-id="d8b24-150">String</span><span class="sxs-lookup"><span data-stu-id="d8b24-150">String</span></span>|<span data-ttu-id="d8b24-151">El tipo de actividad que se realizó.</span><span class="sxs-lookup"><span data-stu-id="d8b24-151">The type of activity that was being performed.</span></span>|
|<span data-ttu-id="d8b24-152">activityOperationType</span><span class="sxs-lookup"><span data-stu-id="d8b24-152">activityOperationType</span></span>|<span data-ttu-id="d8b24-153">String</span><span class="sxs-lookup"><span data-stu-id="d8b24-153">String</span></span>|<span data-ttu-id="d8b24-154">El tipo de operación HTTP de la actividad.</span><span class="sxs-lookup"><span data-stu-id="d8b24-154">The HTTP operation type of the activity.</span></span>|
|<span data-ttu-id="d8b24-155">activityResult</span><span class="sxs-lookup"><span data-stu-id="d8b24-155">activityResult</span></span>|<span data-ttu-id="d8b24-156">String</span><span class="sxs-lookup"><span data-stu-id="d8b24-156">String</span></span>|<span data-ttu-id="d8b24-157">El resultado de la actividad.</span><span class="sxs-lookup"><span data-stu-id="d8b24-157">The result of the activity.</span></span>|
|<span data-ttu-id="d8b24-158">correlationId</span><span class="sxs-lookup"><span data-stu-id="d8b24-158">correlationId</span></span>|<span data-ttu-id="d8b24-159">Guid</span><span class="sxs-lookup"><span data-stu-id="d8b24-159">Guid</span></span>|<span data-ttu-id="d8b24-160">El identificador de la solicitud de cliente que se usa para correlacionar las actividades dentro del sistema.</span><span class="sxs-lookup"><span data-stu-id="d8b24-160">The client request Id that is used to correlate activity within the system.</span></span>|
|<span data-ttu-id="d8b24-161">recursos</span><span class="sxs-lookup"><span data-stu-id="d8b24-161">resources</span></span>|<span data-ttu-id="d8b24-162">Colección [auditResource](../resources/intune-auditing-auditresource.md)</span><span class="sxs-lookup"><span data-stu-id="d8b24-162">[auditResource](../resources/intune-auditing-auditresource.md) collection</span></span>|<span data-ttu-id="d8b24-163">Recursos que se están modificando.</span><span class="sxs-lookup"><span data-stu-id="d8b24-163">Resources being modified.</span></span>|
|<span data-ttu-id="d8b24-164">.</span><span class="sxs-lookup"><span data-stu-id="d8b24-164">category</span></span>|<span data-ttu-id="d8b24-165">String</span><span class="sxs-lookup"><span data-stu-id="d8b24-165">String</span></span>|<span data-ttu-id="d8b24-166">Categoría de auditoría.</span><span class="sxs-lookup"><span data-stu-id="d8b24-166">Audit category.</span></span>|



## <a name="response"></a><span data-ttu-id="d8b24-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d8b24-167">Response</span></span>
<span data-ttu-id="d8b24-168">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [auditEvent](../resources/intune-auditing-auditevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d8b24-168">If successful, this method returns a `201 Created` response code and a [auditEvent](../resources/intune-auditing-auditevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d8b24-169">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d8b24-169">Example</span></span>
### <a name="request"></a><span data-ttu-id="d8b24-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d8b24-170">Request</span></span>
<span data-ttu-id="d8b24-171">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d8b24-171">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="d8b24-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d8b24-172">Response</span></span>
<span data-ttu-id="d8b24-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d8b24-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



