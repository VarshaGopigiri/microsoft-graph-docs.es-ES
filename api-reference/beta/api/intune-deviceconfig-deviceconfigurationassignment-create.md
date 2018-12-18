---
title: Crear deviceConfigurationAssignment
description: Cree un objeto deviceConfigurationAssignment.
author: tfitzmac
ms.openlocfilehash: 87d5ba51fce59340b869e6b78b7227546ab67df1
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27321451"
---
# <a name="create-deviceconfigurationassignment"></a><span data-ttu-id="e7576-103">Crear deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="e7576-103">Create deviceConfigurationAssignment</span></span>

> <span data-ttu-id="e7576-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e7576-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e7576-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e7576-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e7576-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e7576-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e7576-107">Cree un objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="e7576-107">Create a new [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e7576-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e7576-108">Prerequisites</span></span>
<span data-ttu-id="e7576-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e7576-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e7576-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e7576-111">Permission type</span></span>|<span data-ttu-id="e7576-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e7576-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e7576-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e7576-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e7576-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e7576-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="e7576-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e7576-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e7576-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e7576-116">Not supported.</span></span>|
|<span data-ttu-id="e7576-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e7576-117">Application</span></span>|<span data-ttu-id="e7576-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e7576-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e7576-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e7576-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/assignments
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/rootCertificate/assignments
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/assignments
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/rootCertificate/assignments
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/rootCertificate/assignments
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSScepCertificateProfile/rootCertificate/assignments
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsPhone81VpnConfiguration/identityCertificate/assignments
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/assignments
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/rootCertificatesForServerValidation/{windows81TrustedRootCertificateId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="e7576-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e7576-120">Request headers</span></span>
|<span data-ttu-id="e7576-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7576-121">Header</span></span>|<span data-ttu-id="e7576-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e7576-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e7576-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="e7576-123">Authorization</span></span>|<span data-ttu-id="e7576-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e7576-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e7576-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e7576-125">Accept</span></span>|<span data-ttu-id="e7576-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e7576-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e7576-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e7576-127">Request body</span></span>
<span data-ttu-id="e7576-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceConfigurationAssignment.</span><span class="sxs-lookup"><span data-stu-id="e7576-128">In the request body, supply a JSON representation for the deviceConfigurationAssignment object.</span></span>

<span data-ttu-id="e7576-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceConfigurationAssignment.</span><span class="sxs-lookup"><span data-stu-id="e7576-129">The following table shows the properties that are required when you create the deviceConfigurationAssignment.</span></span>

|<span data-ttu-id="e7576-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e7576-130">Property</span></span>|<span data-ttu-id="e7576-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7576-131">Type</span></span>|<span data-ttu-id="e7576-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7576-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e7576-133">id</span><span class="sxs-lookup"><span data-stu-id="e7576-133">id</span></span>|<span data-ttu-id="e7576-134">String</span><span class="sxs-lookup"><span data-stu-id="e7576-134">String</span></span>|<span data-ttu-id="e7576-135">La clave de la asignación.</span><span class="sxs-lookup"><span data-stu-id="e7576-135">The key of the assignment.</span></span>|
|<span data-ttu-id="e7576-136">target</span><span class="sxs-lookup"><span data-stu-id="e7576-136">target</span></span>|[<span data-ttu-id="e7576-137">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="e7576-137">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="e7576-138">El destino de la tarea para la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7576-138">The assignment target for the device configuration.</span></span>|



## <a name="response"></a><span data-ttu-id="e7576-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e7576-139">Response</span></span>
<span data-ttu-id="e7576-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e7576-140">If successful, this method returns a `201 Created` response code and a [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e7576-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e7576-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="e7576-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e7576-142">Request</span></span>
<span data-ttu-id="e7576-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e7576-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/assignments
Content-type: application/json
Content-length: 169

{
  "@odata.type": "#microsoft.graph.deviceConfigurationAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="e7576-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e7576-144">Response</span></span>
<span data-ttu-id="e7576-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e7576-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 218

{
  "@odata.type": "#microsoft.graph.deviceConfigurationAssignment",
  "id": "d59b6342-6342-d59b-4263-9bd542639bd5",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```





