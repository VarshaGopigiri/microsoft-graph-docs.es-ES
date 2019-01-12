---
title: Actualizar windowsInformationProtectionAppLearningSummary
description: Actualice las propiedades de un objeto windowsInformationProtectionAppLearningSummary.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 465002edd3060961a2e53484aef998d9e4e0051a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27948734"
---
# <a name="update-windowsinformationprotectionapplearningsummary"></a><span data-ttu-id="6dc5a-103">Actualizar windowsInformationProtectionAppLearningSummary</span><span class="sxs-lookup"><span data-stu-id="6dc5a-103">Update windowsInformationProtectionAppLearningSummary</span></span>

> <span data-ttu-id="6dc5a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6dc5a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6dc5a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6dc5a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6dc5a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6dc5a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6dc5a-107">Actualice las propiedades de un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="6dc5a-107">Update the properties of a [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6dc5a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6dc5a-108">Prerequisites</span></span>
<span data-ttu-id="6dc5a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6dc5a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6dc5a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6dc5a-111">Permission type</span></span>|<span data-ttu-id="6dc5a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6dc5a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6dc5a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6dc5a-113">Delegated (work or school account)</span></span>|<span data-ttu-id="6dc5a-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6dc5a-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="6dc5a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6dc5a-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6dc5a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6dc5a-116">Not supported.</span></span>|
|<span data-ttu-id="6dc5a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6dc5a-117">Application</span></span>|<span data-ttu-id="6dc5a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6dc5a-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6dc5a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6dc5a-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/windowsInformationProtectionAppLearningSummaries/{windowsInformationProtectionAppLearningSummaryId}
```

## <a name="request-headers"></a><span data-ttu-id="6dc5a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6dc5a-120">Request headers</span></span>
|<span data-ttu-id="6dc5a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6dc5a-121">Header</span></span>|<span data-ttu-id="6dc5a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6dc5a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6dc5a-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="6dc5a-123">Authorization</span></span>|<span data-ttu-id="6dc5a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6dc5a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6dc5a-125">Accept</span><span class="sxs-lookup"><span data-stu-id="6dc5a-125">Accept</span></span>|<span data-ttu-id="6dc5a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="6dc5a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6dc5a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6dc5a-127">Request body</span></span>
<span data-ttu-id="6dc5a-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="6dc5a-128">In the request body, supply a JSON representation for the [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md) object.</span></span>

<span data-ttu-id="6dc5a-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="6dc5a-129">The following table shows the properties that are required when you create the [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md).</span></span>

|<span data-ttu-id="6dc5a-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6dc5a-130">Property</span></span>|<span data-ttu-id="6dc5a-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6dc5a-131">Type</span></span>|<span data-ttu-id="6dc5a-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6dc5a-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6dc5a-133">id</span><span class="sxs-lookup"><span data-stu-id="6dc5a-133">id</span></span>|<span data-ttu-id="6dc5a-134">String</span><span class="sxs-lookup"><span data-stu-id="6dc5a-134">String</span></span>|<span data-ttu-id="6dc5a-135">Identificador único para WindowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="6dc5a-135">Unique Identifier for the WindowsInformationProtectionAppLearningSummary.</span></span>|
|<span data-ttu-id="6dc5a-136">applicationName</span><span class="sxs-lookup"><span data-stu-id="6dc5a-136">applicationName</span></span>|<span data-ttu-id="6dc5a-137">String</span><span class="sxs-lookup"><span data-stu-id="6dc5a-137">String</span></span>|<span data-ttu-id="6dc5a-138">Nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="6dc5a-138">Application Name</span></span>|
|<span data-ttu-id="6dc5a-139">applicationType</span><span class="sxs-lookup"><span data-stu-id="6dc5a-139">applicationType</span></span>|[<span data-ttu-id="6dc5a-140">applicationType</span><span class="sxs-lookup"><span data-stu-id="6dc5a-140">applicationType</span></span>](../resources/intune-wip-applicationtype.md)|<span data-ttu-id="6dc5a-141">Tipo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="6dc5a-141">Application Type.</span></span> <span data-ttu-id="6dc5a-142">Los valores posibles son: `universal` y `desktop`.</span><span class="sxs-lookup"><span data-stu-id="6dc5a-142">Possible values are: `universal`, `desktop`.</span></span>|
|<span data-ttu-id="6dc5a-143">deviceCount</span><span class="sxs-lookup"><span data-stu-id="6dc5a-143">deviceCount</span></span>|<span data-ttu-id="6dc5a-144">Int32</span><span class="sxs-lookup"><span data-stu-id="6dc5a-144">Int32</span></span>|<span data-ttu-id="6dc5a-145">Recuento de dispositivos</span><span class="sxs-lookup"><span data-stu-id="6dc5a-145">Device Count</span></span>|



## <a name="response"></a><span data-ttu-id="6dc5a-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6dc5a-146">Response</span></span>
<span data-ttu-id="6dc5a-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6dc5a-147">If successful, this method returns a `200 OK` response code and an updated [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6dc5a-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6dc5a-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="6dc5a-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6dc5a-149">Request</span></span>
<span data-ttu-id="6dc5a-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6dc5a-150">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/windowsInformationProtectionAppLearningSummaries/{windowsInformationProtectionAppLearningSummaryId}
Content-type: application/json
Content-length: 106

{
  "applicationName": "Application Name value",
  "applicationType": "desktop",
  "deviceCount": 11
}
```

### <a name="response"></a><span data-ttu-id="6dc5a-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6dc5a-151">Response</span></span>
<span data-ttu-id="6dc5a-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6dc5a-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





