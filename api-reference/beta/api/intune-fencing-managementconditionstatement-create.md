---
title: Crear managementConditionStatement
description: Crear un nuevo objeto managementConditionStatement.
ms.openlocfilehash: a01d0233eff9d22b3174a8aa7bd382b9a1266ac2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084207"
---
# <a name="create-managementconditionstatement"></a><span data-ttu-id="30b59-103">Crear managementConditionStatement</span><span class="sxs-lookup"><span data-stu-id="30b59-103">Create managementConditionStatement</span></span>

> <span data-ttu-id="30b59-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="30b59-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="30b59-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="30b59-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="30b59-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="30b59-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="30b59-107">Crear un nuevo objeto [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) .</span><span class="sxs-lookup"><span data-stu-id="30b59-107">Create a new [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="30b59-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="30b59-108">Prerequisites</span></span>
<span data-ttu-id="30b59-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="30b59-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="30b59-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="30b59-111">Permission type</span></span>|<span data-ttu-id="30b59-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="30b59-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="30b59-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="30b59-113">Delegated (work or school account)</span></span>|<span data-ttu-id="30b59-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="30b59-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="30b59-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="30b59-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="30b59-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="30b59-116">Not supported.</span></span>|
|<span data-ttu-id="30b59-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="30b59-117">Application</span></span>|<span data-ttu-id="30b59-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="30b59-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="30b59-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="30b59-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/managementConditionStatements
POST /deviceManagement/managementConditions/{managementConditionId}/managementConditionStatements
```

## <a name="request-headers"></a><span data-ttu-id="30b59-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="30b59-120">Request headers</span></span>
|<span data-ttu-id="30b59-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30b59-121">Header</span></span>|<span data-ttu-id="30b59-122">Valor</span><span class="sxs-lookup"><span data-stu-id="30b59-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="30b59-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="30b59-123">Authorization</span></span>|<span data-ttu-id="30b59-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="30b59-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="30b59-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="30b59-125">Accept</span></span>|<span data-ttu-id="30b59-126">application/json</span><span class="sxs-lookup"><span data-stu-id="30b59-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="30b59-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="30b59-127">Request body</span></span>
<span data-ttu-id="30b59-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto managementConditionStatement.</span><span class="sxs-lookup"><span data-stu-id="30b59-128">In the request body, supply a JSON representation for the managementConditionStatement object.</span></span>

<span data-ttu-id="30b59-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el managementConditionStatement.</span><span class="sxs-lookup"><span data-stu-id="30b59-129">The following table shows the properties that are required when you create the managementConditionStatement.</span></span>

|<span data-ttu-id="30b59-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="30b59-130">Property</span></span>|<span data-ttu-id="30b59-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="30b59-131">Type</span></span>|<span data-ttu-id="30b59-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="30b59-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="30b59-133">id</span><span class="sxs-lookup"><span data-stu-id="30b59-133">id</span></span>|<span data-ttu-id="30b59-134">String</span><span class="sxs-lookup"><span data-stu-id="30b59-134">String</span></span>|<span data-ttu-id="30b59-135">Identificador único de la instrucción de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="30b59-135">Unique identifier for the management condition statement.</span></span> <span data-ttu-id="30b59-136">Valor asignado al crear generada por el sistema.</span><span class="sxs-lookup"><span data-stu-id="30b59-136">System generated value assigned when created.</span></span>|
|<span data-ttu-id="30b59-137">displayName</span><span class="sxs-lookup"><span data-stu-id="30b59-137">displayName</span></span>|<span data-ttu-id="30b59-138">String</span><span class="sxs-lookup"><span data-stu-id="30b59-138">String</span></span>|<span data-ttu-id="30b59-139">El nombre definido de administración de la instrucción de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="30b59-139">The admin defined name of the management condition statement.</span></span>|
|<span data-ttu-id="30b59-140">descripción</span><span class="sxs-lookup"><span data-stu-id="30b59-140">description</span></span>|<span data-ttu-id="30b59-141">String</span><span class="sxs-lookup"><span data-stu-id="30b59-141">String</span></span>|<span data-ttu-id="30b59-142">El administrador define la descripción de la instrucción de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="30b59-142">The admin defined description of the management condition statement.</span></span>|
|<span data-ttu-id="30b59-143">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="30b59-143">createdDateTime</span></span>|<span data-ttu-id="30b59-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="30b59-144">DateTimeOffset</span></span>|<span data-ttu-id="30b59-145">La hora en que se creó la instrucción de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="30b59-145">The time the management condition statement was created.</span></span> <span data-ttu-id="30b59-146">Servicio generado al lado.</span><span class="sxs-lookup"><span data-stu-id="30b59-146">Generated service side.</span></span>|
|<span data-ttu-id="30b59-147">modifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="30b59-147">modifiedDateTime</span></span>|<span data-ttu-id="30b59-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="30b59-148">DateTimeOffset</span></span>|<span data-ttu-id="30b59-149">La hora en que se modificó por última vez la instrucción de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="30b59-149">The time the management condition statement was last modified.</span></span> <span data-ttu-id="30b59-150">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="30b59-150">Updated service side.</span></span>|
|<span data-ttu-id="30b59-151">expresión</span><span class="sxs-lookup"><span data-stu-id="30b59-151">expression</span></span>|[<span data-ttu-id="30b59-152">managementConditionExpression</span><span class="sxs-lookup"><span data-stu-id="30b59-152">managementConditionExpression</span></span>](../resources/intune-fencing-managementconditionexpression.md)|<span data-ttu-id="30b59-153">La expresión de instrucción de condición de administración que se usa para evaluar si una administración condición instrucción estaba activada o desactivada.</span><span class="sxs-lookup"><span data-stu-id="30b59-153">The management condition statement expression used to evaluate if a management condition statement was activated/deactivated.</span></span>|
|<span data-ttu-id="30b59-154">eTag</span><span class="sxs-lookup"><span data-stu-id="30b59-154">eTag</span></span>|<span data-ttu-id="30b59-155">String</span><span class="sxs-lookup"><span data-stu-id="30b59-155">String</span></span>|<span data-ttu-id="30b59-156">ETag de la instrucción de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="30b59-156">ETag of the management condition statement.</span></span> <span data-ttu-id="30b59-157">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="30b59-157">Updated service side.</span></span>|
|<span data-ttu-id="30b59-158">applicablePlatforms</span><span class="sxs-lookup"><span data-stu-id="30b59-158">applicablePlatforms</span></span>|<span data-ttu-id="30b59-159">colección de [devicePlatformType](../resources/intune-shared-deviceplatformtype.md)</span><span class="sxs-lookup"><span data-stu-id="30b59-159">[devicePlatformType](../resources/intune-shared-deviceplatformtype.md) collection</span></span>|<span data-ttu-id="30b59-160">Las plataformas aplicables para esta instrucción de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="30b59-160">The applicable platforms for this management condition statement.</span></span>
<span data-ttu-id="30b59-161">Esto se calcula a partir de ¿está buscando las condiciones de administración asociadas a la administración de la condición de la instrucción y buscar la intersección de plataformas aplicables.</span><span class="sxs-lookup"><span data-stu-id="30b59-161">This is calculated from looking the management conditions associated to the management condition statement and finding the intersection of applicable platforms.</span></span> <span data-ttu-id="30b59-162">Los valores posibles son: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater` y `androidWorkProfile`.</span><span class="sxs-lookup"><span data-stu-id="30b59-162">Possible values are: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile`.</span></span>|



## <a name="response"></a><span data-ttu-id="30b59-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30b59-163">Response</span></span>
<span data-ttu-id="30b59-164">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="30b59-164">If successful, this method returns a `201 Created` response code and a [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="30b59-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="30b59-165">Example</span></span>
### <a name="request"></a><span data-ttu-id="30b59-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="30b59-166">Request</span></span>
<span data-ttu-id="30b59-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="30b59-167">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/managementConditionStatements
Content-type: application/json
Content-length: 323

{
  "@odata.type": "#microsoft.graph.managementConditionStatement",
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

### <a name="response"></a><span data-ttu-id="30b59-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30b59-168">Response</span></span>
<span data-ttu-id="30b59-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="30b59-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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





