---
title: Actualizar iosLobAppProvisioningConfigurationAssignment
description: Actualizar las propiedades de un objeto iosLobAppProvisioningConfigurationAssignment.
author: tfitzmac
ms.openlocfilehash: 0212d357ceee946e8515a5143ffd7bf7307a7773
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27338881"
---
# <a name="update-ioslobappprovisioningconfigurationassignment"></a><span data-ttu-id="54b03-103">Actualizar iosLobAppProvisioningConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="54b03-103">Update iosLobAppProvisioningConfigurationAssignment</span></span>

> <span data-ttu-id="54b03-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="54b03-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="54b03-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="54b03-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="54b03-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="54b03-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="54b03-107">Actualizar las propiedades de un objeto [iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="54b03-107">Update the properties of a [iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="54b03-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="54b03-108">Prerequisites</span></span>
<span data-ttu-id="54b03-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="54b03-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="54b03-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="54b03-111">Permission type</span></span>|<span data-ttu-id="54b03-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="54b03-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="54b03-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="54b03-113">Delegated (work or school account)</span></span>|<span data-ttu-id="54b03-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="54b03-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="54b03-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="54b03-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="54b03-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="54b03-116">Not supported.</span></span>|
|<span data-ttu-id="54b03-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="54b03-117">Application</span></span>|<span data-ttu-id="54b03-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="54b03-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="54b03-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="54b03-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/iosLobAppProvisioningConfigurations/{iosLobAppProvisioningConfigurationId}/assignments/{iosLobAppProvisioningConfigurationAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="54b03-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="54b03-120">Request headers</span></span>
|<span data-ttu-id="54b03-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54b03-121">Header</span></span>|<span data-ttu-id="54b03-122">Valor</span><span class="sxs-lookup"><span data-stu-id="54b03-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="54b03-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="54b03-123">Authorization</span></span>|<span data-ttu-id="54b03-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="54b03-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="54b03-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="54b03-125">Accept</span></span>|<span data-ttu-id="54b03-126">application/json</span><span class="sxs-lookup"><span data-stu-id="54b03-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="54b03-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="54b03-127">Request body</span></span>
<span data-ttu-id="54b03-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="54b03-128">In the request body, supply a JSON representation for the [iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md) object.</span></span>

<span data-ttu-id="54b03-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="54b03-129">The following table shows the properties that are required when you create the [iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md).</span></span>

|<span data-ttu-id="54b03-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="54b03-130">Property</span></span>|<span data-ttu-id="54b03-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="54b03-131">Type</span></span>|<span data-ttu-id="54b03-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="54b03-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="54b03-133">id</span><span class="sxs-lookup"><span data-stu-id="54b03-133">id</span></span>|<span data-ttu-id="54b03-134">String</span><span class="sxs-lookup"><span data-stu-id="54b03-134">String</span></span>|<span data-ttu-id="54b03-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="54b03-135">Key of the entity.</span></span>|
|<span data-ttu-id="54b03-136">target</span><span class="sxs-lookup"><span data-stu-id="54b03-136">target</span></span>|[<span data-ttu-id="54b03-137">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="54b03-137">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="54b03-138">La asignación de grupo de destino definida por el administrador.</span><span class="sxs-lookup"><span data-stu-id="54b03-138">The target group assignment defined by the admin.</span></span>|



## <a name="response"></a><span data-ttu-id="54b03-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54b03-139">Response</span></span>
<span data-ttu-id="54b03-140">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="54b03-140">If successful, this method returns a `200 OK` response code and an updated [iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="54b03-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="54b03-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="54b03-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="54b03-142">Request</span></span>
<span data-ttu-id="54b03-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="54b03-143">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/iosLobAppProvisioningConfigurations/{iosLobAppProvisioningConfigurationId}/assignments/{iosLobAppProvisioningConfigurationAssignmentId}
Content-type: application/json
Content-length: 101

{
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="54b03-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54b03-144">Response</span></span>
<span data-ttu-id="54b03-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="54b03-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 233

{
  "@odata.type": "#microsoft.graph.iosLobAppProvisioningConfigurationAssignment",
  "id": "eac7008e-008e-eac7-8e00-c7ea8e00c7ea",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```





