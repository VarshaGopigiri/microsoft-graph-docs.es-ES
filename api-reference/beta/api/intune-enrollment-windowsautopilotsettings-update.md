---
title: Actualizar windowsAutopilotSettings
description: Actualizar las propiedades de un objeto windowsAutopilotSettings.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8087ce2a3d7fd02eb6cc118d75082382bcddd58d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27877654"
---
# <a name="update-windowsautopilotsettings"></a><span data-ttu-id="e4b82-103">Actualizar windowsAutopilotSettings</span><span class="sxs-lookup"><span data-stu-id="e4b82-103">Update windowsAutopilotSettings</span></span>

> <span data-ttu-id="e4b82-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e4b82-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e4b82-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e4b82-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e4b82-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e4b82-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e4b82-107">Actualizar las propiedades de un objeto [windowsAutopilotSettings](../resources/intune-enrollment-windowsautopilotsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="e4b82-107">Update the properties of a [windowsAutopilotSettings](../resources/intune-enrollment-windowsautopilotsettings.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e4b82-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e4b82-108">Prerequisites</span></span>
<span data-ttu-id="e4b82-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e4b82-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e4b82-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e4b82-111">Permission type</span></span>|<span data-ttu-id="e4b82-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e4b82-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e4b82-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e4b82-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e4b82-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e4b82-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="e4b82-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e4b82-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e4b82-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e4b82-116">Not supported.</span></span>|
|<span data-ttu-id="e4b82-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e4b82-117">Application</span></span>|<span data-ttu-id="e4b82-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e4b82-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e4b82-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e4b82-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/windowsAutopilotSettings
```

## <a name="request-headers"></a><span data-ttu-id="e4b82-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e4b82-120">Request headers</span></span>
|<span data-ttu-id="e4b82-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4b82-121">Header</span></span>|<span data-ttu-id="e4b82-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e4b82-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e4b82-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="e4b82-123">Authorization</span></span>|<span data-ttu-id="e4b82-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e4b82-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e4b82-125">Accept</span><span class="sxs-lookup"><span data-stu-id="e4b82-125">Accept</span></span>|<span data-ttu-id="e4b82-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e4b82-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e4b82-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e4b82-127">Request body</span></span>
<span data-ttu-id="e4b82-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsAutopilotSettings](../resources/intune-enrollment-windowsautopilotsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="e4b82-128">In the request body, supply a JSON representation for the [windowsAutopilotSettings](../resources/intune-enrollment-windowsautopilotsettings.md) object.</span></span>

<span data-ttu-id="e4b82-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsAutopilotSettings](../resources/intune-enrollment-windowsautopilotsettings.md).</span><span class="sxs-lookup"><span data-stu-id="e4b82-129">The following table shows the properties that are required when you create the [windowsAutopilotSettings](../resources/intune-enrollment-windowsautopilotsettings.md).</span></span>

|<span data-ttu-id="e4b82-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e4b82-130">Property</span></span>|<span data-ttu-id="e4b82-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4b82-131">Type</span></span>|<span data-ttu-id="e4b82-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4b82-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e4b82-133">id</span><span class="sxs-lookup"><span data-stu-id="e4b82-133">id</span></span>|<span data-ttu-id="e4b82-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="e4b82-134">String</span></span>|<span data-ttu-id="e4b82-135">El GUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="e4b82-135">The GUID for the object</span></span>|
|<span data-ttu-id="e4b82-136">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="e4b82-136">lastSyncDateTime</span></span>|<span data-ttu-id="e4b82-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e4b82-137">DateTimeOffset</span></span>|<span data-ttu-id="e4b82-138">Datos de la última sincronización de la hora de fecha con el servicio DDS.</span><span class="sxs-lookup"><span data-stu-id="e4b82-138">Last data sync date time with DDS service.</span></span>|
|<span data-ttu-id="e4b82-139">lastManualSyncTriggerDateTime</span><span class="sxs-lookup"><span data-stu-id="e4b82-139">lastManualSyncTriggerDateTime</span></span>|<span data-ttu-id="e4b82-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e4b82-140">DateTimeOffset</span></span>|<span data-ttu-id="e4b82-141">Datos de la última sincronización de la hora de fecha con el servicio DDS.</span><span class="sxs-lookup"><span data-stu-id="e4b82-141">Last data sync date time with DDS service.</span></span>|
|<span data-ttu-id="e4b82-142">syncStatus</span><span class="sxs-lookup"><span data-stu-id="e4b82-142">syncStatus</span></span>|[<span data-ttu-id="e4b82-143">windowsAutopilotSyncStatus</span><span class="sxs-lookup"><span data-stu-id="e4b82-143">windowsAutopilotSyncStatus</span></span>](../resources/intune-enrollment-windowsautopilotsyncstatus.md)|<span data-ttu-id="e4b82-144">Indica el estado de sincronización con el servicio de sincronización (DDS) de datos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e4b82-144">Indicates the status of sync with Device data sync (DDS) service.</span></span> <span data-ttu-id="e4b82-145">Los valores posibles son: `unknown`, `inProgress`, `completed` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="e4b82-145">Possible values are: `unknown`, `inProgress`, `completed`, `failed`.</span></span>|



## <a name="response"></a><span data-ttu-id="e4b82-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4b82-146">Response</span></span>
<span data-ttu-id="e4b82-147">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windowsAutopilotSettings](../resources/intune-enrollment-windowsautopilotsettings.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e4b82-147">If successful, this method returns a `200 OK` response code and an updated [windowsAutopilotSettings](../resources/intune-enrollment-windowsautopilotsettings.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e4b82-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e4b82-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="e4b82-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e4b82-149">Request</span></span>
<span data-ttu-id="e4b82-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e4b82-150">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/windowsAutopilotSettings
Content-type: application/json
Content-length: 167

{
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "lastManualSyncTriggerDateTime": "2016-12-31T23:57:54.7364636-08:00",
  "syncStatus": "inProgress"
}
```

### <a name="response"></a><span data-ttu-id="e4b82-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4b82-151">Response</span></span>
<span data-ttu-id="e4b82-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e4b82-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 279

{
  "@odata.type": "#microsoft.graph.windowsAutopilotSettings",
  "id": "08c16770-6770-08c1-7067-c1087067c108",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "lastManualSyncTriggerDateTime": "2016-12-31T23:57:54.7364636-08:00",
  "syncStatus": "inProgress"
}
```





