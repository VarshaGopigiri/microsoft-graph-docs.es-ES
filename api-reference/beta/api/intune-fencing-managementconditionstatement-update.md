---
title: Actualizar managementConditionStatement
description: Actualizar las propiedades de un objeto managementConditionStatement.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 800d40bda342ea23b55e7dc9bf62a99f1e41e3df
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27935419"
---
# <a name="update-managementconditionstatement"></a><span data-ttu-id="1485b-103">Actualizar managementConditionStatement</span><span class="sxs-lookup"><span data-stu-id="1485b-103">Update managementConditionStatement</span></span>

> <span data-ttu-id="1485b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1485b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1485b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1485b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1485b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1485b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1485b-107">Actualizar las propiedades de un objeto [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) .</span><span class="sxs-lookup"><span data-stu-id="1485b-107">Update the properties of a [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1485b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1485b-108">Prerequisites</span></span>
<span data-ttu-id="1485b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1485b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1485b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1485b-111">Permission type</span></span>|<span data-ttu-id="1485b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1485b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1485b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1485b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1485b-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1485b-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="1485b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1485b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1485b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1485b-116">Not supported.</span></span>|
|<span data-ttu-id="1485b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1485b-117">Application</span></span>|<span data-ttu-id="1485b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1485b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1485b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1485b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/managementConditionStatements/{managementConditionStatementId}
PATCH /deviceManagement/managementConditions/{managementConditionId}/managementConditionStatements/{managementConditionStatementId}
```

## <a name="request-headers"></a><span data-ttu-id="1485b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1485b-120">Request headers</span></span>
|<span data-ttu-id="1485b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1485b-121">Header</span></span>|<span data-ttu-id="1485b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1485b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1485b-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="1485b-123">Authorization</span></span>|<span data-ttu-id="1485b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1485b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1485b-125">Accept</span><span class="sxs-lookup"><span data-stu-id="1485b-125">Accept</span></span>|<span data-ttu-id="1485b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1485b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1485b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1485b-127">Request body</span></span>
<span data-ttu-id="1485b-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) .</span><span class="sxs-lookup"><span data-stu-id="1485b-128">In the request body, supply a JSON representation for the [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) object.</span></span>

<span data-ttu-id="1485b-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md).</span><span class="sxs-lookup"><span data-stu-id="1485b-129">The following table shows the properties that are required when you create the [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md).</span></span>

|<span data-ttu-id="1485b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1485b-130">Property</span></span>|<span data-ttu-id="1485b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="1485b-131">Type</span></span>|<span data-ttu-id="1485b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="1485b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1485b-133">id</span><span class="sxs-lookup"><span data-stu-id="1485b-133">id</span></span>|<span data-ttu-id="1485b-134">String</span><span class="sxs-lookup"><span data-stu-id="1485b-134">String</span></span>|<span data-ttu-id="1485b-135">Identificador único de la instrucción de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1485b-135">Unique identifier for the management condition statement.</span></span> <span data-ttu-id="1485b-136">Valor asignado al crear generada por el sistema.</span><span class="sxs-lookup"><span data-stu-id="1485b-136">System generated value assigned when created.</span></span>|
|<span data-ttu-id="1485b-137">displayName</span><span class="sxs-lookup"><span data-stu-id="1485b-137">displayName</span></span>|<span data-ttu-id="1485b-138">String</span><span class="sxs-lookup"><span data-stu-id="1485b-138">String</span></span>|<span data-ttu-id="1485b-139">El nombre definido de administración de la instrucción de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1485b-139">The admin defined name of the management condition statement.</span></span>|
|<span data-ttu-id="1485b-140">descripción</span><span class="sxs-lookup"><span data-stu-id="1485b-140">description</span></span>|<span data-ttu-id="1485b-141">String</span><span class="sxs-lookup"><span data-stu-id="1485b-141">String</span></span>|<span data-ttu-id="1485b-142">El administrador define la descripción de la instrucción de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1485b-142">The admin defined description of the management condition statement.</span></span>|
|<span data-ttu-id="1485b-143">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="1485b-143">createdDateTime</span></span>|<span data-ttu-id="1485b-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1485b-144">DateTimeOffset</span></span>|<span data-ttu-id="1485b-145">La hora en que se creó la instrucción de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1485b-145">The time the management condition statement was created.</span></span> <span data-ttu-id="1485b-146">Servicio generado al lado.</span><span class="sxs-lookup"><span data-stu-id="1485b-146">Generated service side.</span></span>|
|<span data-ttu-id="1485b-147">modifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="1485b-147">modifiedDateTime</span></span>|<span data-ttu-id="1485b-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1485b-148">DateTimeOffset</span></span>|<span data-ttu-id="1485b-149">La hora en que se modificó por última vez la instrucción de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1485b-149">The time the management condition statement was last modified.</span></span> <span data-ttu-id="1485b-150">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="1485b-150">Updated service side.</span></span>|
|<span data-ttu-id="1485b-151">expresión</span><span class="sxs-lookup"><span data-stu-id="1485b-151">expression</span></span>|[<span data-ttu-id="1485b-152">managementConditionExpression</span><span class="sxs-lookup"><span data-stu-id="1485b-152">managementConditionExpression</span></span>](../resources/intune-fencing-managementconditionexpression.md)|<span data-ttu-id="1485b-153">La expresión de instrucción de condición de administración que se usa para evaluar si una administración condición instrucción estaba activada o desactivada.</span><span class="sxs-lookup"><span data-stu-id="1485b-153">The management condition statement expression used to evaluate if a management condition statement was activated/deactivated.</span></span>|
|<span data-ttu-id="1485b-154">eTag</span><span class="sxs-lookup"><span data-stu-id="1485b-154">eTag</span></span>|<span data-ttu-id="1485b-155">String</span><span class="sxs-lookup"><span data-stu-id="1485b-155">String</span></span>|<span data-ttu-id="1485b-156">ETag de la instrucción de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1485b-156">ETag of the management condition statement.</span></span> <span data-ttu-id="1485b-157">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="1485b-157">Updated service side.</span></span>|
|<span data-ttu-id="1485b-158">applicablePlatforms</span><span class="sxs-lookup"><span data-stu-id="1485b-158">applicablePlatforms</span></span>|<span data-ttu-id="1485b-159">colección de [devicePlatformType](../resources/intune-shared-deviceplatformtype.md)</span><span class="sxs-lookup"><span data-stu-id="1485b-159">[devicePlatformType](../resources/intune-shared-deviceplatformtype.md) collection</span></span>|<span data-ttu-id="1485b-160">Las plataformas aplicables para esta instrucción de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1485b-160">The applicable platforms for this management condition statement.</span></span>
<span data-ttu-id="1485b-161">Esto se calcula a partir de ¿está buscando las condiciones de administración asociadas a la administración de la condición de la instrucción y buscar la intersección de plataformas aplicables.</span><span class="sxs-lookup"><span data-stu-id="1485b-161">This is calculated from looking the management conditions associated to the management condition statement and finding the intersection of applicable platforms.</span></span> <span data-ttu-id="1485b-162">Los valores posibles son: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater` y `androidWorkProfile`.</span><span class="sxs-lookup"><span data-stu-id="1485b-162">Possible values are: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile`.</span></span>|



## <a name="response"></a><span data-ttu-id="1485b-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1485b-163">Response</span></span>
<span data-ttu-id="1485b-164">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1485b-164">If successful, this method returns a `200 OK` response code and an updated [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1485b-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1485b-165">Example</span></span>
### <a name="request"></a><span data-ttu-id="1485b-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1485b-166">Request</span></span>
<span data-ttu-id="1485b-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1485b-167">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/managementConditionStatements/{managementConditionStatementId}
Content-type: application/json
Content-length: 256

{
  "displayName": "Display Name value",
  "description": "Description value",
  "expression": {
    "@odata.type": "microsoft.graph.managementConditionExpression"
  },
  "eTag": "ETag value",
  "applicablePlatforms": [
    "androidForWork"
  ]
}
```

### <a name="response"></a><span data-ttu-id="1485b-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1485b-168">Response</span></span>
<span data-ttu-id="1485b-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1485b-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 491

{
  "@odata.type": "#microsoft.graph.managementConditionStatement",
  "id": "bedb0c00-0c00-bedb-000c-dbbe000cdbbe",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "modifiedDateTime": "2017-01-01T00:00:22.8983556-08:00",
  "expression": {
    "@odata.type": "microsoft.graph.managementConditionExpression"
  },
  "eTag": "ETag value",
  "applicablePlatforms": [
    "androidForWork"
  ]
}
```





