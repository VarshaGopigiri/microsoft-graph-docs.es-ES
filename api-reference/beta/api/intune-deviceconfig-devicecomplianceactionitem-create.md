---
title: Crear deviceComplianceActionItem
description: Cree un objeto deviceComplianceActionItem.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 788677e6cdf8259cfea3850be3745904e5371220
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27982676"
---
# <a name="create-devicecomplianceactionitem"></a><span data-ttu-id="9b572-103">Crear deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="9b572-103">Create deviceComplianceActionItem</span></span>

> <span data-ttu-id="9b572-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9b572-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9b572-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9b572-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9b572-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9b572-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9b572-107">Cree un objeto [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="9b572-107">Create a new [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9b572-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9b572-108">Prerequisites</span></span>
<span data-ttu-id="9b572-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9b572-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9b572-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9b572-111">Permission type</span></span>|<span data-ttu-id="9b572-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9b572-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9b572-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9b572-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9b572-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9b572-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="9b572-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9b572-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9b572-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b572-116">Not supported.</span></span>|
|<span data-ttu-id="9b572-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9b572-117">Application</span></span>|<span data-ttu-id="9b572-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b572-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9b572-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b572-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}/scheduledActionConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="9b572-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b572-120">Request headers</span></span>
|<span data-ttu-id="9b572-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b572-121">Header</span></span>|<span data-ttu-id="9b572-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9b572-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9b572-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="9b572-123">Authorization</span></span>|<span data-ttu-id="9b572-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9b572-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9b572-125">Accept</span><span class="sxs-lookup"><span data-stu-id="9b572-125">Accept</span></span>|<span data-ttu-id="9b572-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9b572-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9b572-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9b572-127">Request body</span></span>
<span data-ttu-id="9b572-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceComplianceActionItem.</span><span class="sxs-lookup"><span data-stu-id="9b572-128">In the request body, supply a JSON representation for the deviceComplianceActionItem object.</span></span>

<span data-ttu-id="9b572-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceComplianceActionItem.</span><span class="sxs-lookup"><span data-stu-id="9b572-129">The following table shows the properties that are required when you create the deviceComplianceActionItem.</span></span>

|<span data-ttu-id="9b572-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9b572-130">Property</span></span>|<span data-ttu-id="9b572-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b572-131">Type</span></span>|<span data-ttu-id="9b572-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b572-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9b572-133">id</span><span class="sxs-lookup"><span data-stu-id="9b572-133">id</span></span>|<span data-ttu-id="9b572-134">String</span><span class="sxs-lookup"><span data-stu-id="9b572-134">String</span></span>|<span data-ttu-id="9b572-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9b572-135">Key of the entity.</span></span>|
|<span data-ttu-id="9b572-136">gracePeriodHours</span><span class="sxs-lookup"><span data-stu-id="9b572-136">gracePeriodHours</span></span>|<span data-ttu-id="9b572-137">Int32</span><span class="sxs-lookup"><span data-stu-id="9b572-137">Int32</span></span>|<span data-ttu-id="9b572-138">Número de horas de espera hasta que se aplica la acción.</span><span class="sxs-lookup"><span data-stu-id="9b572-138">Number of hours to wait till the action will be enforced.</span></span> <span data-ttu-id="9b572-139">Valores válidos de 0 a 8760</span><span class="sxs-lookup"><span data-stu-id="9b572-139">Valid values 0 to 8760</span></span>|
|<span data-ttu-id="9b572-140">actionType</span><span class="sxs-lookup"><span data-stu-id="9b572-140">actionType</span></span>|[<span data-ttu-id="9b572-141">deviceComplianceActionType</span><span class="sxs-lookup"><span data-stu-id="9b572-141">deviceComplianceActionType</span></span>](../resources/intune-deviceconfig-devicecomplianceactiontype.md)|<span data-ttu-id="9b572-142">¿Qué acción debe realizar.</span><span class="sxs-lookup"><span data-stu-id="9b572-142">What action to take.</span></span> <span data-ttu-id="9b572-143">Los valores posibles son: `noAction`, `notification`, `block`, `retire`, `wipe`, `removeResourceAccessProfiles`, `pushNotification` y `remoteLock`.</span><span class="sxs-lookup"><span data-stu-id="9b572-143">Possible values are: `noAction`, `notification`, `block`, `retire`, `wipe`, `removeResourceAccessProfiles`, `pushNotification`, `remoteLock`.</span></span>|
|<span data-ttu-id="9b572-144">notificationTemplateId</span><span class="sxs-lookup"><span data-stu-id="9b572-144">notificationTemplateId</span></span>|<span data-ttu-id="9b572-145">String</span><span class="sxs-lookup"><span data-stu-id="9b572-145">String</span></span>|<span data-ttu-id="9b572-146">Qué plantilla de mensaje de notificación usar</span><span class="sxs-lookup"><span data-stu-id="9b572-146">What notification Message template to use</span></span>|
|<span data-ttu-id="9b572-147">notificationMessageCCList</span><span class="sxs-lookup"><span data-stu-id="9b572-147">notificationMessageCCList</span></span>|<span data-ttu-id="9b572-148">Colección string</span><span class="sxs-lookup"><span data-stu-id="9b572-148">String collection</span></span>|<span data-ttu-id="9b572-149">Una lista de identificadores de grupo para especificar a quién enviar este mensaje de notificación.</span><span class="sxs-lookup"><span data-stu-id="9b572-149">A list of group IDs to speicify who to CC this notification message to.</span></span>|



## <a name="response"></a><span data-ttu-id="9b572-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b572-150">Response</span></span>
<span data-ttu-id="9b572-151">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b572-151">If successful, this method returns a `201 Created` response code and a [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9b572-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b572-152">Example</span></span>
### <a name="request"></a><span data-ttu-id="9b572-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9b572-153">Request</span></span>
<span data-ttu-id="9b572-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9b572-154">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}/scheduledActionConfigurations
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

### <a name="response"></a><span data-ttu-id="9b572-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b572-155">Response</span></span>
<span data-ttu-id="9b572-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9b572-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





