---
title: Crear windowsInformationProtectionNetworkLearningSummary
description: Cree un objeto windowsInformationProtectionNetworkLearningSummary.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: f3cb295fd24b70b4d40464218532fd1298fd2ab1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27841506"
---
# <a name="create-windowsinformationprotectionnetworklearningsummary"></a><span data-ttu-id="63b1e-103">Crear windowsInformationProtectionNetworkLearningSummary</span><span class="sxs-lookup"><span data-stu-id="63b1e-103">Create windowsInformationProtectionNetworkLearningSummary</span></span>

> <span data-ttu-id="63b1e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="63b1e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="63b1e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="63b1e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="63b1e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="63b1e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="63b1e-107">Cree un objeto [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="63b1e-107">Create a new [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="63b1e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="63b1e-108">Prerequisites</span></span>
<span data-ttu-id="63b1e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="63b1e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="63b1e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="63b1e-111">Permission type</span></span>|<span data-ttu-id="63b1e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="63b1e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="63b1e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="63b1e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="63b1e-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="63b1e-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="63b1e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="63b1e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="63b1e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63b1e-116">Not supported.</span></span>|
|<span data-ttu-id="63b1e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="63b1e-117">Application</span></span>|<span data-ttu-id="63b1e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63b1e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="63b1e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="63b1e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/windowsInformationProtectionNetworkLearningSummaries
```

## <a name="request-headers"></a><span data-ttu-id="63b1e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="63b1e-120">Request headers</span></span>
|<span data-ttu-id="63b1e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63b1e-121">Header</span></span>|<span data-ttu-id="63b1e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="63b1e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="63b1e-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="63b1e-123">Authorization</span></span>|<span data-ttu-id="63b1e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="63b1e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="63b1e-125">Accept</span><span class="sxs-lookup"><span data-stu-id="63b1e-125">Accept</span></span>|<span data-ttu-id="63b1e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="63b1e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="63b1e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="63b1e-127">Request body</span></span>
<span data-ttu-id="63b1e-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsInformationProtectionNetworkLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="63b1e-128">In the request body, supply a JSON representation for the windowsInformationProtectionNetworkLearningSummary object.</span></span>

<span data-ttu-id="63b1e-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsInformationProtectionNetworkLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="63b1e-129">The following table shows the properties that are required when you create the windowsInformationProtectionNetworkLearningSummary.</span></span>

|<span data-ttu-id="63b1e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="63b1e-130">Property</span></span>|<span data-ttu-id="63b1e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="63b1e-131">Type</span></span>|<span data-ttu-id="63b1e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="63b1e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="63b1e-133">id</span><span class="sxs-lookup"><span data-stu-id="63b1e-133">id</span></span>|<span data-ttu-id="63b1e-134">String</span><span class="sxs-lookup"><span data-stu-id="63b1e-134">String</span></span>|<span data-ttu-id="63b1e-135">Identificador único para WindowsInformationProtectionNetworkLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="63b1e-135">Unique Identifier for the WindowsInformationProtectionNetworkLearningSummary.</span></span>|
|<span data-ttu-id="63b1e-136">url</span><span class="sxs-lookup"><span data-stu-id="63b1e-136">url</span></span>|<span data-ttu-id="63b1e-137">String</span><span class="sxs-lookup"><span data-stu-id="63b1e-137">String</span></span>|<span data-ttu-id="63b1e-138">Dirección URL del sitio web</span><span class="sxs-lookup"><span data-stu-id="63b1e-138">Website url</span></span>|
|<span data-ttu-id="63b1e-139">deviceCount</span><span class="sxs-lookup"><span data-stu-id="63b1e-139">deviceCount</span></span>|<span data-ttu-id="63b1e-140">Int32</span><span class="sxs-lookup"><span data-stu-id="63b1e-140">Int32</span></span>|<span data-ttu-id="63b1e-141">Recuento de dispositivos</span><span class="sxs-lookup"><span data-stu-id="63b1e-141">Device Count</span></span>|



## <a name="response"></a><span data-ttu-id="63b1e-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63b1e-142">Response</span></span>
<span data-ttu-id="63b1e-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63b1e-143">If successful, this method returns a `201 Created` response code and a [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="63b1e-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="63b1e-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="63b1e-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="63b1e-145">Request</span></span>
<span data-ttu-id="63b1e-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63b1e-146">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="63b1e-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63b1e-147">Response</span></span>
<span data-ttu-id="63b1e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="63b1e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





