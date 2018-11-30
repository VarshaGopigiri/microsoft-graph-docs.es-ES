---
title: Crear deviceConfigurationGroupAssignment
description: Crear un nuevo objeto deviceConfigurationGroupAssignment.
ms.openlocfilehash: 3e349664a1458b13be357dbabf7e9a1a8e14025e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084224"
---
# <a name="create-deviceconfigurationgroupassignment"></a><span data-ttu-id="b8760-103">Crear deviceConfigurationGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="b8760-103">Create deviceConfigurationGroupAssignment</span></span>

> <span data-ttu-id="b8760-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b8760-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b8760-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b8760-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b8760-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b8760-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b8760-107">Crear un nuevo objeto [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="b8760-107">Create a new [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b8760-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b8760-108">Prerequisites</span></span>
<span data-ttu-id="b8760-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b8760-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b8760-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b8760-111">Permission type</span></span>|<span data-ttu-id="b8760-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b8760-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b8760-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b8760-113">Delegated (work or school account)</span></span>|<span data-ttu-id="b8760-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b8760-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="b8760-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b8760-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b8760-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b8760-116">Not supported.</span></span>|
|<span data-ttu-id="b8760-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b8760-117">Application</span></span>|<span data-ttu-id="b8760-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b8760-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b8760-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b8760-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/rootCertificate/groupAssignments
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/groupAssignments
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/rootCertificate/groupAssignments
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/rootCertificate/groupAssignments
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSScepCertificateProfile/rootCertificate/groupAssignments
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsPhone81VpnConfiguration/identityCertificate/groupAssignments
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/groupAssignments
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/rootCertificatesForServerValidation/{windows81TrustedRootCertificateId}/groupAssignments
```

## <a name="request-headers"></a><span data-ttu-id="b8760-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b8760-120">Request headers</span></span>
|<span data-ttu-id="b8760-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8760-121">Header</span></span>|<span data-ttu-id="b8760-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b8760-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b8760-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="b8760-123">Authorization</span></span>|<span data-ttu-id="b8760-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b8760-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b8760-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b8760-125">Accept</span></span>|<span data-ttu-id="b8760-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b8760-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b8760-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b8760-127">Request body</span></span>
<span data-ttu-id="b8760-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto deviceConfigurationGroupAssignment.</span><span class="sxs-lookup"><span data-stu-id="b8760-128">In the request body, supply a JSON representation for the deviceConfigurationGroupAssignment object.</span></span>

<span data-ttu-id="b8760-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el deviceConfigurationGroupAssignment.</span><span class="sxs-lookup"><span data-stu-id="b8760-129">The following table shows the properties that are required when you create the deviceConfigurationGroupAssignment.</span></span>

|<span data-ttu-id="b8760-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b8760-130">Property</span></span>|<span data-ttu-id="b8760-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8760-131">Type</span></span>|<span data-ttu-id="b8760-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8760-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b8760-133">id</span><span class="sxs-lookup"><span data-stu-id="b8760-133">id</span></span>|<span data-ttu-id="b8760-134">String</span><span class="sxs-lookup"><span data-stu-id="b8760-134">String</span></span>|<span data-ttu-id="b8760-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b8760-135">Key of the entity.</span></span>|
|<span data-ttu-id="b8760-136">targetGroupId</span><span class="sxs-lookup"><span data-stu-id="b8760-136">targetGroupId</span></span>|<span data-ttu-id="b8760-137">String</span><span class="sxs-lookup"><span data-stu-id="b8760-137">String</span></span>|<span data-ttu-id="b8760-138">El identificador del grupo AAD, nuestro destino son para la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b8760-138">The Id of the AAD group we are targeting the device configuration to.</span></span>|
|<span data-ttu-id="b8760-139">excludeGroup</span><span class="sxs-lookup"><span data-stu-id="b8760-139">excludeGroup</span></span>|<span data-ttu-id="b8760-140">Booleano</span><span class="sxs-lookup"><span data-stu-id="b8760-140">Boolean</span></span>|<span data-ttu-id="b8760-141">Indica si este grupo se deben excluir.</span><span class="sxs-lookup"><span data-stu-id="b8760-141">Indicates if this group is should be excluded.</span></span> <span data-ttu-id="b8760-142">Valores predeterminados que se debe incluir en el grupo</span><span class="sxs-lookup"><span data-stu-id="b8760-142">Defaults that the group should be included</span></span>|



## <a name="response"></a><span data-ttu-id="b8760-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b8760-143">Response</span></span>
<span data-ttu-id="b8760-144">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b8760-144">If successful, this method returns a `201 Created` response code and a [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b8760-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b8760-145">Example</span></span>
### <a name="request"></a><span data-ttu-id="b8760-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b8760-146">Request</span></span>
<span data-ttu-id="b8760-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b8760-147">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments
Content-type: application/json
Content-length: 146

{
  "@odata.type": "#microsoft.graph.deviceConfigurationGroupAssignment",
  "targetGroupId": "Target Group Id value",
  "excludeGroup": true
}
```

### <a name="response"></a><span data-ttu-id="b8760-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b8760-148">Response</span></span>
<span data-ttu-id="b8760-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b8760-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 195

{
  "@odata.type": "#microsoft.graph.deviceConfigurationGroupAssignment",
  "id": "561d26c5-26c5-561d-c526-1d56c5261d56",
  "targetGroupId": "Target Group Id value",
  "excludeGroup": true
}
```





