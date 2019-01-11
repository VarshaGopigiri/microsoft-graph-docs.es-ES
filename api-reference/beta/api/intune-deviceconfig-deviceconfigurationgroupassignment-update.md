---
title: Actualizar deviceConfigurationGroupAssignment
description: Actualizar las propiedades de un objeto deviceConfigurationGroupAssignment.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 4742cfb5fb61b94eda6b299927160d0e51f6ab98
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822993"
---
# <a name="update-deviceconfigurationgroupassignment"></a><span data-ttu-id="b15f4-103">Actualizar deviceConfigurationGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="b15f4-103">Update deviceConfigurationGroupAssignment</span></span>

> <span data-ttu-id="b15f4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b15f4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b15f4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b15f4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b15f4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b15f4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b15f4-107">Actualizar las propiedades de un objeto [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="b15f4-107">Update the properties of a [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b15f4-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b15f4-108">Prerequisites</span></span>
<span data-ttu-id="b15f4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b15f4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b15f4-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b15f4-111">Permission type</span></span>|<span data-ttu-id="b15f4-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b15f4-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b15f4-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b15f4-113">Delegated (work or school account)</span></span>|<span data-ttu-id="b15f4-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b15f4-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="b15f4-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b15f4-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b15f4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b15f4-116">Not supported.</span></span>|
|<span data-ttu-id="b15f4-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b15f4-117">Application</span></span>|<span data-ttu-id="b15f4-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b15f4-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b15f4-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b15f4-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/rootCertificate/groupAssignments/{deviceConfigurationGroupAssignmentId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/groupAssignments/{deviceConfigurationGroupAssignmentId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/rootCertificate/groupAssignments/{deviceConfigurationGroupAssignmentId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/rootCertificate/groupAssignments/{deviceConfigurationGroupAssignmentId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSScepCertificateProfile/rootCertificate/groupAssignments/{deviceConfigurationGroupAssignmentId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsPhone81VpnConfiguration/identityCertificate/groupAssignments/{deviceConfigurationGroupAssignmentId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/groupAssignments/{deviceConfigurationGroupAssignmentId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/rootCertificatesForServerValidation/{windows81TrustedRootCertificateId}/groupAssignments/{deviceConfigurationGroupAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="b15f4-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b15f4-120">Request headers</span></span>
|<span data-ttu-id="b15f4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b15f4-121">Header</span></span>|<span data-ttu-id="b15f4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b15f4-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b15f4-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="b15f4-123">Authorization</span></span>|<span data-ttu-id="b15f4-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b15f4-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b15f4-125">Accept</span><span class="sxs-lookup"><span data-stu-id="b15f4-125">Accept</span></span>|<span data-ttu-id="b15f4-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b15f4-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b15f4-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b15f4-127">Request body</span></span>
<span data-ttu-id="b15f4-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="b15f4-128">In the request body, supply a JSON representation for the [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) object.</span></span>

<span data-ttu-id="b15f4-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md).</span><span class="sxs-lookup"><span data-stu-id="b15f4-129">The following table shows the properties that are required when you create the [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md).</span></span>

|<span data-ttu-id="b15f4-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b15f4-130">Property</span></span>|<span data-ttu-id="b15f4-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="b15f4-131">Type</span></span>|<span data-ttu-id="b15f4-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="b15f4-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b15f4-133">id</span><span class="sxs-lookup"><span data-stu-id="b15f4-133">id</span></span>|<span data-ttu-id="b15f4-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="b15f4-134">String</span></span>|<span data-ttu-id="b15f4-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b15f4-135">Key of the entity.</span></span>|
|<span data-ttu-id="b15f4-136">targetGroupId</span><span class="sxs-lookup"><span data-stu-id="b15f4-136">targetGroupId</span></span>|<span data-ttu-id="b15f4-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="b15f4-137">String</span></span>|<span data-ttu-id="b15f4-138">El identificador del grupo AAD, nuestro destino son para la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b15f4-138">The Id of the AAD group we are targeting the device configuration to.</span></span>|
|<span data-ttu-id="b15f4-139">excludeGroup</span><span class="sxs-lookup"><span data-stu-id="b15f4-139">excludeGroup</span></span>|<span data-ttu-id="b15f4-140">Booleano</span><span class="sxs-lookup"><span data-stu-id="b15f4-140">Boolean</span></span>|<span data-ttu-id="b15f4-141">Indica si este grupo se deben excluir.</span><span class="sxs-lookup"><span data-stu-id="b15f4-141">Indicates if this group is should be excluded.</span></span> <span data-ttu-id="b15f4-142">Valores predeterminados que se debe incluir en el grupo</span><span class="sxs-lookup"><span data-stu-id="b15f4-142">Defaults that the group should be included</span></span>|



## <a name="response"></a><span data-ttu-id="b15f4-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b15f4-143">Response</span></span>
<span data-ttu-id="b15f4-144">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b15f4-144">If successful, this method returns a `200 OK` response code and an updated [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b15f4-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b15f4-145">Example</span></span>
### <a name="request"></a><span data-ttu-id="b15f4-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b15f4-146">Request</span></span>
<span data-ttu-id="b15f4-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b15f4-147">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}
Content-type: application/json
Content-length: 73

{
  "targetGroupId": "Target Group Id value",
  "excludeGroup": true
}
```

### <a name="response"></a><span data-ttu-id="b15f4-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b15f4-148">Response</span></span>
<span data-ttu-id="b15f4-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b15f4-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 195

{
  "@odata.type": "#microsoft.graph.deviceConfigurationGroupAssignment",
  "id": "561d26c5-26c5-561d-c526-1d56c5261d56",
  "targetGroupId": "Target Group Id value",
  "excludeGroup": true
}
```





