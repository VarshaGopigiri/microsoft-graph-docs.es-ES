---
title: Crear windowsInformationProtectionAppLearningSummary
description: Cree un objeto windowsInformationProtectionAppLearningSummary.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 66658cdd601ec7ea1af60a29a9302ca100debfaf
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27940585"
---
# <a name="create-windowsinformationprotectionapplearningsummary"></a><span data-ttu-id="63be1-103">Crear windowsInformationProtectionAppLearningSummary</span><span class="sxs-lookup"><span data-stu-id="63be1-103">Create windowsInformationProtectionAppLearningSummary</span></span>

> <span data-ttu-id="63be1-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="63be1-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="63be1-105">Cree un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="63be1-105">Create a new [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="63be1-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="63be1-106">Prerequisites</span></span>
<span data-ttu-id="63be1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="63be1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="63be1-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="63be1-109">Permission type</span></span>|<span data-ttu-id="63be1-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="63be1-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="63be1-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="63be1-111">Delegated (work or school account)</span></span>|<span data-ttu-id="63be1-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="63be1-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="63be1-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="63be1-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="63be1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63be1-114">Not supported.</span></span>|
|<span data-ttu-id="63be1-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="63be1-115">Application</span></span>|<span data-ttu-id="63be1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63be1-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="63be1-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="63be1-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/windowsInformationProtectionAppLearningSummaries
```

## <a name="request-headers"></a><span data-ttu-id="63be1-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="63be1-118">Request headers</span></span>
|<span data-ttu-id="63be1-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63be1-119">Header</span></span>|<span data-ttu-id="63be1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="63be1-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="63be1-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="63be1-121">Authorization</span></span>|<span data-ttu-id="63be1-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="63be1-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="63be1-123">Accept</span><span class="sxs-lookup"><span data-stu-id="63be1-123">Accept</span></span>|<span data-ttu-id="63be1-124">application/json</span><span class="sxs-lookup"><span data-stu-id="63be1-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="63be1-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="63be1-125">Request body</span></span>
<span data-ttu-id="63be1-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="63be1-126">In the request body, supply a JSON representation for the windowsInformationProtectionAppLearningSummary object.</span></span>

<span data-ttu-id="63be1-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="63be1-127">The following table shows the properties that are required when you create the windowsInformationProtectionAppLearningSummary.</span></span>

|<span data-ttu-id="63be1-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="63be1-128">Property</span></span>|<span data-ttu-id="63be1-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="63be1-129">Type</span></span>|<span data-ttu-id="63be1-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="63be1-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="63be1-131">id</span><span class="sxs-lookup"><span data-stu-id="63be1-131">id</span></span>|<span data-ttu-id="63be1-132">String</span><span class="sxs-lookup"><span data-stu-id="63be1-132">String</span></span>|<span data-ttu-id="63be1-133">Identificador único para WindowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="63be1-133">Unique Identifier for the WindowsInformationProtectionAppLearningSummary.</span></span>|
|<span data-ttu-id="63be1-134">applicationName</span><span class="sxs-lookup"><span data-stu-id="63be1-134">applicationName</span></span>|<span data-ttu-id="63be1-135">String</span><span class="sxs-lookup"><span data-stu-id="63be1-135">String</span></span>|<span data-ttu-id="63be1-136">Nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="63be1-136">Application Name</span></span>|
|<span data-ttu-id="63be1-137">applicationType</span><span class="sxs-lookup"><span data-stu-id="63be1-137">applicationType</span></span>|[<span data-ttu-id="63be1-138">applicationType</span><span class="sxs-lookup"><span data-stu-id="63be1-138">applicationType</span></span>](../resources/intune-wip-applicationtype.md)|<span data-ttu-id="63be1-139">Tipo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="63be1-139">Application Type.</span></span> <span data-ttu-id="63be1-140">Los valores posibles son: `universal` y `desktop`.</span><span class="sxs-lookup"><span data-stu-id="63be1-140">Possible values are: `universal`, `desktop`.</span></span>|
|<span data-ttu-id="63be1-141">deviceCount</span><span class="sxs-lookup"><span data-stu-id="63be1-141">deviceCount</span></span>|<span data-ttu-id="63be1-142">Int32</span><span class="sxs-lookup"><span data-stu-id="63be1-142">Int32</span></span>|<span data-ttu-id="63be1-143">Recuento de dispositivos</span><span class="sxs-lookup"><span data-stu-id="63be1-143">Device Count</span></span>|



## <a name="response"></a><span data-ttu-id="63be1-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63be1-144">Response</span></span>
<span data-ttu-id="63be1-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63be1-145">If successful, this method returns a `201 Created` response code and a [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="63be1-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="63be1-146">Example</span></span>
### <a name="request"></a><span data-ttu-id="63be1-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="63be1-147">Request</span></span>
<span data-ttu-id="63be1-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63be1-148">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="63be1-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63be1-149">Response</span></span>
<span data-ttu-id="63be1-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="63be1-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



