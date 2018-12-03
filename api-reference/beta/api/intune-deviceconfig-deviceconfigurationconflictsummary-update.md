---
title: Actualizar deviceConfigurationConflictSummary
description: Actualizar las propiedades de un objeto deviceConfigurationConflictSummary.
ms.openlocfilehash: 583d00b1ee7bbb3547592cc58f45899aa89c4219
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083899"
---
# <a name="update-deviceconfigurationconflictsummary"></a><span data-ttu-id="f5842-103">Actualizar deviceConfigurationConflictSummary</span><span class="sxs-lookup"><span data-stu-id="f5842-103">Update deviceConfigurationConflictSummary</span></span>

> <span data-ttu-id="f5842-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f5842-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f5842-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f5842-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f5842-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f5842-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f5842-107">Actualizar las propiedades de un objeto [deviceConfigurationConflictSummary](../resources/intune-deviceconfig-deviceconfigurationconflictsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="f5842-107">Update the properties of a [deviceConfigurationConflictSummary](../resources/intune-deviceconfig-deviceconfigurationconflictsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f5842-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f5842-108">Prerequisites</span></span>
<span data-ttu-id="f5842-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f5842-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f5842-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f5842-111">Permission type</span></span>|<span data-ttu-id="f5842-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f5842-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f5842-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f5842-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f5842-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f5842-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="f5842-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f5842-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f5842-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f5842-116">Not supported.</span></span>|
|<span data-ttu-id="f5842-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f5842-117">Application</span></span>|<span data-ttu-id="f5842-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f5842-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f5842-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f5842-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurationConflictSummary/{deviceConfigurationConflictSummaryId}
```

## <a name="request-headers"></a><span data-ttu-id="f5842-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f5842-120">Request headers</span></span>
|<span data-ttu-id="f5842-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5842-121">Header</span></span>|<span data-ttu-id="f5842-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f5842-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f5842-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="f5842-123">Authorization</span></span>|<span data-ttu-id="f5842-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f5842-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f5842-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f5842-125">Accept</span></span>|<span data-ttu-id="f5842-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f5842-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f5842-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f5842-127">Request body</span></span>
<span data-ttu-id="f5842-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [deviceConfigurationConflictSummary](../resources/intune-deviceconfig-deviceconfigurationconflictsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="f5842-128">In the request body, supply a JSON representation for the [deviceConfigurationConflictSummary](../resources/intune-deviceconfig-deviceconfigurationconflictsummary.md) object.</span></span>

<span data-ttu-id="f5842-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [deviceConfigurationConflictSummary](../resources/intune-deviceconfig-deviceconfigurationconflictsummary.md).</span><span class="sxs-lookup"><span data-stu-id="f5842-129">The following table shows the properties that are required when you create the [deviceConfigurationConflictSummary](../resources/intune-deviceconfig-deviceconfigurationconflictsummary.md).</span></span>

|<span data-ttu-id="f5842-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f5842-130">Property</span></span>|<span data-ttu-id="f5842-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5842-131">Type</span></span>|<span data-ttu-id="f5842-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5842-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f5842-133">conflictingDeviceConfigurations</span><span class="sxs-lookup"><span data-stu-id="f5842-133">conflictingDeviceConfigurations</span></span>|<span data-ttu-id="f5842-134">Colección [settingSource](../resources/intune-deviceconfig-settingsource.md)</span><span class="sxs-lookup"><span data-stu-id="f5842-134">[settingSource](../resources/intune-deviceconfig-settingsource.md) collection</span></span>|<span data-ttu-id="f5842-135">El conjunto de directivas en conflicto con la configuración determinada</span><span class="sxs-lookup"><span data-stu-id="f5842-135">The set of policies in conflict with the given setting</span></span>|
|<span data-ttu-id="f5842-136">id</span><span class="sxs-lookup"><span data-stu-id="f5842-136">id</span></span>|<span data-ttu-id="f5842-137">String</span><span class="sxs-lookup"><span data-stu-id="f5842-137">String</span></span>|<span data-ttu-id="f5842-138">El identificador para este conjunto de directivas en conflicto.</span><span class="sxs-lookup"><span data-stu-id="f5842-138">The id for this set of conflicting policies.</span></span> <span data-ttu-id="f5842-139">Este identificador es los identificadores de todas las directivas en ConflictingDeviceConfigurations en orden lexicográfica separados por caracteres de subrayado.</span><span class="sxs-lookup"><span data-stu-id="f5842-139">This id is the ids of all the policies in ConflictingDeviceConfigurations in lexicographical order separated by underscores.</span></span>|
|<span data-ttu-id="f5842-140">contributingSettings</span><span class="sxs-lookup"><span data-stu-id="f5842-140">contributingSettings</span></span>|<span data-ttu-id="f5842-141">Colección String</span><span class="sxs-lookup"><span data-stu-id="f5842-141">String collection</span></span>|<span data-ttu-id="f5842-142">El conjunto de configuraciones en conflicto con las directivas determinadas</span><span class="sxs-lookup"><span data-stu-id="f5842-142">The set of settings in conflict with the given policies</span></span>|
|<span data-ttu-id="f5842-143">deviceCheckinsImpacted</span><span class="sxs-lookup"><span data-stu-id="f5842-143">deviceCheckinsImpacted</span></span>|<span data-ttu-id="f5842-144">Int32</span><span class="sxs-lookup"><span data-stu-id="f5842-144">Int32</span></span>|<span data-ttu-id="f5842-145">El recuento de protecciones afectado por la configuración y las directivas en conflicto</span><span class="sxs-lookup"><span data-stu-id="f5842-145">The count of checkins impacted by the conflicting policies and settings</span></span>|



## <a name="response"></a><span data-ttu-id="f5842-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5842-146">Response</span></span>
<span data-ttu-id="f5842-147">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [deviceConfigurationConflictSummary](../resources/intune-deviceconfig-deviceconfigurationconflictsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f5842-147">If successful, this method returns a `200 OK` response code and an updated [deviceConfigurationConflictSummary](../resources/intune-deviceconfig-deviceconfigurationconflictsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f5842-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f5842-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="f5842-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f5842-149">Request</span></span>
<span data-ttu-id="f5842-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f5842-150">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurationConflictSummary/{deviceConfigurationConflictSummaryId}
Content-type: application/json
Content-length: 288

{
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

### <a name="response"></a><span data-ttu-id="f5842-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5842-151">Response</span></span>
<span data-ttu-id="f5842-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f5842-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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




