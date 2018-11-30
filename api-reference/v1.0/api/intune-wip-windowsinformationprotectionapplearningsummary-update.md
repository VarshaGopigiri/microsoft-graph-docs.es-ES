---
title: Actualizar windowsInformationProtectionAppLearningSummary
description: Actualice las propiedades de un objeto windowsInformationProtectionAppLearningSummary.
ms.openlocfilehash: 54eb3de891ad10a41bbe4ca747227b8b3af4f1d8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029626"
---
# <a name="update-windowsinformationprotectionapplearningsummary"></a><span data-ttu-id="6891c-103">Actualizar windowsInformationProtectionAppLearningSummary</span><span class="sxs-lookup"><span data-stu-id="6891c-103">Update windowsInformationProtectionAppLearningSummary</span></span>

> <span data-ttu-id="6891c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6891c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6891c-105">Actualice las propiedades de un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="6891c-105">Update the properties of a [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6891c-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6891c-106">Prerequisites</span></span>
<span data-ttu-id="6891c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6891c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6891c-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6891c-109">Permission type</span></span>|<span data-ttu-id="6891c-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6891c-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6891c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6891c-111">Delegated (work or school account)</span></span>|<span data-ttu-id="6891c-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6891c-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="6891c-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6891c-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6891c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6891c-114">Not supported.</span></span>|
|<span data-ttu-id="6891c-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6891c-115">Application</span></span>|<span data-ttu-id="6891c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6891c-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6891c-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6891c-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/windowsInformationProtectionAppLearningSummaries/{windowsInformationProtectionAppLearningSummaryId}
```

## <a name="request-headers"></a><span data-ttu-id="6891c-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6891c-118">Request headers</span></span>
|<span data-ttu-id="6891c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6891c-119">Header</span></span>|<span data-ttu-id="6891c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6891c-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6891c-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="6891c-121">Authorization</span></span>|<span data-ttu-id="6891c-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6891c-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6891c-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6891c-123">Accept</span></span>|<span data-ttu-id="6891c-124">application/json</span><span class="sxs-lookup"><span data-stu-id="6891c-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6891c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6891c-125">Request body</span></span>
<span data-ttu-id="6891c-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="6891c-126">In the request body, supply a JSON representation for the [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md) object.</span></span>

<span data-ttu-id="6891c-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="6891c-127">The following table shows the properties that are required when you create the [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md).</span></span>

|<span data-ttu-id="6891c-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6891c-128">Property</span></span>|<span data-ttu-id="6891c-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="6891c-129">Type</span></span>|<span data-ttu-id="6891c-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="6891c-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6891c-131">id</span><span class="sxs-lookup"><span data-stu-id="6891c-131">id</span></span>|<span data-ttu-id="6891c-132">String</span><span class="sxs-lookup"><span data-stu-id="6891c-132">String</span></span>|<span data-ttu-id="6891c-133">Identificador único para WindowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="6891c-133">Unique Identifier for the WindowsInformationProtectionAppLearningSummary.</span></span>|
|<span data-ttu-id="6891c-134">applicationName</span><span class="sxs-lookup"><span data-stu-id="6891c-134">applicationName</span></span>|<span data-ttu-id="6891c-135">String</span><span class="sxs-lookup"><span data-stu-id="6891c-135">String</span></span>|<span data-ttu-id="6891c-136">Nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="6891c-136">Application Name</span></span>|
|<span data-ttu-id="6891c-137">applicationType</span><span class="sxs-lookup"><span data-stu-id="6891c-137">applicationType</span></span>|[<span data-ttu-id="6891c-138">applicationType</span><span class="sxs-lookup"><span data-stu-id="6891c-138">applicationType</span></span>](../resources/intune-wip-applicationtype.md)|<span data-ttu-id="6891c-139">Tipo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="6891c-139">Application Type.</span></span> <span data-ttu-id="6891c-140">Los valores posibles son: `universal` y `desktop`.</span><span class="sxs-lookup"><span data-stu-id="6891c-140">Possible values are: `universal`, `desktop`.</span></span>|
|<span data-ttu-id="6891c-141">deviceCount</span><span class="sxs-lookup"><span data-stu-id="6891c-141">deviceCount</span></span>|<span data-ttu-id="6891c-142">Int32</span><span class="sxs-lookup"><span data-stu-id="6891c-142">Int32</span></span>|<span data-ttu-id="6891c-143">Recuento de dispositivos</span><span class="sxs-lookup"><span data-stu-id="6891c-143">Device Count</span></span>|



## <a name="response"></a><span data-ttu-id="6891c-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6891c-144">Response</span></span>
<span data-ttu-id="6891c-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6891c-145">If successful, this method returns a `200 OK` response code and an updated [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6891c-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6891c-146">Example</span></span>
### <a name="request"></a><span data-ttu-id="6891c-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6891c-147">Request</span></span>
<span data-ttu-id="6891c-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6891c-148">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/windowsInformationProtectionAppLearningSummaries/{windowsInformationProtectionAppLearningSummaryId}
Content-type: application/json
Content-length: 191

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLearningSummary",
  "applicationName": "Application Name value",
  "applicationType": "desktop",
  "deviceCount": 11
}
```

### <a name="response"></a><span data-ttu-id="6891c-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6891c-149">Response</span></span>
<span data-ttu-id="6891c-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6891c-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 240

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLearningSummary",
  "id": "063baf50-af50-063b-50af-3b0650af3b06",
  "applicationName": "Application Name value",
  "applicationType": "desktop",
  "deviceCount": 11
}
```



