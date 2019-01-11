---
title: Eliminar windowsDomainJoinConfiguration
description: Elimina un windowsDomainJoinConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 04ef2c85351614533e21a107e8e1cbf9636bd753
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27821724"
---
# <a name="delete-windowsdomainjoinconfiguration"></a><span data-ttu-id="e6c04-103">Eliminar windowsDomainJoinConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6c04-103">Delete windowsDomainJoinConfiguration</span></span>

> <span data-ttu-id="e6c04-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e6c04-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e6c04-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e6c04-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e6c04-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e6c04-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e6c04-107">Elimina un [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="e6c04-107">Deletes a [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e6c04-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e6c04-108">Prerequisites</span></span>
<span data-ttu-id="e6c04-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e6c04-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e6c04-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e6c04-111">Permission type</span></span>|<span data-ttu-id="e6c04-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e6c04-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e6c04-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e6c04-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="e6c04-114">&nbsp; &nbsp; **Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="e6c04-114">&nbsp; &nbsp; **Device configuration**</span></span> | <span data-ttu-id="e6c04-115">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e6c04-115">DeviceManagementConfiguration.ReadWrite.All</span></span> |
|<span data-ttu-id="e6c04-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e6c04-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e6c04-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6c04-117">Not supported.</span></span>|
|<span data-ttu-id="e6c04-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e6c04-118">Application</span></span>|<span data-ttu-id="e6c04-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6c04-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e6c04-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e6c04-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="e6c04-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e6c04-121">Request headers</span></span>
|<span data-ttu-id="e6c04-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6c04-122">Header</span></span>|<span data-ttu-id="e6c04-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e6c04-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e6c04-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="e6c04-124">Authorization</span></span>|<span data-ttu-id="e6c04-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e6c04-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e6c04-126">Accept</span><span class="sxs-lookup"><span data-stu-id="e6c04-126">Accept</span></span>|<span data-ttu-id="e6c04-127">application/json</span><span class="sxs-lookup"><span data-stu-id="e6c04-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e6c04-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e6c04-128">Request body</span></span>
<span data-ttu-id="e6c04-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e6c04-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e6c04-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6c04-130">Response</span></span>
<span data-ttu-id="e6c04-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="e6c04-131">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="e6c04-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e6c04-132">Example</span></span>
### <a name="request"></a><span data-ttu-id="e6c04-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e6c04-133">Request</span></span>
<span data-ttu-id="e6c04-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e6c04-134">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="e6c04-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6c04-135">Response</span></span>
<span data-ttu-id="e6c04-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e6c04-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



