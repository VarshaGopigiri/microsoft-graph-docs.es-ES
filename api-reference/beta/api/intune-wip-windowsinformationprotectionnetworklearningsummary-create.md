---
title: Crear windowsInformationProtectionNetworkLearningSummary
description: Cree un objeto windowsInformationProtectionNetworkLearningSummary.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 59b55111a022c1172abb9ab9f65ccf23e153c8cd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27915532"
---
# <a name="create-windowsinformationprotectionnetworklearningsummary"></a><span data-ttu-id="1ad62-103">Crear windowsInformationProtectionNetworkLearningSummary</span><span class="sxs-lookup"><span data-stu-id="1ad62-103">Create windowsInformationProtectionNetworkLearningSummary</span></span>

> <span data-ttu-id="1ad62-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1ad62-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1ad62-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1ad62-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1ad62-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1ad62-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1ad62-107">Cree un objeto [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="1ad62-107">Create a new [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1ad62-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1ad62-108">Prerequisites</span></span>
<span data-ttu-id="1ad62-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1ad62-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1ad62-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1ad62-111">Permission type</span></span>|<span data-ttu-id="1ad62-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1ad62-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1ad62-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1ad62-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1ad62-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1ad62-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="1ad62-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1ad62-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1ad62-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1ad62-116">Not supported.</span></span>|
|<span data-ttu-id="1ad62-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1ad62-117">Application</span></span>|<span data-ttu-id="1ad62-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1ad62-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1ad62-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1ad62-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/windowsInformationProtectionNetworkLearningSummaries
```

## <a name="request-headers"></a><span data-ttu-id="1ad62-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1ad62-120">Request headers</span></span>
|<span data-ttu-id="1ad62-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ad62-121">Header</span></span>|<span data-ttu-id="1ad62-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1ad62-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1ad62-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="1ad62-123">Authorization</span></span>|<span data-ttu-id="1ad62-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1ad62-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1ad62-125">Accept</span><span class="sxs-lookup"><span data-stu-id="1ad62-125">Accept</span></span>|<span data-ttu-id="1ad62-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1ad62-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1ad62-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1ad62-127">Request body</span></span>
<span data-ttu-id="1ad62-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsInformationProtectionNetworkLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="1ad62-128">In the request body, supply a JSON representation for the windowsInformationProtectionNetworkLearningSummary object.</span></span>

<span data-ttu-id="1ad62-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsInformationProtectionNetworkLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="1ad62-129">The following table shows the properties that are required when you create the windowsInformationProtectionNetworkLearningSummary.</span></span>

|<span data-ttu-id="1ad62-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1ad62-130">Property</span></span>|<span data-ttu-id="1ad62-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="1ad62-131">Type</span></span>|<span data-ttu-id="1ad62-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ad62-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1ad62-133">id</span><span class="sxs-lookup"><span data-stu-id="1ad62-133">id</span></span>|<span data-ttu-id="1ad62-134">String</span><span class="sxs-lookup"><span data-stu-id="1ad62-134">String</span></span>|<span data-ttu-id="1ad62-135">Identificador único para WindowsInformationProtectionNetworkLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="1ad62-135">Unique Identifier for the WindowsInformationProtectionNetworkLearningSummary.</span></span>|
|<span data-ttu-id="1ad62-136">url</span><span class="sxs-lookup"><span data-stu-id="1ad62-136">url</span></span>|<span data-ttu-id="1ad62-137">String</span><span class="sxs-lookup"><span data-stu-id="1ad62-137">String</span></span>|<span data-ttu-id="1ad62-138">Dirección URL del sitio web</span><span class="sxs-lookup"><span data-stu-id="1ad62-138">Website url</span></span>|
|<span data-ttu-id="1ad62-139">deviceCount</span><span class="sxs-lookup"><span data-stu-id="1ad62-139">deviceCount</span></span>|<span data-ttu-id="1ad62-140">Int32</span><span class="sxs-lookup"><span data-stu-id="1ad62-140">Int32</span></span>|<span data-ttu-id="1ad62-141">Recuento de dispositivos</span><span class="sxs-lookup"><span data-stu-id="1ad62-141">Device Count</span></span>|



## <a name="response"></a><span data-ttu-id="1ad62-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1ad62-142">Response</span></span>
<span data-ttu-id="1ad62-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1ad62-143">If successful, this method returns a `201 Created` response code and a [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1ad62-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1ad62-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="1ad62-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1ad62-145">Request</span></span>
<span data-ttu-id="1ad62-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1ad62-146">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/windowsInformationProtectionNetworkLearningSummaries
Content-type: application/json
Content-length: 137

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionNetworkLearningSummary",
  "url": "Url value",
  "deviceCount": 11
}
```

### <a name="response"></a><span data-ttu-id="1ad62-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1ad62-147">Response</span></span>
<span data-ttu-id="1ad62-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1ad62-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 186

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionNetworkLearningSummary",
  "id": "242108f7-08f7-2421-f708-2124f7082124",
  "url": "Url value",
  "deviceCount": 11
}
```





