---
title: Crear embeddedSIMActivationCodePool
description: Crear un nuevo objeto embeddedSIMActivationCodePool.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a46245cb8f0a246363b5b1112298c360c3a4c24d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27973702"
---
# <a name="create-embeddedsimactivationcodepool"></a><span data-ttu-id="0eec4-103">Crear embeddedSIMActivationCodePool</span><span class="sxs-lookup"><span data-stu-id="0eec4-103">Create embeddedSIMActivationCodePool</span></span>

> <span data-ttu-id="0eec4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0eec4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0eec4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0eec4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0eec4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0eec4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0eec4-107">Crear un nuevo objeto [embeddedSIMActivationCodePool](../resources/intune-esim-embeddedsimactivationcodepool.md) .</span><span class="sxs-lookup"><span data-stu-id="0eec4-107">Create a new [embeddedSIMActivationCodePool](../resources/intune-esim-embeddedsimactivationcodepool.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0eec4-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0eec4-108">Prerequisites</span></span>
<span data-ttu-id="0eec4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0eec4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0eec4-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0eec4-111">Permission type</span></span>|<span data-ttu-id="0eec4-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0eec4-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0eec4-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0eec4-113">Delegated (work or school account)</span></span>|<span data-ttu-id="0eec4-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0eec4-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="0eec4-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0eec4-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0eec4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0eec4-116">Not supported.</span></span>|
|<span data-ttu-id="0eec4-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0eec4-117">Application</span></span>|<span data-ttu-id="0eec4-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0eec4-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0eec4-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0eec4-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/embeddedSIMActivationCodePools
```

## <a name="request-headers"></a><span data-ttu-id="0eec4-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0eec4-120">Request headers</span></span>
|<span data-ttu-id="0eec4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0eec4-121">Header</span></span>|<span data-ttu-id="0eec4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0eec4-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0eec4-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="0eec4-123">Authorization</span></span>|<span data-ttu-id="0eec4-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0eec4-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0eec4-125">Accept</span><span class="sxs-lookup"><span data-stu-id="0eec4-125">Accept</span></span>|<span data-ttu-id="0eec4-126">application/json</span><span class="sxs-lookup"><span data-stu-id="0eec4-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0eec4-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0eec4-127">Request body</span></span>
<span data-ttu-id="0eec4-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto embeddedSIMActivationCodePool.</span><span class="sxs-lookup"><span data-stu-id="0eec4-128">In the request body, supply a JSON representation for the embeddedSIMActivationCodePool object.</span></span>

<span data-ttu-id="0eec4-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el embeddedSIMActivationCodePool.</span><span class="sxs-lookup"><span data-stu-id="0eec4-129">The following table shows the properties that are required when you create the embeddedSIMActivationCodePool.</span></span>

|<span data-ttu-id="0eec4-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0eec4-130">Property</span></span>|<span data-ttu-id="0eec4-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="0eec4-131">Type</span></span>|<span data-ttu-id="0eec4-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="0eec4-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0eec4-133">id</span><span class="sxs-lookup"><span data-stu-id="0eec4-133">id</span></span>|<span data-ttu-id="0eec4-134">String</span><span class="sxs-lookup"><span data-stu-id="0eec4-134">String</span></span>|<span data-ttu-id="0eec4-135">Identificador único para el grupo de código de activación de SIM incrustado.</span><span class="sxs-lookup"><span data-stu-id="0eec4-135">Unique identifier for the embedded SIM activation code pool.</span></span> <span data-ttu-id="0eec4-136">Valor asignado al crear generada por el sistema.</span><span class="sxs-lookup"><span data-stu-id="0eec4-136">System generated value assigned when created.</span></span>|
|<span data-ttu-id="0eec4-137">displayName</span><span class="sxs-lookup"><span data-stu-id="0eec4-137">displayName</span></span>|<span data-ttu-id="0eec4-138">String</span><span class="sxs-lookup"><span data-stu-id="0eec4-138">String</span></span>|<span data-ttu-id="0eec4-139">El administrador definida por el nombre del grupo de código de activación SIM incrustado.</span><span class="sxs-lookup"><span data-stu-id="0eec4-139">The admin defined name of the embedded SIM activation code pool.</span></span>|
|<span data-ttu-id="0eec4-140">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="0eec4-140">createdDateTime</span></span>|<span data-ttu-id="0eec4-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0eec4-141">DateTimeOffset</span></span>|<span data-ttu-id="0eec4-142">La hora en que se creó el grupo de código de activación de SIM incrustado.</span><span class="sxs-lookup"><span data-stu-id="0eec4-142">The time the embedded SIM activation code pool was created.</span></span> <span data-ttu-id="0eec4-143">Servicio generado al lado.</span><span class="sxs-lookup"><span data-stu-id="0eec4-143">Generated service side.</span></span>|
|<span data-ttu-id="0eec4-144">modifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="0eec4-144">modifiedDateTime</span></span>|<span data-ttu-id="0eec4-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0eec4-145">DateTimeOffset</span></span>|<span data-ttu-id="0eec4-146">La hora en que se modificó por última vez el grupo de código de activación de SIM incrustado.</span><span class="sxs-lookup"><span data-stu-id="0eec4-146">The time the embedded SIM activation code pool was last modified.</span></span> <span data-ttu-id="0eec4-147">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="0eec4-147">Updated service side.</span></span>|
|<span data-ttu-id="0eec4-148">activationCodes</span><span class="sxs-lookup"><span data-stu-id="0eec4-148">activationCodes</span></span>|<span data-ttu-id="0eec4-149">colección de [embeddedSIMActivationCode](../resources/intune-esim-embeddedsimactivationcode.md)</span><span class="sxs-lookup"><span data-stu-id="0eec4-149">[embeddedSIMActivationCode](../resources/intune-esim-embeddedsimactivationcode.md) collection</span></span>|<span data-ttu-id="0eec4-150">Los códigos de activación que pertenecen a este grupo de servidores.</span><span class="sxs-lookup"><span data-stu-id="0eec4-150">The activation codes which belong to this pool.</span></span> <span data-ttu-id="0eec4-151">Esta propiedad de navegación se usa para registrar los códigos de activación para Intune pero no se puede usar para leer los códigos de activación de Intune.</span><span class="sxs-lookup"><span data-stu-id="0eec4-151">This navigation property is used to post activation codes to Intune but cannot be used to read activation codes from Intune.</span></span>|
|<span data-ttu-id="0eec4-152">activationCodeCount</span><span class="sxs-lookup"><span data-stu-id="0eec4-152">activationCodeCount</span></span>|<span data-ttu-id="0eec4-153">Int32</span><span class="sxs-lookup"><span data-stu-id="0eec4-153">Int32</span></span>|<span data-ttu-id="0eec4-154">El número total de códigos de activación que pertenecen a este grupo de servidores.</span><span class="sxs-lookup"><span data-stu-id="0eec4-154">The total count of activation codes which belong to this pool.</span></span>|



## <a name="response"></a><span data-ttu-id="0eec4-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0eec4-155">Response</span></span>
<span data-ttu-id="0eec4-156">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [embeddedSIMActivationCodePool](../resources/intune-esim-embeddedsimactivationcodepool.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0eec4-156">If successful, this method returns a `201 Created` response code and a [embeddedSIMActivationCodePool](../resources/intune-esim-embeddedsimactivationcodepool.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0eec4-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0eec4-157">Example</span></span>
### <a name="request"></a><span data-ttu-id="0eec4-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0eec4-158">Request</span></span>
<span data-ttu-id="0eec4-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0eec4-159">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/embeddedSIMActivationCodePools
Content-type: application/json
Content-length: 460

{
  "@odata.type": "#microsoft.graph.embeddedSIMActivationCodePool",
  "displayName": "Display Name value",
  "activationCodes": [
    {
      "@odata.type": "microsoft.graph.embeddedSIMActivationCode",
      "integratedCircuitCardIdentifier": "Integrated Circuit Card Identifier value",
      "matchingIdentifier": "Matching Identifier value",
      "smdpPlusServerAddress": "Smdp Plus Server Address value"
    }
  ],
  "activationCodeCount": 3
}
```

### <a name="response"></a><span data-ttu-id="0eec4-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0eec4-160">Response</span></span>
<span data-ttu-id="0eec4-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0eec4-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 628

{
  "@odata.type": "#microsoft.graph.embeddedSIMActivationCodePool",
  "id": "ec308741-8741-ec30-4187-30ec418730ec",
  "displayName": "Display Name value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "modifiedDateTime": "2017-01-01T00:00:22.8983556-08:00",
  "activationCodes": [
    {
      "@odata.type": "microsoft.graph.embeddedSIMActivationCode",
      "integratedCircuitCardIdentifier": "Integrated Circuit Card Identifier value",
      "matchingIdentifier": "Matching Identifier value",
      "smdpPlusServerAddress": "Smdp Plus Server Address value"
    }
  ],
  "activationCodeCount": 3
}
```





