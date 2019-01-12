---
title: Crear deviceConfigurationConflictSummary
description: Crear un nuevo objeto deviceConfigurationConflictSummary.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ea5aa43cf4df325afbffddcc1323f98bf89a3166
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27968403"
---
# <a name="create-deviceconfigurationconflictsummary"></a><span data-ttu-id="51932-103">Crear deviceConfigurationConflictSummary</span><span class="sxs-lookup"><span data-stu-id="51932-103">Create deviceConfigurationConflictSummary</span></span>

> <span data-ttu-id="51932-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="51932-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="51932-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="51932-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="51932-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="51932-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="51932-107">Crear un nuevo objeto [deviceConfigurationConflictSummary](../resources/intune-deviceconfig-deviceconfigurationconflictsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="51932-107">Create a new [deviceConfigurationConflictSummary](../resources/intune-deviceconfig-deviceconfigurationconflictsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="51932-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="51932-108">Prerequisites</span></span>
<span data-ttu-id="51932-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="51932-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="51932-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="51932-111">Permission type</span></span>|<span data-ttu-id="51932-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="51932-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="51932-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="51932-113">Delegated (work or school account)</span></span>|<span data-ttu-id="51932-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="51932-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="51932-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="51932-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="51932-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="51932-116">Not supported.</span></span>|
|<span data-ttu-id="51932-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="51932-117">Application</span></span>|<span data-ttu-id="51932-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="51932-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="51932-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="51932-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurationConflictSummary
```

## <a name="request-headers"></a><span data-ttu-id="51932-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="51932-120">Request headers</span></span>
|<span data-ttu-id="51932-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51932-121">Header</span></span>|<span data-ttu-id="51932-122">Valor</span><span class="sxs-lookup"><span data-stu-id="51932-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="51932-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="51932-123">Authorization</span></span>|<span data-ttu-id="51932-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="51932-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="51932-125">Accept</span><span class="sxs-lookup"><span data-stu-id="51932-125">Accept</span></span>|<span data-ttu-id="51932-126">application/json</span><span class="sxs-lookup"><span data-stu-id="51932-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="51932-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="51932-127">Request body</span></span>
<span data-ttu-id="51932-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto deviceConfigurationConflictSummary.</span><span class="sxs-lookup"><span data-stu-id="51932-128">In the request body, supply a JSON representation for the deviceConfigurationConflictSummary object.</span></span>

<span data-ttu-id="51932-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el deviceConfigurationConflictSummary.</span><span class="sxs-lookup"><span data-stu-id="51932-129">The following table shows the properties that are required when you create the deviceConfigurationConflictSummary.</span></span>

|<span data-ttu-id="51932-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="51932-130">Property</span></span>|<span data-ttu-id="51932-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="51932-131">Type</span></span>|<span data-ttu-id="51932-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="51932-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="51932-133">conflictingDeviceConfigurations</span><span class="sxs-lookup"><span data-stu-id="51932-133">conflictingDeviceConfigurations</span></span>|<span data-ttu-id="51932-134">Colección [settingSource](../resources/intune-deviceconfig-settingsource.md)</span><span class="sxs-lookup"><span data-stu-id="51932-134">[settingSource](../resources/intune-deviceconfig-settingsource.md) collection</span></span>|<span data-ttu-id="51932-135">El conjunto de directivas en conflicto con la configuración determinada</span><span class="sxs-lookup"><span data-stu-id="51932-135">The set of policies in conflict with the given setting</span></span>|
|<span data-ttu-id="51932-136">id</span><span class="sxs-lookup"><span data-stu-id="51932-136">id</span></span>|<span data-ttu-id="51932-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="51932-137">String</span></span>|<span data-ttu-id="51932-138">El identificador para este conjunto de directivas en conflicto.</span><span class="sxs-lookup"><span data-stu-id="51932-138">The id for this set of conflicting policies.</span></span> <span data-ttu-id="51932-139">Este identificador es los identificadores de todas las directivas en ConflictingDeviceConfigurations en orden lexicográfica separados por caracteres de subrayado.</span><span class="sxs-lookup"><span data-stu-id="51932-139">This id is the ids of all the policies in ConflictingDeviceConfigurations in lexicographical order separated by underscores.</span></span>|
|<span data-ttu-id="51932-140">contributingSettings</span><span class="sxs-lookup"><span data-stu-id="51932-140">contributingSettings</span></span>|<span data-ttu-id="51932-141">Colección String</span><span class="sxs-lookup"><span data-stu-id="51932-141">String collection</span></span>|<span data-ttu-id="51932-142">El conjunto de configuraciones en conflicto con las directivas determinadas</span><span class="sxs-lookup"><span data-stu-id="51932-142">The set of settings in conflict with the given policies</span></span>|
|<span data-ttu-id="51932-143">deviceCheckinsImpacted</span><span class="sxs-lookup"><span data-stu-id="51932-143">deviceCheckinsImpacted</span></span>|<span data-ttu-id="51932-144">Int32</span><span class="sxs-lookup"><span data-stu-id="51932-144">Int32</span></span>|<span data-ttu-id="51932-145">El recuento de protecciones afectado por la configuración y las directivas en conflicto</span><span class="sxs-lookup"><span data-stu-id="51932-145">The count of checkins impacted by the conflicting policies and settings</span></span>|



## <a name="response"></a><span data-ttu-id="51932-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51932-146">Response</span></span>
<span data-ttu-id="51932-147">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [deviceConfigurationConflictSummary](../resources/intune-deviceconfig-deviceconfigurationconflictsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="51932-147">If successful, this method returns a `201 Created` response code and a [deviceConfigurationConflictSummary](../resources/intune-deviceconfig-deviceconfigurationconflictsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="51932-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="51932-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="51932-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="51932-149">Request</span></span>
<span data-ttu-id="51932-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="51932-150">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurationConflictSummary
Content-type: application/json
Content-length: 361

{
  "@odata.type": "#microsoft.graph.deviceConfigurationConflictSummary",
  "conflictingDeviceConfigurations": [
    {
      "@odata.type": "microsoft.graph.settingSource",
      "id": "Id value",
      "displayName": "Display Name value"
    }
  ],
  "contributingSettings": [
    "Contributing Settings value"
  ],
  "deviceCheckinsImpacted": 6
}
```

### <a name="response"></a><span data-ttu-id="51932-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51932-151">Response</span></span>
<span data-ttu-id="51932-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="51932-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 410

{
  "@odata.type": "#microsoft.graph.deviceConfigurationConflictSummary",
  "conflictingDeviceConfigurations": [
    {
      "@odata.type": "microsoft.graph.settingSource",
      "id": "Id value",
      "displayName": "Display Name value"
    }
  ],
  "id": "d5f22c23-2c23-d5f2-232c-f2d5232cf2d5",
  "contributingSettings": [
    "Contributing Settings value"
  ],
  "deviceCheckinsImpacted": 6
}
```





