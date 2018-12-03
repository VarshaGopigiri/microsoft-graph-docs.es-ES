---
title: Actualizar deviceComplianceActionItem
description: Actualice las propiedades de un objeto deviceComplianceActionItem.
ms.openlocfilehash: 0f2d94411c88bf4e7d377150ebd59d3056b1f6c7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084273"
---
# <a name="update-devicecomplianceactionitem"></a><span data-ttu-id="6ae7d-103">Actualizar deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="6ae7d-103">Update deviceComplianceActionItem</span></span>

> <span data-ttu-id="6ae7d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6ae7d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6ae7d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6ae7d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6ae7d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6ae7d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6ae7d-107">Actualice las propiedades de un objeto [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="6ae7d-107">Update the properties of a [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6ae7d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6ae7d-108">Prerequisites</span></span>
<span data-ttu-id="6ae7d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6ae7d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6ae7d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6ae7d-111">Permission type</span></span>|<span data-ttu-id="6ae7d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6ae7d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6ae7d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6ae7d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="6ae7d-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6ae7d-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="6ae7d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6ae7d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6ae7d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ae7d-116">Not supported.</span></span>|
|<span data-ttu-id="6ae7d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6ae7d-117">Application</span></span>|<span data-ttu-id="6ae7d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ae7d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6ae7d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6ae7d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}/scheduledActionConfigurations/{deviceComplianceActionItemId}
```

## <a name="request-headers"></a><span data-ttu-id="6ae7d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6ae7d-120">Request headers</span></span>
|<span data-ttu-id="6ae7d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ae7d-121">Header</span></span>|<span data-ttu-id="6ae7d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6ae7d-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6ae7d-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="6ae7d-123">Authorization</span></span>|<span data-ttu-id="6ae7d-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6ae7d-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6ae7d-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6ae7d-125">Accept</span></span>|<span data-ttu-id="6ae7d-126">application/json</span><span class="sxs-lookup"><span data-stu-id="6ae7d-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6ae7d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6ae7d-127">Request body</span></span>
<span data-ttu-id="6ae7d-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="6ae7d-128">In the request body, supply a JSON representation for the [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) object.</span></span>

<span data-ttu-id="6ae7d-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="6ae7d-129">The following table shows the properties that are required when you create the [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).</span></span>

|<span data-ttu-id="6ae7d-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6ae7d-130">Property</span></span>|<span data-ttu-id="6ae7d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ae7d-131">Type</span></span>|<span data-ttu-id="6ae7d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ae7d-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6ae7d-133">id</span><span class="sxs-lookup"><span data-stu-id="6ae7d-133">id</span></span>|<span data-ttu-id="6ae7d-134">String</span><span class="sxs-lookup"><span data-stu-id="6ae7d-134">String</span></span>|<span data-ttu-id="6ae7d-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6ae7d-135">Key of the entity.</span></span>|
|<span data-ttu-id="6ae7d-136">gracePeriodHours</span><span class="sxs-lookup"><span data-stu-id="6ae7d-136">gracePeriodHours</span></span>|<span data-ttu-id="6ae7d-137">Int32</span><span class="sxs-lookup"><span data-stu-id="6ae7d-137">Int32</span></span>|<span data-ttu-id="6ae7d-138">Número de horas de espera hasta que se aplica la acción.</span><span class="sxs-lookup"><span data-stu-id="6ae7d-138">Number of hours to wait till the action will be enforced.</span></span> <span data-ttu-id="6ae7d-139">Valores válidos de 0 a 8760</span><span class="sxs-lookup"><span data-stu-id="6ae7d-139">Valid values 0 to 8760</span></span>|
|<span data-ttu-id="6ae7d-140">actionType</span><span class="sxs-lookup"><span data-stu-id="6ae7d-140">actionType</span></span>|[<span data-ttu-id="6ae7d-141">deviceComplianceActionType</span><span class="sxs-lookup"><span data-stu-id="6ae7d-141">deviceComplianceActionType</span></span>](../resources/intune-deviceconfig-devicecomplianceactiontype.md)|<span data-ttu-id="6ae7d-142">¿Qué acción debe realizar.</span><span class="sxs-lookup"><span data-stu-id="6ae7d-142">What action to take.</span></span> <span data-ttu-id="6ae7d-143">Los valores posibles son: `noAction`, `notification`, `block`, `retire`, `wipe`, `removeResourceAccessProfiles`, `pushNotification` y `remoteLock`.</span><span class="sxs-lookup"><span data-stu-id="6ae7d-143">Possible values are: `noAction`, `notification`, `block`, `retire`, `wipe`, `removeResourceAccessProfiles`, `pushNotification`, `remoteLock`.</span></span>|
|<span data-ttu-id="6ae7d-144">notificationTemplateId</span><span class="sxs-lookup"><span data-stu-id="6ae7d-144">notificationTemplateId</span></span>|<span data-ttu-id="6ae7d-145">String</span><span class="sxs-lookup"><span data-stu-id="6ae7d-145">String</span></span>|<span data-ttu-id="6ae7d-146">Qué plantilla de mensaje de notificación usar</span><span class="sxs-lookup"><span data-stu-id="6ae7d-146">What notification Message template to use</span></span>|
|<span data-ttu-id="6ae7d-147">notificationMessageCCList</span><span class="sxs-lookup"><span data-stu-id="6ae7d-147">notificationMessageCCList</span></span>|<span data-ttu-id="6ae7d-148">Colección string</span><span class="sxs-lookup"><span data-stu-id="6ae7d-148">String collection</span></span>|<span data-ttu-id="6ae7d-149">Una lista de identificadores de grupo para especificar a quién enviar este mensaje de notificación.</span><span class="sxs-lookup"><span data-stu-id="6ae7d-149">A list of group IDs to speicify who to CC this notification message to.</span></span>|



## <a name="response"></a><span data-ttu-id="6ae7d-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ae7d-150">Response</span></span>
<span data-ttu-id="6ae7d-151">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ae7d-151">If successful, this method returns a `200 OK` response code and an updated [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6ae7d-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6ae7d-152">Example</span></span>
### <a name="request"></a><span data-ttu-id="6ae7d-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ae7d-153">Request</span></span>
<span data-ttu-id="6ae7d-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6ae7d-154">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}/scheduledActionConfigurations/{deviceComplianceActionItemId}
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

### <a name="response"></a><span data-ttu-id="6ae7d-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ae7d-155">Response</span></span>
<span data-ttu-id="6ae7d-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6ae7d-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




