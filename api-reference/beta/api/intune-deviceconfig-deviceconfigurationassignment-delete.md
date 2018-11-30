---
title: Eliminar deviceConfigurationAssignment
description: Elimina un deviceConfigurationAssignment.
ms.openlocfilehash: b1806b6508f0efdfc70f7dbb9fe3427a918c786d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27082927"
---
# <a name="delete-deviceconfigurationassignment"></a><span data-ttu-id="ad78a-103">Eliminar deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="ad78a-103">Delete deviceConfigurationAssignment</span></span>

> <span data-ttu-id="ad78a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ad78a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ad78a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ad78a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ad78a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ad78a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ad78a-107">Elimina un [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="ad78a-107">Deletes a [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ad78a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ad78a-108">Prerequisites</span></span>
<span data-ttu-id="ad78a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ad78a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ad78a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ad78a-111">Permission type</span></span>|<span data-ttu-id="ad78a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ad78a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ad78a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ad78a-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ad78a-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ad78a-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="ad78a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ad78a-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ad78a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ad78a-116">Not supported.</span></span>|
|<span data-ttu-id="ad78a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ad78a-117">Application</span></span>|<span data-ttu-id="ad78a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ad78a-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ad78a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ad78a-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/assignments/{deviceConfigurationAssignmentId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/rootCertificate/assignments/{deviceConfigurationAssignmentId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/assignments/{deviceConfigurationAssignmentId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/rootCertificate/assignments/{deviceConfigurationAssignmentId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/rootCertificate/assignments/{deviceConfigurationAssignmentId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSScepCertificateProfile/rootCertificate/assignments/{deviceConfigurationAssignmentId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsPhone81VpnConfiguration/identityCertificate/assignments/{deviceConfigurationAssignmentId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/assignments/{deviceConfigurationAssignmentId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/rootCertificatesForServerValidation/{windows81TrustedRootCertificateId}/assignments/{deviceConfigurationAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="ad78a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ad78a-120">Request headers</span></span>
|<span data-ttu-id="ad78a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad78a-121">Header</span></span>|<span data-ttu-id="ad78a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ad78a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ad78a-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="ad78a-123">Authorization</span></span>|<span data-ttu-id="ad78a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ad78a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ad78a-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ad78a-125">Accept</span></span>|<span data-ttu-id="ad78a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ad78a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ad78a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ad78a-127">Request body</span></span>
<span data-ttu-id="ad78a-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ad78a-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ad78a-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad78a-129">Response</span></span>
<span data-ttu-id="ad78a-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="ad78a-130">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="ad78a-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ad78a-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="ad78a-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ad78a-132">Request</span></span>
<span data-ttu-id="ad78a-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ad78a-133">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/assignments/{deviceConfigurationAssignmentId}
```

### <a name="response"></a><span data-ttu-id="ad78a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad78a-134">Response</span></span>
<span data-ttu-id="ad78a-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ad78a-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





