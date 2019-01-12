---
title: Actualizar termsAndConditions
description: Actualice las propiedades de un objeto termsAndConditions.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 3a713e2d2af3ebf5218ed27d6e30cdeb5239bd9e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27929490"
---
# <a name="update-termsandconditions"></a><span data-ttu-id="72820-103">Actualizar termsAndConditions</span><span class="sxs-lookup"><span data-stu-id="72820-103">Update termsAndConditions</span></span>

> <span data-ttu-id="72820-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="72820-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="72820-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="72820-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="72820-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="72820-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="72820-107">Actualice las propiedades de un objeto [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).</span><span class="sxs-lookup"><span data-stu-id="72820-107">Update the properties of a [termsAndConditions](../resources/intune-companyterms-termsandconditions.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="72820-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="72820-108">Prerequisites</span></span>
<span data-ttu-id="72820-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="72820-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="72820-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="72820-111">Permission type</span></span>|<span data-ttu-id="72820-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="72820-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="72820-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="72820-113">Delegated (work or school account)</span></span>|<span data-ttu-id="72820-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="72820-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="72820-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="72820-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="72820-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="72820-116">Not supported.</span></span>|
|<span data-ttu-id="72820-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="72820-117">Application</span></span>|<span data-ttu-id="72820-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="72820-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="72820-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="72820-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/termsAndConditions/{termsAndConditionsId}
PATCH /deviceManagement/termsAndConditions/{termsAndConditionsId}/groupAssignments/{termsAndConditionsGroupAssignmentId}/termsAndConditions
PATCH /deviceManagement/termsAndConditions/{termsAndConditionsId}/acceptanceStatuses/{termsAndConditionsAcceptanceStatusId}/termsAndConditions
```

## <a name="request-headers"></a><span data-ttu-id="72820-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="72820-120">Request headers</span></span>
|<span data-ttu-id="72820-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72820-121">Header</span></span>|<span data-ttu-id="72820-122">Valor</span><span class="sxs-lookup"><span data-stu-id="72820-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="72820-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="72820-123">Authorization</span></span>|<span data-ttu-id="72820-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="72820-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="72820-125">Accept</span><span class="sxs-lookup"><span data-stu-id="72820-125">Accept</span></span>|<span data-ttu-id="72820-126">application/json</span><span class="sxs-lookup"><span data-stu-id="72820-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="72820-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="72820-127">Request body</span></span>
<span data-ttu-id="72820-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).</span><span class="sxs-lookup"><span data-stu-id="72820-128">In the request body, supply a JSON representation for the [termsAndConditions](../resources/intune-companyterms-termsandconditions.md) object.</span></span>

<span data-ttu-id="72820-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).</span><span class="sxs-lookup"><span data-stu-id="72820-129">The following table shows the properties that are required when you create the [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).</span></span>

|<span data-ttu-id="72820-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="72820-130">Property</span></span>|<span data-ttu-id="72820-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="72820-131">Type</span></span>|<span data-ttu-id="72820-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="72820-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="72820-133">id</span><span class="sxs-lookup"><span data-stu-id="72820-133">id</span></span>|<span data-ttu-id="72820-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="72820-134">String</span></span>|<span data-ttu-id="72820-135">Identificador único de la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="72820-135">Unique identifier of the T&C policy.</span></span>|
|<span data-ttu-id="72820-136">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="72820-136">createdDateTime</span></span>|<span data-ttu-id="72820-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="72820-137">DateTimeOffset</span></span>|<span data-ttu-id="72820-138">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="72820-138">DateTime the object was created.</span></span>|
|<span data-ttu-id="72820-139">modifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="72820-139">modifiedDateTime</span></span>|<span data-ttu-id="72820-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="72820-140">DateTimeOffset</span></span>|<span data-ttu-id="72820-141">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="72820-141">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="72820-142">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="72820-142">lastModifiedDateTime</span></span>|<span data-ttu-id="72820-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="72820-143">DateTimeOffset</span></span>|<span data-ttu-id="72820-144">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="72820-144">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="72820-145">displayName</span><span class="sxs-lookup"><span data-stu-id="72820-145">displayName</span></span>|<span data-ttu-id="72820-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="72820-146">String</span></span>|<span data-ttu-id="72820-147">Nombre proporcionado por el administrador de la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="72820-147">Administrator-supplied name for the T&C policy.</span></span> |
|<span data-ttu-id="72820-148">description</span><span class="sxs-lookup"><span data-stu-id="72820-148">description</span></span>|<span data-ttu-id="72820-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="72820-149">String</span></span>|<span data-ttu-id="72820-150">Descripción de la directiva de TyC proporcionada por el administrador.</span><span class="sxs-lookup"><span data-stu-id="72820-150">Administrator-supplied description of the T&C policy.</span></span>|
|<span data-ttu-id="72820-151">title</span><span class="sxs-lookup"><span data-stu-id="72820-151">title</span></span>|<span data-ttu-id="72820-152">Cadena</span><span class="sxs-lookup"><span data-stu-id="72820-152">String</span></span>|<span data-ttu-id="72820-153">Título de los términos y condiciones proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="72820-153">Administrator-supplied title of the terms and conditions.</span></span> <span data-ttu-id="72820-154">Se muestra a los usuarios cuando se les solicita que acepten la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="72820-154">This is shown to the user on prompts to accept the T&C policy.</span></span>|
|<span data-ttu-id="72820-155">bodyText</span><span class="sxs-lookup"><span data-stu-id="72820-155">bodyText</span></span>|<span data-ttu-id="72820-156">Cadena</span><span class="sxs-lookup"><span data-stu-id="72820-156">String</span></span>|<span data-ttu-id="72820-157">Texto de cuerpo de los términos y condiciones proporcionado por el administrador, normalmente los propios términos.</span><span class="sxs-lookup"><span data-stu-id="72820-157">Administrator-supplied body text of the terms and conditions, typically the terms themselves.</span></span> <span data-ttu-id="72820-158">Se muestra a los usuarios cuando se les solicita que acepten la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="72820-158">This is shown to the user on prompts to accept the T&C policy.</span></span>|
|<span data-ttu-id="72820-159">acceptanceStatement</span><span class="sxs-lookup"><span data-stu-id="72820-159">acceptanceStatement</span></span>|<span data-ttu-id="72820-160">Cadena</span><span class="sxs-lookup"><span data-stu-id="72820-160">String</span></span>|<span data-ttu-id="72820-161">Explicación de los términos y condiciones proporcionada por el administrador, normalmente describe lo que implica aceptar los términos y condiciones de la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="72820-161">Administrator-supplied explanation of the terms and conditions, typically describing what it means to accept the terms and conditions set out in the T&C policy.</span></span> <span data-ttu-id="72820-162">Se muestra a los usuarios cuando se les solicita que acepten la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="72820-162">This is shown to the user on prompts to accept the T&C policy.</span></span>|
|<span data-ttu-id="72820-163">version</span><span class="sxs-lookup"><span data-stu-id="72820-163">version</span></span>|<span data-ttu-id="72820-164">Int32</span><span class="sxs-lookup"><span data-stu-id="72820-164">Int32</span></span>|<span data-ttu-id="72820-165">Entero que indica la versión actual de los términos.</span><span class="sxs-lookup"><span data-stu-id="72820-165">Integer indicating the current version of the terms.</span></span> <span data-ttu-id="72820-166">Aumenta cuando un administrador realiza un cambio en los términos y quiere que los usuarios tengan que volver a aceptar la directiva de TyC modificada.</span><span class="sxs-lookup"><span data-stu-id="72820-166">Incremented when an administrator makes a change to the terms and wishes to require users to re-accept the modified T&C policy.</span></span>|



## <a name="response"></a><span data-ttu-id="72820-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="72820-167">Response</span></span>
<span data-ttu-id="72820-168">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [termsAndConditions](../resources/intune-companyterms-termsandconditions.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="72820-168">If successful, this method returns a `200 OK` response code and an updated [termsAndConditions](../resources/intune-companyterms-termsandconditions.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="72820-169">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="72820-169">Example</span></span>
### <a name="request"></a><span data-ttu-id="72820-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="72820-170">Request</span></span>
<span data-ttu-id="72820-171">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="72820-171">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/termsAndConditions/{termsAndConditionsId}
Content-type: application/json
Content-length: 280

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "description": "Description value",
  "title": "Title value",
  "bodyText": "Body Text value",
  "acceptanceStatement": "Acceptance Statement value",
  "version": 7
}
```

### <a name="response"></a><span data-ttu-id="72820-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="72820-172">Response</span></span>
<span data-ttu-id="72820-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="72820-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 505

{
  "@odata.type": "#microsoft.graph.termsAndConditions",
  "id": "eefc80cf-80cf-eefc-cf80-fceecf80fcee",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "modifiedDateTime": "2017-01-01T00:00:22.8983556-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "description": "Description value",
  "title": "Title value",
  "bodyText": "Body Text value",
  "acceptanceStatement": "Acceptance Statement value",
  "version": 7
}
```





