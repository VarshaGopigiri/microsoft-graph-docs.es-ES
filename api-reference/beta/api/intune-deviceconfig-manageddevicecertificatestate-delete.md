---
title: Eliminar managedDeviceCertificateState
description: Elimina un managedDeviceCertificateState.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 5184ec7723caf6d22e657c13766f78a2922c2645
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27877605"
---
# <a name="delete-manageddevicecertificatestate"></a><span data-ttu-id="2597f-103">Eliminar managedDeviceCertificateState</span><span class="sxs-lookup"><span data-stu-id="2597f-103">Delete managedDeviceCertificateState</span></span>

> <span data-ttu-id="2597f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2597f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2597f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2597f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2597f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2597f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2597f-107">Elimina un [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md).</span><span class="sxs-lookup"><span data-stu-id="2597f-107">Deletes a [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2597f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2597f-108">Prerequisites</span></span>
<span data-ttu-id="2597f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2597f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2597f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2597f-111">Permission type</span></span>|<span data-ttu-id="2597f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2597f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2597f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2597f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="2597f-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2597f-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="2597f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2597f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2597f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2597f-116">Not supported.</span></span>|
|<span data-ttu-id="2597f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2597f-117">Application</span></span>|<span data-ttu-id="2597f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2597f-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2597f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2597f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosPkcsCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSScepCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidPkcsCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidScepCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosImportedPFXCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSImportedPFXCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidImportedPFXCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidWorkProfileScepCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidForWorkImportedPFXCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/microsoft.graph.androidForWorkPkcsCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/microsoft.graph.androidForWorkScepCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsPhone81VpnConfiguration/identityCertificate/microsoft.graph.windowsPhone81SCEPCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windows10PkcsCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windows81SCEPCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windows10ImportedPFXCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windowsPhone81ImportedPFXCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
```

## <a name="request-headers"></a><span data-ttu-id="2597f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2597f-120">Request headers</span></span>
|<span data-ttu-id="2597f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2597f-121">Header</span></span>|<span data-ttu-id="2597f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2597f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2597f-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="2597f-123">Authorization</span></span>|<span data-ttu-id="2597f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2597f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2597f-125">Accept</span><span class="sxs-lookup"><span data-stu-id="2597f-125">Accept</span></span>|<span data-ttu-id="2597f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2597f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2597f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2597f-127">Request body</span></span>
<span data-ttu-id="2597f-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2597f-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2597f-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2597f-129">Response</span></span>
<span data-ttu-id="2597f-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="2597f-130">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="2597f-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2597f-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="2597f-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2597f-132">Request</span></span>
<span data-ttu-id="2597f-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2597f-133">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosPkcsCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
```

### <a name="response"></a><span data-ttu-id="2597f-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2597f-134">Response</span></span>
<span data-ttu-id="2597f-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2597f-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





