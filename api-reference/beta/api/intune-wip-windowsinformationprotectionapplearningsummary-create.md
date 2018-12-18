---
title: Crear windowsInformationProtectionAppLearningSummary
description: Cree un objeto windowsInformationProtectionAppLearningSummary.
author: tfitzmac
ms.openlocfilehash: 018d31a7ea356478bff2d416e13d2924931cc7cb
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27318756"
---
# <a name="create-windowsinformationprotectionapplearningsummary"></a><span data-ttu-id="cbb32-103">Crear windowsInformationProtectionAppLearningSummary</span><span class="sxs-lookup"><span data-stu-id="cbb32-103">Create windowsInformationProtectionAppLearningSummary</span></span>

> <span data-ttu-id="cbb32-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cbb32-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cbb32-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cbb32-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cbb32-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cbb32-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cbb32-107">Cree un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="cbb32-107">Create a new [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cbb32-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cbb32-108">Prerequisites</span></span>
<span data-ttu-id="cbb32-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cbb32-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cbb32-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cbb32-111">Permission type</span></span>|<span data-ttu-id="cbb32-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cbb32-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cbb32-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cbb32-113">Delegated (work or school account)</span></span>|<span data-ttu-id="cbb32-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cbb32-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="cbb32-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cbb32-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cbb32-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cbb32-116">Not supported.</span></span>|
|<span data-ttu-id="cbb32-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cbb32-117">Application</span></span>|<span data-ttu-id="cbb32-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cbb32-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cbb32-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cbb32-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/windowsInformationProtectionAppLearningSummaries
```

## <a name="request-headers"></a><span data-ttu-id="cbb32-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cbb32-120">Request headers</span></span>
|<span data-ttu-id="cbb32-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cbb32-121">Header</span></span>|<span data-ttu-id="cbb32-122">Valor</span><span class="sxs-lookup"><span data-stu-id="cbb32-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cbb32-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="cbb32-123">Authorization</span></span>|<span data-ttu-id="cbb32-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cbb32-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cbb32-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cbb32-125">Accept</span></span>|<span data-ttu-id="cbb32-126">application/json</span><span class="sxs-lookup"><span data-stu-id="cbb32-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cbb32-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cbb32-127">Request body</span></span>
<span data-ttu-id="cbb32-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="cbb32-128">In the request body, supply a JSON representation for the windowsInformationProtectionAppLearningSummary object.</span></span>

<span data-ttu-id="cbb32-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="cbb32-129">The following table shows the properties that are required when you create the windowsInformationProtectionAppLearningSummary.</span></span>

|<span data-ttu-id="cbb32-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cbb32-130">Property</span></span>|<span data-ttu-id="cbb32-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbb32-131">Type</span></span>|<span data-ttu-id="cbb32-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbb32-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cbb32-133">id</span><span class="sxs-lookup"><span data-stu-id="cbb32-133">id</span></span>|<span data-ttu-id="cbb32-134">String</span><span class="sxs-lookup"><span data-stu-id="cbb32-134">String</span></span>|<span data-ttu-id="cbb32-135">Identificador único para WindowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="cbb32-135">Unique Identifier for the WindowsInformationProtectionAppLearningSummary.</span></span>|
|<span data-ttu-id="cbb32-136">applicationName</span><span class="sxs-lookup"><span data-stu-id="cbb32-136">applicationName</span></span>|<span data-ttu-id="cbb32-137">String</span><span class="sxs-lookup"><span data-stu-id="cbb32-137">String</span></span>|<span data-ttu-id="cbb32-138">Nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="cbb32-138">Application Name</span></span>|
|<span data-ttu-id="cbb32-139">applicationType</span><span class="sxs-lookup"><span data-stu-id="cbb32-139">applicationType</span></span>|[<span data-ttu-id="cbb32-140">applicationType</span><span class="sxs-lookup"><span data-stu-id="cbb32-140">applicationType</span></span>](../resources/intune-wip-applicationtype.md)|<span data-ttu-id="cbb32-141">Tipo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="cbb32-141">Application Type.</span></span> <span data-ttu-id="cbb32-142">Los valores posibles son: `universal` y `desktop`.</span><span class="sxs-lookup"><span data-stu-id="cbb32-142">Possible values are: `universal`, `desktop`.</span></span>|
|<span data-ttu-id="cbb32-143">deviceCount</span><span class="sxs-lookup"><span data-stu-id="cbb32-143">deviceCount</span></span>|<span data-ttu-id="cbb32-144">Int32</span><span class="sxs-lookup"><span data-stu-id="cbb32-144">Int32</span></span>|<span data-ttu-id="cbb32-145">Recuento de dispositivos</span><span class="sxs-lookup"><span data-stu-id="cbb32-145">Device Count</span></span>|



## <a name="response"></a><span data-ttu-id="cbb32-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cbb32-146">Response</span></span>
<span data-ttu-id="cbb32-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cbb32-147">If successful, this method returns a `201 Created` response code and a [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cbb32-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cbb32-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="cbb32-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cbb32-149">Request</span></span>
<span data-ttu-id="cbb32-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cbb32-150">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/windowsInformationProtectionAppLearningSummaries
Content-type: application/json
Content-length: 191

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLearningSummary",
  "applicationName": "Application Name value",
  "applicationType": "desktop",
  "deviceCount": 11
}
```

### <a name="response"></a><span data-ttu-id="cbb32-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cbb32-151">Response</span></span>
<span data-ttu-id="cbb32-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cbb32-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





