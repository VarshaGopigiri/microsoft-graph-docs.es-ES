---
title: Actualizar organización
description: Actualice las propiedades de un objeto organization.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 023bc7bdedfce2fc18784cd027bc0f041d7b8527
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27928979"
---
# <a name="update-organization"></a><span data-ttu-id="d306b-103">Actualizar organización</span><span class="sxs-lookup"><span data-stu-id="d306b-103">Update organization</span></span>

> <span data-ttu-id="d306b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d306b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d306b-105">Actualice las propiedades de un objeto [organization](../resources/intune-onboarding-organization.md).</span><span class="sxs-lookup"><span data-stu-id="d306b-105">Update the properties of a [organization](../resources/intune-onboarding-organization.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d306b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d306b-106">Prerequisites</span></span>
<span data-ttu-id="d306b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d306b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d306b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d306b-109">Permission type</span></span>|<span data-ttu-id="d306b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d306b-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d306b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d306b-111">Delegated (work or school account)</span></span>|<span data-ttu-id="d306b-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d306b-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="d306b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d306b-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d306b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d306b-114">Not supported.</span></span>|
|<span data-ttu-id="d306b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d306b-115">Application</span></span>|<span data-ttu-id="d306b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d306b-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d306b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d306b-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /organization/{organizationId}
```

## <a name="request-headers"></a><span data-ttu-id="d306b-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d306b-118">Request headers</span></span>
|<span data-ttu-id="d306b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d306b-119">Header</span></span>|<span data-ttu-id="d306b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d306b-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d306b-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="d306b-121">Authorization</span></span>|<span data-ttu-id="d306b-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d306b-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d306b-123">Accept</span><span class="sxs-lookup"><span data-stu-id="d306b-123">Accept</span></span>|<span data-ttu-id="d306b-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d306b-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d306b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d306b-125">Request body</span></span>
<span data-ttu-id="d306b-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [organization](../resources/intune-onboarding-organization.md).</span><span class="sxs-lookup"><span data-stu-id="d306b-126">In the request body, supply a JSON representation for the [organization](../resources/intune-onboarding-organization.md) object.</span></span>

<span data-ttu-id="d306b-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [organization](../resources/intune-onboarding-organization.md).</span><span class="sxs-lookup"><span data-stu-id="d306b-127">The following table shows the properties that are required when you create the [organization](../resources/intune-onboarding-organization.md).</span></span>

|<span data-ttu-id="d306b-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d306b-128">Property</span></span>|<span data-ttu-id="d306b-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="d306b-129">Type</span></span>|<span data-ttu-id="d306b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d306b-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d306b-131">id</span><span class="sxs-lookup"><span data-stu-id="d306b-131">id</span></span>|<span data-ttu-id="d306b-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="d306b-132">String</span></span>|<span data-ttu-id="d306b-133">El GUID para el objeto.</span><span class="sxs-lookup"><span data-stu-id="d306b-133">The GUID for the object.</span></span>|
|<span data-ttu-id="d306b-134">mobileDeviceManagementAuthority</span><span class="sxs-lookup"><span data-stu-id="d306b-134">mobileDeviceManagementAuthority</span></span>|[<span data-ttu-id="d306b-135">mdmAuthority</span><span class="sxs-lookup"><span data-stu-id="d306b-135">mdmAuthority</span></span>](../resources/intune-onboarding-mdmauthority.md)|<span data-ttu-id="d306b-136">Entidad de administración de dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="d306b-136">Mobile device management authority.</span></span> <span data-ttu-id="d306b-137">Los valores posibles son: `unknown`, `intune`, `sccm` y `office365`.</span><span class="sxs-lookup"><span data-stu-id="d306b-137">Possible values are: `unknown`, `intune`, `sccm`, `office365`.</span></span>|



## <a name="response"></a><span data-ttu-id="d306b-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d306b-138">Response</span></span>
<span data-ttu-id="d306b-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [organization](../resources/intune-onboarding-organization.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d306b-139">If successful, this method returns a `200 OK` response code and an updated [organization](../resources/intune-onboarding-organization.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d306b-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d306b-140">Example</span></span>
### <a name="request"></a><span data-ttu-id="d306b-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d306b-141">Request</span></span>
<span data-ttu-id="d306b-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d306b-142">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/organization/{organizationId}
Content-type: application/json
Content-length: 102

{
  "@odata.type": "#microsoft.graph.organization",
  "mobileDeviceManagementAuthority": "intune"
}
```

### <a name="response"></a><span data-ttu-id="d306b-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d306b-143">Response</span></span>
<span data-ttu-id="d306b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d306b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 151

{
  "@odata.type": "#microsoft.graph.organization",
  "id": "9efe224a-224a-9efe-4a22-fe9e4a22fe9e",
  "mobileDeviceManagementAuthority": "intune"
}
```



