---
title: Crear windowsInformationProtectionAppLearningSummary
description: Cree un objeto windowsInformationProtectionAppLearningSummary.
ms.openlocfilehash: 03a03e0e32115cd0f5b2f56e652c608073db7d94
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030520"
---
# <a name="create-windowsinformationprotectionapplearningsummary"></a><span data-ttu-id="e336b-103">Crear windowsInformationProtectionAppLearningSummary</span><span class="sxs-lookup"><span data-stu-id="e336b-103">Create windowsInformationProtectionAppLearningSummary</span></span>

> <span data-ttu-id="e336b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e336b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e336b-105">Cree un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="e336b-105">Create a new [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e336b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e336b-106">Prerequisites</span></span>
<span data-ttu-id="e336b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e336b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e336b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e336b-109">Permission type</span></span>|<span data-ttu-id="e336b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e336b-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e336b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e336b-111">Delegated (work or school account)</span></span>|<span data-ttu-id="e336b-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e336b-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="e336b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e336b-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e336b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e336b-114">Not supported.</span></span>|
|<span data-ttu-id="e336b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e336b-115">Application</span></span>|<span data-ttu-id="e336b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e336b-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e336b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e336b-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/windowsInformationProtectionAppLearningSummaries
```

## <a name="request-headers"></a><span data-ttu-id="e336b-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e336b-118">Request headers</span></span>
|<span data-ttu-id="e336b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e336b-119">Header</span></span>|<span data-ttu-id="e336b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e336b-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e336b-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="e336b-121">Authorization</span></span>|<span data-ttu-id="e336b-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e336b-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e336b-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e336b-123">Accept</span></span>|<span data-ttu-id="e336b-124">application/json</span><span class="sxs-lookup"><span data-stu-id="e336b-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e336b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e336b-125">Request body</span></span>
<span data-ttu-id="e336b-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="e336b-126">In the request body, supply a JSON representation for the windowsInformationProtectionAppLearningSummary object.</span></span>

<span data-ttu-id="e336b-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="e336b-127">The following table shows the properties that are required when you create the windowsInformationProtectionAppLearningSummary.</span></span>

|<span data-ttu-id="e336b-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e336b-128">Property</span></span>|<span data-ttu-id="e336b-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="e336b-129">Type</span></span>|<span data-ttu-id="e336b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="e336b-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e336b-131">id</span><span class="sxs-lookup"><span data-stu-id="e336b-131">id</span></span>|<span data-ttu-id="e336b-132">String</span><span class="sxs-lookup"><span data-stu-id="e336b-132">String</span></span>|<span data-ttu-id="e336b-133">Identificador único para WindowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="e336b-133">Unique Identifier for the WindowsInformationProtectionAppLearningSummary.</span></span>|
|<span data-ttu-id="e336b-134">applicationName</span><span class="sxs-lookup"><span data-stu-id="e336b-134">applicationName</span></span>|<span data-ttu-id="e336b-135">String</span><span class="sxs-lookup"><span data-stu-id="e336b-135">String</span></span>|<span data-ttu-id="e336b-136">Nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="e336b-136">Application Name</span></span>|
|<span data-ttu-id="e336b-137">applicationType</span><span class="sxs-lookup"><span data-stu-id="e336b-137">applicationType</span></span>|[<span data-ttu-id="e336b-138">applicationType</span><span class="sxs-lookup"><span data-stu-id="e336b-138">applicationType</span></span>](../resources/intune-wip-applicationtype.md)|<span data-ttu-id="e336b-139">Tipo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="e336b-139">Application Type.</span></span> <span data-ttu-id="e336b-140">Los valores posibles son: `universal` y `desktop`.</span><span class="sxs-lookup"><span data-stu-id="e336b-140">Possible values are: `universal`, `desktop`.</span></span>|
|<span data-ttu-id="e336b-141">deviceCount</span><span class="sxs-lookup"><span data-stu-id="e336b-141">deviceCount</span></span>|<span data-ttu-id="e336b-142">Int32</span><span class="sxs-lookup"><span data-stu-id="e336b-142">Int32</span></span>|<span data-ttu-id="e336b-143">Recuento de dispositivos</span><span class="sxs-lookup"><span data-stu-id="e336b-143">Device Count</span></span>|



## <a name="response"></a><span data-ttu-id="e336b-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e336b-144">Response</span></span>
<span data-ttu-id="e336b-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e336b-145">If successful, this method returns a `201 Created` response code and a [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e336b-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e336b-146">Example</span></span>
### <a name="request"></a><span data-ttu-id="e336b-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e336b-147">Request</span></span>
<span data-ttu-id="e336b-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e336b-148">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/windowsInformationProtectionAppLearningSummaries
Content-type: application/json
Content-length: 191

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLearningSummary",
  "applicationName": "Application Name value",
  "applicationType": "desktop",
  "deviceCount": 11
}
```

### <a name="response"></a><span data-ttu-id="e336b-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e336b-149">Response</span></span>
<span data-ttu-id="e336b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e336b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



