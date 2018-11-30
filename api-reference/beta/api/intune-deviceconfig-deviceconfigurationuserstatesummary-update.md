---
title: Actualizar deviceConfigurationUserStateSummary
description: Actualizar las propiedades de un objeto deviceConfigurationUserStateSummary.
ms.openlocfilehash: fd22d51f9d52f97c080cace5c6cf434ccaff2416
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088239"
---
# <a name="update-deviceconfigurationuserstatesummary"></a><span data-ttu-id="99e18-103">Actualizar deviceConfigurationUserStateSummary</span><span class="sxs-lookup"><span data-stu-id="99e18-103">Update deviceConfigurationUserStateSummary</span></span>

> <span data-ttu-id="99e18-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="99e18-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="99e18-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="99e18-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="99e18-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="99e18-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="99e18-107">Actualizar las propiedades de un objeto [deviceConfigurationUserStateSummary](../resources/intune-deviceconfig-deviceconfigurationuserstatesummary.md) .</span><span class="sxs-lookup"><span data-stu-id="99e18-107">Update the properties of a [deviceConfigurationUserStateSummary](../resources/intune-deviceconfig-deviceconfigurationuserstatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="99e18-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="99e18-108">Prerequisites</span></span>
<span data-ttu-id="99e18-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="99e18-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="99e18-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="99e18-111">Permission type</span></span>|<span data-ttu-id="99e18-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="99e18-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="99e18-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="99e18-113">Delegated (work or school account)</span></span>|<span data-ttu-id="99e18-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="99e18-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="99e18-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="99e18-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="99e18-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="99e18-116">Not supported.</span></span>|
|<span data-ttu-id="99e18-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="99e18-117">Application</span></span>|<span data-ttu-id="99e18-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="99e18-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="99e18-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="99e18-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurationUserStateSummaries
```

## <a name="request-headers"></a><span data-ttu-id="99e18-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="99e18-120">Request headers</span></span>
|<span data-ttu-id="99e18-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99e18-121">Header</span></span>|<span data-ttu-id="99e18-122">Valor</span><span class="sxs-lookup"><span data-stu-id="99e18-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="99e18-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="99e18-123">Authorization</span></span>|<span data-ttu-id="99e18-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="99e18-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="99e18-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="99e18-125">Accept</span></span>|<span data-ttu-id="99e18-126">application/json</span><span class="sxs-lookup"><span data-stu-id="99e18-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="99e18-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="99e18-127">Request body</span></span>
<span data-ttu-id="99e18-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [deviceConfigurationUserStateSummary](../resources/intune-deviceconfig-deviceconfigurationuserstatesummary.md) .</span><span class="sxs-lookup"><span data-stu-id="99e18-128">In the request body, supply a JSON representation for the [deviceConfigurationUserStateSummary](../resources/intune-deviceconfig-deviceconfigurationuserstatesummary.md) object.</span></span>

<span data-ttu-id="99e18-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [deviceConfigurationUserStateSummary](../resources/intune-deviceconfig-deviceconfigurationuserstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="99e18-129">The following table shows the properties that are required when you create the [deviceConfigurationUserStateSummary](../resources/intune-deviceconfig-deviceconfigurationuserstatesummary.md).</span></span>

|<span data-ttu-id="99e18-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="99e18-130">Property</span></span>|<span data-ttu-id="99e18-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="99e18-131">Type</span></span>|<span data-ttu-id="99e18-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="99e18-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="99e18-133">id</span><span class="sxs-lookup"><span data-stu-id="99e18-133">id</span></span>|<span data-ttu-id="99e18-134">String</span><span class="sxs-lookup"><span data-stu-id="99e18-134">String</span></span>|<span data-ttu-id="99e18-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="99e18-135">Key of the entity.</span></span>|
|<span data-ttu-id="99e18-136">unknownUserCount</span><span class="sxs-lookup"><span data-stu-id="99e18-136">unknownUserCount</span></span>|<span data-ttu-id="99e18-137">Int32</span><span class="sxs-lookup"><span data-stu-id="99e18-137">Int32</span></span>|<span data-ttu-id="99e18-138">Número de usuarios desconocidos</span><span class="sxs-lookup"><span data-stu-id="99e18-138">Number of unknown users</span></span>|
|<span data-ttu-id="99e18-139">notApplicableUserCount</span><span class="sxs-lookup"><span data-stu-id="99e18-139">notApplicableUserCount</span></span>|<span data-ttu-id="99e18-140">Int32</span><span class="sxs-lookup"><span data-stu-id="99e18-140">Int32</span></span>|<span data-ttu-id="99e18-141">Número de usuarios no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="99e18-141">Number of not applicable users</span></span>|
|<span data-ttu-id="99e18-142">compliantUserCount</span><span class="sxs-lookup"><span data-stu-id="99e18-142">compliantUserCount</span></span>|<span data-ttu-id="99e18-143">Int32</span><span class="sxs-lookup"><span data-stu-id="99e18-143">Int32</span></span>|<span data-ttu-id="99e18-144">Número de usuarios compatible con</span><span class="sxs-lookup"><span data-stu-id="99e18-144">Number of compliant users</span></span>|
|<span data-ttu-id="99e18-145">remediatedUserCount</span><span class="sxs-lookup"><span data-stu-id="99e18-145">remediatedUserCount</span></span>|<span data-ttu-id="99e18-146">Int32</span><span class="sxs-lookup"><span data-stu-id="99e18-146">Int32</span></span>|<span data-ttu-id="99e18-147">Número de usuarios corregidos con pruebas</span><span class="sxs-lookup"><span data-stu-id="99e18-147">Number of remediated users</span></span>|
|<span data-ttu-id="99e18-148">nonCompliantUserCount</span><span class="sxs-lookup"><span data-stu-id="99e18-148">nonCompliantUserCount</span></span>|<span data-ttu-id="99e18-149">Int32</span><span class="sxs-lookup"><span data-stu-id="99e18-149">Int32</span></span>|<span data-ttu-id="99e18-150">Número de usuarios no compatibles</span><span class="sxs-lookup"><span data-stu-id="99e18-150">Number of NonCompliant users</span></span>|
|<span data-ttu-id="99e18-151">errorUserCount</span><span class="sxs-lookup"><span data-stu-id="99e18-151">errorUserCount</span></span>|<span data-ttu-id="99e18-152">Int32</span><span class="sxs-lookup"><span data-stu-id="99e18-152">Int32</span></span>|<span data-ttu-id="99e18-153">Número de usuarios de error</span><span class="sxs-lookup"><span data-stu-id="99e18-153">Number of error users</span></span>|
|<span data-ttu-id="99e18-154">conflictUserCount</span><span class="sxs-lookup"><span data-stu-id="99e18-154">conflictUserCount</span></span>|<span data-ttu-id="99e18-155">Int32</span><span class="sxs-lookup"><span data-stu-id="99e18-155">Int32</span></span>|<span data-ttu-id="99e18-156">Número de usuarios de conflicto</span><span class="sxs-lookup"><span data-stu-id="99e18-156">Number of conflict users</span></span>|



## <a name="response"></a><span data-ttu-id="99e18-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="99e18-157">Response</span></span>
<span data-ttu-id="99e18-158">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [deviceConfigurationUserStateSummary](../resources/intune-deviceconfig-deviceconfigurationuserstatesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="99e18-158">If successful, this method returns a `200 OK` response code and an updated [deviceConfigurationUserStateSummary](../resources/intune-deviceconfig-deviceconfigurationuserstatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="99e18-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="99e18-159">Example</span></span>
### <a name="request"></a><span data-ttu-id="99e18-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="99e18-160">Request</span></span>
<span data-ttu-id="99e18-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="99e18-161">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurationUserStateSummaries
Content-type: application/json
Content-length: 201

{
  "unknownUserCount": 0,
  "notApplicableUserCount": 6,
  "compliantUserCount": 2,
  "remediatedUserCount": 3,
  "nonCompliantUserCount": 5,
  "errorUserCount": 14,
  "conflictUserCount": 1
}
```

### <a name="response"></a><span data-ttu-id="99e18-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="99e18-162">Response</span></span>
<span data-ttu-id="99e18-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="99e18-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 324

{
  "@odata.type": "#microsoft.graph.deviceConfigurationUserStateSummary",
  "id": "e8957887-7887-e895-8778-95e8877895e8",
  "unknownUserCount": 0,
  "notApplicableUserCount": 6,
  "compliantUserCount": 2,
  "remediatedUserCount": 3,
  "nonCompliantUserCount": 5,
  "errorUserCount": 14,
  "conflictUserCount": 1
}
```




