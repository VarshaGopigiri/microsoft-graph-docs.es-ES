---
title: Actualizar auditEvent
description: Actualice las propiedades de un objeto auditEvent.
ms.openlocfilehash: 1a1de92517b59d168147feafe16fe2479b8afc2b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089526"
---
# <a name="update-auditevent"></a><span data-ttu-id="59eba-103">Actualizar auditEvent</span><span class="sxs-lookup"><span data-stu-id="59eba-103">Update auditEvent</span></span>

> <span data-ttu-id="59eba-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="59eba-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="59eba-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="59eba-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="59eba-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="59eba-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="59eba-107">Actualice las propiedades de un objeto [auditEvent](../resources/intune-auditing-auditevent.md).</span><span class="sxs-lookup"><span data-stu-id="59eba-107">Update the properties of a [auditEvent](../resources/intune-auditing-auditevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="59eba-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="59eba-108">Prerequisites</span></span>
<span data-ttu-id="59eba-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="59eba-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="59eba-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="59eba-111">Permission type</span></span>|<span data-ttu-id="59eba-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="59eba-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="59eba-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="59eba-113">Delegated (work or school account)</span></span>|<span data-ttu-id="59eba-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="59eba-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="59eba-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="59eba-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="59eba-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="59eba-116">Not supported.</span></span>|
|<span data-ttu-id="59eba-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="59eba-117">Application</span></span>|<span data-ttu-id="59eba-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="59eba-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="59eba-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="59eba-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/auditEvents/{auditEventId}
```

## <a name="request-headers"></a><span data-ttu-id="59eba-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="59eba-120">Request headers</span></span>
|<span data-ttu-id="59eba-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59eba-121">Header</span></span>|<span data-ttu-id="59eba-122">Valor</span><span class="sxs-lookup"><span data-stu-id="59eba-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="59eba-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="59eba-123">Authorization</span></span>|<span data-ttu-id="59eba-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="59eba-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="59eba-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="59eba-125">Accept</span></span>|<span data-ttu-id="59eba-126">application/json</span><span class="sxs-lookup"><span data-stu-id="59eba-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="59eba-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="59eba-127">Request body</span></span>
<span data-ttu-id="59eba-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [auditEvent](../resources/intune-auditing-auditevent.md).</span><span class="sxs-lookup"><span data-stu-id="59eba-128">In the request body, supply a JSON representation for the [auditEvent](../resources/intune-auditing-auditevent.md) object.</span></span>

<span data-ttu-id="59eba-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [auditEvent](../resources/intune-auditing-auditevent.md).</span><span class="sxs-lookup"><span data-stu-id="59eba-129">The following table shows the properties that are required when you create the [auditEvent](../resources/intune-auditing-auditevent.md).</span></span>

|<span data-ttu-id="59eba-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="59eba-130">Property</span></span>|<span data-ttu-id="59eba-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="59eba-131">Type</span></span>|<span data-ttu-id="59eba-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="59eba-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="59eba-133">id</span><span class="sxs-lookup"><span data-stu-id="59eba-133">id</span></span>|<span data-ttu-id="59eba-134">String</span><span class="sxs-lookup"><span data-stu-id="59eba-134">String</span></span>|<span data-ttu-id="59eba-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="59eba-135">Key of the entity.</span></span>|
|<span data-ttu-id="59eba-136">displayName</span><span class="sxs-lookup"><span data-stu-id="59eba-136">displayName</span></span>|<span data-ttu-id="59eba-137">String</span><span class="sxs-lookup"><span data-stu-id="59eba-137">String</span></span>|<span data-ttu-id="59eba-138">Nombre para mostrar del evento.</span><span class="sxs-lookup"><span data-stu-id="59eba-138">Event display name.</span></span>|
|<span data-ttu-id="59eba-139">componentName</span><span class="sxs-lookup"><span data-stu-id="59eba-139">componentName</span></span>|<span data-ttu-id="59eba-140">String</span><span class="sxs-lookup"><span data-stu-id="59eba-140">String</span></span>|<span data-ttu-id="59eba-141">Nombre del componente.</span><span class="sxs-lookup"><span data-stu-id="59eba-141">Component name.</span></span>|
|<span data-ttu-id="59eba-142">actor</span><span class="sxs-lookup"><span data-stu-id="59eba-142">actor</span></span>|[<span data-ttu-id="59eba-143">auditActor</span><span class="sxs-lookup"><span data-stu-id="59eba-143">auditActor</span></span>](../resources/intune-auditing-auditactor.md)|<span data-ttu-id="59eba-144">Usuario y aplicación de AAD que están asociados al evento de auditoría.</span><span class="sxs-lookup"><span data-stu-id="59eba-144">AAD user and application that are associated with the audit event.</span></span>|
|<span data-ttu-id="59eba-145">actividad</span><span class="sxs-lookup"><span data-stu-id="59eba-145">activity</span></span>|<span data-ttu-id="59eba-146">String</span><span class="sxs-lookup"><span data-stu-id="59eba-146">String</span></span>|<span data-ttu-id="59eba-147">Nombre descriptivo de la actividad.</span><span class="sxs-lookup"><span data-stu-id="59eba-147">Friendly name of the activity.</span></span>|
|<span data-ttu-id="59eba-148">activityDateTime</span><span class="sxs-lookup"><span data-stu-id="59eba-148">activityDateTime</span></span>|<span data-ttu-id="59eba-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="59eba-149">DateTimeOffset</span></span>|<span data-ttu-id="59eba-150">La fecha y hora en UTC a la que se realizó la actividad.</span><span class="sxs-lookup"><span data-stu-id="59eba-150">The date time in UTC when the activity was performed.</span></span>|
|<span data-ttu-id="59eba-151">activityType</span><span class="sxs-lookup"><span data-stu-id="59eba-151">activityType</span></span>|<span data-ttu-id="59eba-152">String</span><span class="sxs-lookup"><span data-stu-id="59eba-152">String</span></span>|<span data-ttu-id="59eba-153">El tipo de actividad que se realizó.</span><span class="sxs-lookup"><span data-stu-id="59eba-153">The type of activity that was being performed.</span></span>|
|<span data-ttu-id="59eba-154">activityOperationType</span><span class="sxs-lookup"><span data-stu-id="59eba-154">activityOperationType</span></span>|<span data-ttu-id="59eba-155">String</span><span class="sxs-lookup"><span data-stu-id="59eba-155">String</span></span>|<span data-ttu-id="59eba-156">El tipo de operación HTTP de la actividad.</span><span class="sxs-lookup"><span data-stu-id="59eba-156">The HTTP operation type of the activity.</span></span>|
|<span data-ttu-id="59eba-157">activityResult</span><span class="sxs-lookup"><span data-stu-id="59eba-157">activityResult</span></span>|<span data-ttu-id="59eba-158">String</span><span class="sxs-lookup"><span data-stu-id="59eba-158">String</span></span>|<span data-ttu-id="59eba-159">El resultado de la actividad.</span><span class="sxs-lookup"><span data-stu-id="59eba-159">The result of the activity.</span></span>|
|<span data-ttu-id="59eba-160">correlationId</span><span class="sxs-lookup"><span data-stu-id="59eba-160">correlationId</span></span>|<span data-ttu-id="59eba-161">Guid</span><span class="sxs-lookup"><span data-stu-id="59eba-161">Guid</span></span>|<span data-ttu-id="59eba-162">El identificador de la solicitud de cliente que se usa para correlacionar las actividades dentro del sistema.</span><span class="sxs-lookup"><span data-stu-id="59eba-162">The client request Id that is used to correlate activity within the system.</span></span>|
|<span data-ttu-id="59eba-163">recursos</span><span class="sxs-lookup"><span data-stu-id="59eba-163">resources</span></span>|<span data-ttu-id="59eba-164">Colección [auditResource](../resources/intune-auditing-auditresource.md)</span><span class="sxs-lookup"><span data-stu-id="59eba-164">[auditResource](../resources/intune-auditing-auditresource.md) collection</span></span>|<span data-ttu-id="59eba-165">Recursos que se están modificando.</span><span class="sxs-lookup"><span data-stu-id="59eba-165">Resources being modified.</span></span>|
|<span data-ttu-id="59eba-166">.</span><span class="sxs-lookup"><span data-stu-id="59eba-166">category</span></span>|<span data-ttu-id="59eba-167">String</span><span class="sxs-lookup"><span data-stu-id="59eba-167">String</span></span>|<span data-ttu-id="59eba-168">Categoría de auditoría.</span><span class="sxs-lookup"><span data-stu-id="59eba-168">Audit category.</span></span>|



## <a name="response"></a><span data-ttu-id="59eba-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59eba-169">Response</span></span>
<span data-ttu-id="59eba-170">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [auditEvent](../resources/intune-auditing-auditevent.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="59eba-170">If successful, this method returns a `200 OK` response code and an updated [auditEvent](../resources/intune-auditing-auditevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="59eba-171">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="59eba-171">Example</span></span>
### <a name="request"></a><span data-ttu-id="59eba-172">Solicitud</span><span class="sxs-lookup"><span data-stu-id="59eba-172">Request</span></span>
<span data-ttu-id="59eba-173">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="59eba-173">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/auditEvents/{auditEventId}
Content-type: application/json
Content-length: 1341

{
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

### <a name="response"></a><span data-ttu-id="59eba-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59eba-174">Response</span></span>
<span data-ttu-id="59eba-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="59eba-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





