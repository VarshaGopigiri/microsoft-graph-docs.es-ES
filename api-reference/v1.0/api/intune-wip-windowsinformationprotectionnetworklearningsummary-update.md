---
title: Actualizar windowsInformationProtectionNetworkLearningSummary
description: Actualice las propiedades de un objeto windowsInformationProtectionNetworkLearningSummary.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 3d1268d077c9bfc32e5d85b85b103bc7a3e71f78
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27947109"
---
# <a name="update-windowsinformationprotectionnetworklearningsummary"></a><span data-ttu-id="3d80b-103">Actualizar windowsInformationProtectionNetworkLearningSummary</span><span class="sxs-lookup"><span data-stu-id="3d80b-103">Update windowsInformationProtectionNetworkLearningSummary</span></span>

> <span data-ttu-id="3d80b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3d80b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3d80b-105">Actualice las propiedades de un objeto [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="3d80b-105">Update the properties of a [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3d80b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3d80b-106">Prerequisites</span></span>
<span data-ttu-id="3d80b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3d80b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3d80b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3d80b-109">Permission type</span></span>|<span data-ttu-id="3d80b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3d80b-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3d80b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3d80b-111">Delegated (work or school account)</span></span>|<span data-ttu-id="3d80b-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3d80b-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="3d80b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3d80b-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3d80b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3d80b-114">Not supported.</span></span>|
|<span data-ttu-id="3d80b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3d80b-115">Application</span></span>|<span data-ttu-id="3d80b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3d80b-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3d80b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3d80b-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/windowsInformationProtectionNetworkLearningSummaries/{windowsInformationProtectionNetworkLearningSummaryId}
```

## <a name="request-headers"></a><span data-ttu-id="3d80b-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3d80b-118">Request headers</span></span>
|<span data-ttu-id="3d80b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d80b-119">Header</span></span>|<span data-ttu-id="3d80b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3d80b-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3d80b-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="3d80b-121">Authorization</span></span>|<span data-ttu-id="3d80b-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3d80b-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3d80b-123">Accept</span><span class="sxs-lookup"><span data-stu-id="3d80b-123">Accept</span></span>|<span data-ttu-id="3d80b-124">application/json</span><span class="sxs-lookup"><span data-stu-id="3d80b-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3d80b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3d80b-125">Request body</span></span>
<span data-ttu-id="3d80b-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="3d80b-126">In the request body, supply a JSON representation for the [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) object.</span></span>

<span data-ttu-id="3d80b-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="3d80b-127">The following table shows the properties that are required when you create the [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md).</span></span>

|<span data-ttu-id="3d80b-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3d80b-128">Property</span></span>|<span data-ttu-id="3d80b-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="3d80b-129">Type</span></span>|<span data-ttu-id="3d80b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d80b-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3d80b-131">id</span><span class="sxs-lookup"><span data-stu-id="3d80b-131">id</span></span>|<span data-ttu-id="3d80b-132">String</span><span class="sxs-lookup"><span data-stu-id="3d80b-132">String</span></span>|<span data-ttu-id="3d80b-133">Identificador único para WindowsInformationProtectionNetworkLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="3d80b-133">Unique Identifier for the WindowsInformationProtectionNetworkLearningSummary.</span></span>|
|<span data-ttu-id="3d80b-134">url</span><span class="sxs-lookup"><span data-stu-id="3d80b-134">url</span></span>|<span data-ttu-id="3d80b-135">String</span><span class="sxs-lookup"><span data-stu-id="3d80b-135">String</span></span>|<span data-ttu-id="3d80b-136">Dirección URL del sitio web</span><span class="sxs-lookup"><span data-stu-id="3d80b-136">Website url</span></span>|
|<span data-ttu-id="3d80b-137">deviceCount</span><span class="sxs-lookup"><span data-stu-id="3d80b-137">deviceCount</span></span>|<span data-ttu-id="3d80b-138">Int32</span><span class="sxs-lookup"><span data-stu-id="3d80b-138">Int32</span></span>|<span data-ttu-id="3d80b-139">Recuento de dispositivos</span><span class="sxs-lookup"><span data-stu-id="3d80b-139">Device Count</span></span>|



## <a name="response"></a><span data-ttu-id="3d80b-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3d80b-140">Response</span></span>
<span data-ttu-id="3d80b-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3d80b-141">If successful, this method returns a `200 OK` response code and an updated [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3d80b-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3d80b-142">Example</span></span>
### <a name="request"></a><span data-ttu-id="3d80b-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3d80b-143">Request</span></span>
<span data-ttu-id="3d80b-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3d80b-144">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/windowsInformationProtectionNetworkLearningSummaries/{windowsInformationProtectionNetworkLearningSummaryId}
Content-type: application/json
Content-length: 137

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionNetworkLearningSummary",
  "url": "Url value",
  "deviceCount": 11
}
```

### <a name="response"></a><span data-ttu-id="3d80b-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3d80b-145">Response</span></span>
<span data-ttu-id="3d80b-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3d80b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



