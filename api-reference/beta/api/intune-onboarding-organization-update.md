---
title: Actualizar organización
description: Actualice las propiedades de un objeto organization.
ms.openlocfilehash: 32e9cf3cccecf0a763d20b201040d79d4442cdfe
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091135"
---
# <a name="update-organization"></a><span data-ttu-id="78a18-103">Actualizar organización</span><span class="sxs-lookup"><span data-stu-id="78a18-103">Update organization</span></span>

> <span data-ttu-id="78a18-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="78a18-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="78a18-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="78a18-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="78a18-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="78a18-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="78a18-107">Actualice las propiedades de un objeto [organization](../resources/intune-onboarding-organization.md).</span><span class="sxs-lookup"><span data-stu-id="78a18-107">Update the properties of a [organization](../resources/intune-onboarding-organization.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="78a18-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="78a18-108">Prerequisites</span></span>
<span data-ttu-id="78a18-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="78a18-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="78a18-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="78a18-111">Permission type</span></span>|<span data-ttu-id="78a18-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="78a18-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="78a18-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="78a18-113">Delegated (work or school account)</span></span>|<span data-ttu-id="78a18-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="78a18-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="78a18-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="78a18-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="78a18-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="78a18-116">Not supported.</span></span>|
|<span data-ttu-id="78a18-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="78a18-117">Application</span></span>|<span data-ttu-id="78a18-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="78a18-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="78a18-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="78a18-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /organization/{organizationId}
```

## <a name="request-headers"></a><span data-ttu-id="78a18-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="78a18-120">Request headers</span></span>
|<span data-ttu-id="78a18-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="78a18-121">Header</span></span>|<span data-ttu-id="78a18-122">Valor</span><span class="sxs-lookup"><span data-stu-id="78a18-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="78a18-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="78a18-123">Authorization</span></span>|<span data-ttu-id="78a18-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="78a18-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="78a18-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="78a18-125">Accept</span></span>|<span data-ttu-id="78a18-126">application/json</span><span class="sxs-lookup"><span data-stu-id="78a18-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="78a18-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="78a18-127">Request body</span></span>
<span data-ttu-id="78a18-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [organization](../resources/intune-onboarding-organization.md).</span><span class="sxs-lookup"><span data-stu-id="78a18-128">In the request body, supply a JSON representation for the [organization](../resources/intune-onboarding-organization.md) object.</span></span>

<span data-ttu-id="78a18-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [organization](../resources/intune-onboarding-organization.md).</span><span class="sxs-lookup"><span data-stu-id="78a18-129">The following table shows the properties that are required when you create the [organization](../resources/intune-onboarding-organization.md).</span></span>

|<span data-ttu-id="78a18-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="78a18-130">Property</span></span>|<span data-ttu-id="78a18-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="78a18-131">Type</span></span>|<span data-ttu-id="78a18-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="78a18-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="78a18-133">id</span><span class="sxs-lookup"><span data-stu-id="78a18-133">id</span></span>|<span data-ttu-id="78a18-134">String</span><span class="sxs-lookup"><span data-stu-id="78a18-134">String</span></span>|<span data-ttu-id="78a18-135">El GUID para el objeto.</span><span class="sxs-lookup"><span data-stu-id="78a18-135">The GUID for the object.</span></span>|
|<span data-ttu-id="78a18-136">mobileDeviceManagementAuthority</span><span class="sxs-lookup"><span data-stu-id="78a18-136">mobileDeviceManagementAuthority</span></span>|[<span data-ttu-id="78a18-137">mdmAuthority</span><span class="sxs-lookup"><span data-stu-id="78a18-137">mdmAuthority</span></span>](../resources/intune-onboarding-mdmauthority.md)|<span data-ttu-id="78a18-138">Entidad de administración de dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="78a18-138">Mobile device management authority.</span></span> <span data-ttu-id="78a18-139">Los valores posibles son: `unknown`, `intune`, `sccm` y `office365`.</span><span class="sxs-lookup"><span data-stu-id="78a18-139">Possible values are: `unknown`, `intune`, `sccm`, `office365`.</span></span>|
|<span data-ttu-id="78a18-140">certificateConnectorSetting</span><span class="sxs-lookup"><span data-stu-id="78a18-140">certificateConnectorSetting</span></span>|[<span data-ttu-id="78a18-141">certificateConnectorSetting</span><span class="sxs-lookup"><span data-stu-id="78a18-141">certificateConnectorSetting</span></span>](../resources/intune-onboarding-certificateconnectorsetting.md)|<span data-ttu-id="78a18-142">Configuración del conector del certificado.</span><span class="sxs-lookup"><span data-stu-id="78a18-142">Certificate connector setting.</span></span>|



## <a name="response"></a><span data-ttu-id="78a18-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="78a18-143">Response</span></span>
<span data-ttu-id="78a18-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [organization](../resources/intune-onboarding-organization.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="78a18-144">If successful, this method returns a `200 OK` response code and an updated [organization](../resources/intune-onboarding-organization.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="78a18-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="78a18-145">Example</span></span>
### <a name="request"></a><span data-ttu-id="78a18-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="78a18-146">Request</span></span>
<span data-ttu-id="78a18-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="78a18-147">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/organization/{organizationId}
Content-type: application/json
Content-length: 441

{
  "mobileDeviceManagementAuthority": "intune",
  "certificateConnectorSetting": {
    "@odata.type": "microsoft.graph.certificateConnectorSetting",
    "status": 6,
    "certExpiryTime": "2017-01-01T00:00:03.9979674-08:00",
    "enrollmentError": "Enrollment Error value",
    "lastConnectorConnectionTime": "2017-01-01T00:02:50.2393584-08:00",
    "connectorVersion": "Connector Version value",
    "lastUploadVersion": 1
  }
}
```

### <a name="response"></a><span data-ttu-id="78a18-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="78a18-148">Response</span></span>
<span data-ttu-id="78a18-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="78a18-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 541

{
  "@odata.type": "#microsoft.graph.organization",
  "id": "9efe224a-224a-9efe-4a22-fe9e4a22fe9e",
  "mobileDeviceManagementAuthority": "intune",
  "certificateConnectorSetting": {
    "@odata.type": "microsoft.graph.certificateConnectorSetting",
    "status": 6,
    "certExpiryTime": "2017-01-01T00:00:03.9979674-08:00",
    "enrollmentError": "Enrollment Error value",
    "lastConnectorConnectionTime": "2017-01-01T00:02:50.2393584-08:00",
    "connectorVersion": "Connector Version value",
    "lastUploadVersion": 1
  }
}
```





