---
title: Crear deviceComplianceActionItem
description: Cree un objeto deviceComplianceActionItem.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: cd7cb91d6dde4755f27bdc28b3fb1c0c8804a800
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972064"
---
# <a name="create-devicecomplianceactionitem"></a><span data-ttu-id="4ea66-103">Crear deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="4ea66-103">Create deviceComplianceActionItem</span></span>

> <span data-ttu-id="4ea66-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4ea66-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4ea66-105">Cree un objeto [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="4ea66-105">Create a new [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4ea66-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4ea66-106">Prerequisites</span></span>
<span data-ttu-id="4ea66-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4ea66-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4ea66-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4ea66-109">Permission type</span></span>|<span data-ttu-id="4ea66-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4ea66-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4ea66-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4ea66-111">Delegated (work or school account)</span></span>|<span data-ttu-id="4ea66-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4ea66-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="4ea66-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4ea66-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4ea66-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4ea66-114">Not supported.</span></span>|
|<span data-ttu-id="4ea66-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4ea66-115">Application</span></span>|<span data-ttu-id="4ea66-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4ea66-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4ea66-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4ea66-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}/scheduledActionConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="4ea66-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4ea66-118">Request headers</span></span>
|<span data-ttu-id="4ea66-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ea66-119">Header</span></span>|<span data-ttu-id="4ea66-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4ea66-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4ea66-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="4ea66-121">Authorization</span></span>|<span data-ttu-id="4ea66-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4ea66-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4ea66-123">Accept</span><span class="sxs-lookup"><span data-stu-id="4ea66-123">Accept</span></span>|<span data-ttu-id="4ea66-124">application/json</span><span class="sxs-lookup"><span data-stu-id="4ea66-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4ea66-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4ea66-125">Request body</span></span>
<span data-ttu-id="4ea66-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceComplianceActionItem.</span><span class="sxs-lookup"><span data-stu-id="4ea66-126">In the request body, supply a JSON representation for the deviceComplianceActionItem object.</span></span>

<span data-ttu-id="4ea66-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceComplianceActionItem.</span><span class="sxs-lookup"><span data-stu-id="4ea66-127">The following table shows the properties that are required when you create the deviceComplianceActionItem.</span></span>

|<span data-ttu-id="4ea66-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4ea66-128">Property</span></span>|<span data-ttu-id="4ea66-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="4ea66-129">Type</span></span>|<span data-ttu-id="4ea66-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ea66-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4ea66-131">id</span><span class="sxs-lookup"><span data-stu-id="4ea66-131">id</span></span>|<span data-ttu-id="4ea66-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="4ea66-132">String</span></span>|<span data-ttu-id="4ea66-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="4ea66-133">Key of the entity.</span></span>|
|<span data-ttu-id="4ea66-134">gracePeriodHours</span><span class="sxs-lookup"><span data-stu-id="4ea66-134">gracePeriodHours</span></span>|<span data-ttu-id="4ea66-135">Int32</span><span class="sxs-lookup"><span data-stu-id="4ea66-135">Int32</span></span>|<span data-ttu-id="4ea66-136">Número de horas de espera hasta que se aplica la acción.</span><span class="sxs-lookup"><span data-stu-id="4ea66-136">Number of hours to wait till the action will be enforced.</span></span> <span data-ttu-id="4ea66-137">Valores válidos de 0 a 8760</span><span class="sxs-lookup"><span data-stu-id="4ea66-137">Valid values 0 to 8760</span></span>|
|<span data-ttu-id="4ea66-138">actionType</span><span class="sxs-lookup"><span data-stu-id="4ea66-138">actionType</span></span>|[<span data-ttu-id="4ea66-139">deviceComplianceActionType</span><span class="sxs-lookup"><span data-stu-id="4ea66-139">deviceComplianceActionType</span></span>](../resources/intune-deviceconfig-devicecomplianceactiontype.md)|<span data-ttu-id="4ea66-140">¿Qué acción debe realizar.</span><span class="sxs-lookup"><span data-stu-id="4ea66-140">What action to take.</span></span> <span data-ttu-id="4ea66-141">Los valores posibles son: `noAction`, `notification`, `block`, `retire`, `wipe`, `removeResourceAccessProfiles` y `pushNotification`.</span><span class="sxs-lookup"><span data-stu-id="4ea66-141">Possible values are: `noAction`, `notification`, `block`, `retire`, `wipe`, `removeResourceAccessProfiles`, `pushNotification`.</span></span>|
|<span data-ttu-id="4ea66-142">notificationTemplateId</span><span class="sxs-lookup"><span data-stu-id="4ea66-142">notificationTemplateId</span></span>|<span data-ttu-id="4ea66-143">String</span><span class="sxs-lookup"><span data-stu-id="4ea66-143">String</span></span>|<span data-ttu-id="4ea66-144">Qué plantilla de mensaje de notificación usar</span><span class="sxs-lookup"><span data-stu-id="4ea66-144">What notification Message template to use</span></span>|
|<span data-ttu-id="4ea66-145">notificationMessageCCList</span><span class="sxs-lookup"><span data-stu-id="4ea66-145">notificationMessageCCList</span></span>|<span data-ttu-id="4ea66-146">Colección string</span><span class="sxs-lookup"><span data-stu-id="4ea66-146">String collection</span></span>|<span data-ttu-id="4ea66-147">Una lista de identificadores de grupo para especificar a quién enviar este mensaje de notificación.</span><span class="sxs-lookup"><span data-stu-id="4ea66-147">A list of group IDs to speicify who to CC this notification message to.</span></span>|



## <a name="response"></a><span data-ttu-id="4ea66-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4ea66-148">Response</span></span>
<span data-ttu-id="4ea66-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4ea66-149">If successful, this method returns a `201 Created` response code and a [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4ea66-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4ea66-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="4ea66-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4ea66-151">Request</span></span>
<span data-ttu-id="4ea66-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4ea66-152">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="4ea66-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4ea66-153">Response</span></span>
<span data-ttu-id="4ea66-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4ea66-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



