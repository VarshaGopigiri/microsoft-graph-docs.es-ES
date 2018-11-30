---
title: Actualizar windowsInformationProtectionNetworkLearningSummary
description: Actualice las propiedades de un objeto windowsInformationProtectionNetworkLearningSummary.
ms.openlocfilehash: ade11aa7dfdbe9f189923ad470d411e19a50fb51
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087883"
---
# <a name="update-windowsinformationprotectionnetworklearningsummary"></a><span data-ttu-id="9b6aa-103">Actualizar windowsInformationProtectionNetworkLearningSummary</span><span class="sxs-lookup"><span data-stu-id="9b6aa-103">Update windowsInformationProtectionNetworkLearningSummary</span></span>

> <span data-ttu-id="9b6aa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9b6aa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9b6aa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9b6aa-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9b6aa-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9b6aa-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9b6aa-107">Actualice las propiedades de un objeto [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="9b6aa-107">Update the properties of a [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9b6aa-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9b6aa-108">Prerequisites</span></span>
<span data-ttu-id="9b6aa-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9b6aa-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9b6aa-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9b6aa-111">Permission type</span></span>|<span data-ttu-id="9b6aa-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9b6aa-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9b6aa-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9b6aa-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9b6aa-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9b6aa-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="9b6aa-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9b6aa-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9b6aa-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b6aa-116">Not supported.</span></span>|
|<span data-ttu-id="9b6aa-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9b6aa-117">Application</span></span>|<span data-ttu-id="9b6aa-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b6aa-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9b6aa-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b6aa-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/windowsInformationProtectionNetworkLearningSummaries/{windowsInformationProtectionNetworkLearningSummaryId}
```

## <a name="request-headers"></a><span data-ttu-id="9b6aa-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b6aa-120">Request headers</span></span>
|<span data-ttu-id="9b6aa-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b6aa-121">Header</span></span>|<span data-ttu-id="9b6aa-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9b6aa-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9b6aa-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="9b6aa-123">Authorization</span></span>|<span data-ttu-id="9b6aa-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9b6aa-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9b6aa-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9b6aa-125">Accept</span></span>|<span data-ttu-id="9b6aa-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9b6aa-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9b6aa-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9b6aa-127">Request body</span></span>
<span data-ttu-id="9b6aa-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="9b6aa-128">In the request body, supply a JSON representation for the [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) object.</span></span>

<span data-ttu-id="9b6aa-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="9b6aa-129">The following table shows the properties that are required when you create the [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md).</span></span>

|<span data-ttu-id="9b6aa-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9b6aa-130">Property</span></span>|<span data-ttu-id="9b6aa-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b6aa-131">Type</span></span>|<span data-ttu-id="9b6aa-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b6aa-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9b6aa-133">id</span><span class="sxs-lookup"><span data-stu-id="9b6aa-133">id</span></span>|<span data-ttu-id="9b6aa-134">String</span><span class="sxs-lookup"><span data-stu-id="9b6aa-134">String</span></span>|<span data-ttu-id="9b6aa-135">Identificador único para WindowsInformationProtectionNetworkLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="9b6aa-135">Unique Identifier for the WindowsInformationProtectionNetworkLearningSummary.</span></span>|
|<span data-ttu-id="9b6aa-136">url</span><span class="sxs-lookup"><span data-stu-id="9b6aa-136">url</span></span>|<span data-ttu-id="9b6aa-137">String</span><span class="sxs-lookup"><span data-stu-id="9b6aa-137">String</span></span>|<span data-ttu-id="9b6aa-138">Dirección URL del sitio web</span><span class="sxs-lookup"><span data-stu-id="9b6aa-138">Website url</span></span>|
|<span data-ttu-id="9b6aa-139">deviceCount</span><span class="sxs-lookup"><span data-stu-id="9b6aa-139">deviceCount</span></span>|<span data-ttu-id="9b6aa-140">Int32</span><span class="sxs-lookup"><span data-stu-id="9b6aa-140">Int32</span></span>|<span data-ttu-id="9b6aa-141">Recuento de dispositivos</span><span class="sxs-lookup"><span data-stu-id="9b6aa-141">Device Count</span></span>|



## <a name="response"></a><span data-ttu-id="9b6aa-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b6aa-142">Response</span></span>
<span data-ttu-id="9b6aa-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b6aa-143">If successful, this method returns a `200 OK` response code and an updated [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9b6aa-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b6aa-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="9b6aa-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9b6aa-145">Request</span></span>
<span data-ttu-id="9b6aa-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9b6aa-146">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/windowsInformationProtectionNetworkLearningSummaries/{windowsInformationProtectionNetworkLearningSummaryId}
Content-type: application/json
Content-length: 48

{
  "url": "Url value",
  "deviceCount": 11
}
```

### <a name="response"></a><span data-ttu-id="9b6aa-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b6aa-147">Response</span></span>
<span data-ttu-id="9b6aa-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9b6aa-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 186

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionNetworkLearningSummary",
  "id": "242108f7-08f7-2421-f708-2124f7082124",
  "url": "Url value",
  "deviceCount": 11
}
```





