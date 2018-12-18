---
title: Eliminar iosEnterpriseWiFiConfiguration
description: Elimina un iosEnterpriseWiFiConfiguration.
author: tfitzmac
ms.openlocfilehash: 043890a5789151f4865f969593135c98261a70d2
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27352356"
---
# <a name="delete-iosenterprisewificonfiguration"></a><span data-ttu-id="ce434-103">Eliminar iosEnterpriseWiFiConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce434-103">Delete iosEnterpriseWiFiConfiguration</span></span>

> <span data-ttu-id="ce434-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ce434-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ce434-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ce434-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ce434-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ce434-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ce434-107">Elimina un [iosEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-iosenterprisewificonfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ce434-107">Deletes a [iosEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-iosenterprisewificonfiguration.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ce434-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ce434-108">Prerequisites</span></span>
<span data-ttu-id="ce434-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ce434-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ce434-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ce434-111">Permission type</span></span>|<span data-ttu-id="ce434-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ce434-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ce434-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ce434-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ce434-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ce434-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="ce434-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ce434-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ce434-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ce434-116">Not supported.</span></span>|
|<span data-ttu-id="ce434-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ce434-117">Application</span></span>|<span data-ttu-id="ce434-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ce434-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ce434-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ce434-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="ce434-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ce434-120">Request headers</span></span>
|<span data-ttu-id="ce434-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce434-121">Header</span></span>|<span data-ttu-id="ce434-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ce434-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ce434-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="ce434-123">Authorization</span></span>|<span data-ttu-id="ce434-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ce434-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ce434-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ce434-125">Accept</span></span>|<span data-ttu-id="ce434-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ce434-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ce434-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ce434-127">Request body</span></span>
<span data-ttu-id="ce434-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ce434-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ce434-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ce434-129">Response</span></span>
<span data-ttu-id="ce434-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="ce434-130">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="ce434-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ce434-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="ce434-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ce434-132">Request</span></span>
<span data-ttu-id="ce434-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ce434-133">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="ce434-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ce434-134">Response</span></span>
<span data-ttu-id="ce434-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ce434-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





