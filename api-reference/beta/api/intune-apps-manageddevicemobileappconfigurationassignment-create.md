---
title: Crear managedDeviceMobileAppConfigurationAssignment
description: Cree un objeto managedDeviceMobileAppConfigurationAssignment.
author: tfitzmac
ms.openlocfilehash: 8418b853c4d82f0a56d592a90542505f0355df0b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27342780"
---
# <a name="create-manageddevicemobileappconfigurationassignment"></a><span data-ttu-id="27979-103">Crear managedDeviceMobileAppConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="27979-103">Create managedDeviceMobileAppConfigurationAssignment</span></span>

> <span data-ttu-id="27979-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="27979-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="27979-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="27979-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="27979-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="27979-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="27979-107">Cree un objeto [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="27979-107">Create a new [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="27979-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="27979-108">Prerequisites</span></span>
<span data-ttu-id="27979-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="27979-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="27979-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="27979-111">Permission type</span></span>|<span data-ttu-id="27979-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="27979-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="27979-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="27979-113">Delegated (work or school account)</span></span>|<span data-ttu-id="27979-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="27979-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="27979-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="27979-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="27979-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="27979-116">Not supported.</span></span>|
|<span data-ttu-id="27979-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="27979-117">Application</span></span>|<span data-ttu-id="27979-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="27979-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="27979-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="27979-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="27979-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="27979-120">Request headers</span></span>
|<span data-ttu-id="27979-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27979-121">Header</span></span>|<span data-ttu-id="27979-122">Valor</span><span class="sxs-lookup"><span data-stu-id="27979-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="27979-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="27979-123">Authorization</span></span>|<span data-ttu-id="27979-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="27979-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="27979-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="27979-125">Accept</span></span>|<span data-ttu-id="27979-126">application/json</span><span class="sxs-lookup"><span data-stu-id="27979-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="27979-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="27979-127">Request body</span></span>
<span data-ttu-id="27979-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedDeviceMobileAppConfigurationAssignment.</span><span class="sxs-lookup"><span data-stu-id="27979-128">In the request body, supply a JSON representation for the managedDeviceMobileAppConfigurationAssignment object.</span></span>

<span data-ttu-id="27979-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedDeviceMobileAppConfigurationAssignment.</span><span class="sxs-lookup"><span data-stu-id="27979-129">The following table shows the properties that are required when you create the managedDeviceMobileAppConfigurationAssignment.</span></span>

|<span data-ttu-id="27979-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="27979-130">Property</span></span>|<span data-ttu-id="27979-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="27979-131">Type</span></span>|<span data-ttu-id="27979-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="27979-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="27979-133">id</span><span class="sxs-lookup"><span data-stu-id="27979-133">id</span></span>|<span data-ttu-id="27979-134">String</span><span class="sxs-lookup"><span data-stu-id="27979-134">String</span></span>|<span data-ttu-id="27979-135">Identificador único de la entidad.</span><span class="sxs-lookup"><span data-stu-id="27979-135">Unique identifier of the entity.</span></span>|
|<span data-ttu-id="27979-136">target</span><span class="sxs-lookup"><span data-stu-id="27979-136">target</span></span>|[<span data-ttu-id="27979-137">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="27979-137">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="27979-138">Destino de asignación al que está asignada la directiva de términos y condiciones.</span><span class="sxs-lookup"><span data-stu-id="27979-138">Assignment target that the T&C policy is assigned to.</span></span>|



## <a name="response"></a><span data-ttu-id="27979-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="27979-139">Response</span></span>
<span data-ttu-id="27979-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="27979-140">If successful, this method returns a `201 Created` response code and a [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="27979-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="27979-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="27979-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="27979-142">Request</span></span>
<span data-ttu-id="27979-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="27979-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/assignments
Content-type: application/json
Content-length: 185

{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="27979-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="27979-144">Response</span></span>
<span data-ttu-id="27979-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="27979-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 234

{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationAssignment",
  "id": "4df81c9c-1c9c-4df8-9c1c-f84d9c1cf84d",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```





