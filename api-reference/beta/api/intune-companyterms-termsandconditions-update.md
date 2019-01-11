---
title: Actualizar termsAndConditions
description: Actualice las propiedades de un objeto termsAndConditions.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7617e58dcae72f4f69c08c5f4dfa8c373df8edd1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27852818"
---
# <a name="update-termsandconditions"></a><span data-ttu-id="508c4-103">Actualizar termsAndConditions</span><span class="sxs-lookup"><span data-stu-id="508c4-103">Update termsAndConditions</span></span>

> <span data-ttu-id="508c4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="508c4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="508c4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="508c4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="508c4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="508c4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="508c4-107">Actualice las propiedades de un objeto [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).</span><span class="sxs-lookup"><span data-stu-id="508c4-107">Update the properties of a [termsAndConditions](../resources/intune-companyterms-termsandconditions.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="508c4-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="508c4-108">Prerequisites</span></span>
<span data-ttu-id="508c4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="508c4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="508c4-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="508c4-111">Permission type</span></span>|<span data-ttu-id="508c4-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="508c4-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="508c4-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="508c4-113">Delegated (work or school account)</span></span>|<span data-ttu-id="508c4-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="508c4-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="508c4-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="508c4-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="508c4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="508c4-116">Not supported.</span></span>|
|<span data-ttu-id="508c4-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="508c4-117">Application</span></span>|<span data-ttu-id="508c4-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="508c4-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="508c4-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="508c4-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/termsAndConditions/{termsAndConditionsId}
PATCH /deviceManagement/termsAndConditions/{termsAndConditionsId}/groupAssignments/{termsAndConditionsGroupAssignmentId}/termsAndConditions
PATCH /deviceManagement/termsAndConditions/{termsAndConditionsId}/acceptanceStatuses/{termsAndConditionsAcceptanceStatusId}/termsAndConditions
```

## <a name="request-headers"></a><span data-ttu-id="508c4-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="508c4-120">Request headers</span></span>
|<span data-ttu-id="508c4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="508c4-121">Header</span></span>|<span data-ttu-id="508c4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="508c4-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="508c4-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="508c4-123">Authorization</span></span>|<span data-ttu-id="508c4-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="508c4-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="508c4-125">Accept</span><span class="sxs-lookup"><span data-stu-id="508c4-125">Accept</span></span>|<span data-ttu-id="508c4-126">application/json</span><span class="sxs-lookup"><span data-stu-id="508c4-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="508c4-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="508c4-127">Request body</span></span>
<span data-ttu-id="508c4-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).</span><span class="sxs-lookup"><span data-stu-id="508c4-128">In the request body, supply a JSON representation for the [termsAndConditions](../resources/intune-companyterms-termsandconditions.md) object.</span></span>

<span data-ttu-id="508c4-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).</span><span class="sxs-lookup"><span data-stu-id="508c4-129">The following table shows the properties that are required when you create the [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).</span></span>

|<span data-ttu-id="508c4-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="508c4-130">Property</span></span>|<span data-ttu-id="508c4-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="508c4-131">Type</span></span>|<span data-ttu-id="508c4-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="508c4-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="508c4-133">id</span><span class="sxs-lookup"><span data-stu-id="508c4-133">id</span></span>|<span data-ttu-id="508c4-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="508c4-134">String</span></span>|<span data-ttu-id="508c4-135">Identificador único de la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="508c4-135">Unique identifier of the T&C policy.</span></span>|
|<span data-ttu-id="508c4-136">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="508c4-136">createdDateTime</span></span>|<span data-ttu-id="508c4-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="508c4-137">DateTimeOffset</span></span>|<span data-ttu-id="508c4-138">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="508c4-138">DateTime the object was created.</span></span>|
|<span data-ttu-id="508c4-139">modifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="508c4-139">modifiedDateTime</span></span>|<span data-ttu-id="508c4-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="508c4-140">DateTimeOffset</span></span>|<span data-ttu-id="508c4-141">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="508c4-141">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="508c4-142">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="508c4-142">lastModifiedDateTime</span></span>|<span data-ttu-id="508c4-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="508c4-143">DateTimeOffset</span></span>|<span data-ttu-id="508c4-144">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="508c4-144">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="508c4-145">displayName</span><span class="sxs-lookup"><span data-stu-id="508c4-145">displayName</span></span>|<span data-ttu-id="508c4-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="508c4-146">String</span></span>|<span data-ttu-id="508c4-147">Nombre proporcionado por el administrador de la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="508c4-147">Administrator-supplied name for the T&C policy.</span></span> |
|<span data-ttu-id="508c4-148">description</span><span class="sxs-lookup"><span data-stu-id="508c4-148">description</span></span>|<span data-ttu-id="508c4-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="508c4-149">String</span></span>|<span data-ttu-id="508c4-150">Descripción de la directiva de TyC proporcionada por el administrador.</span><span class="sxs-lookup"><span data-stu-id="508c4-150">Administrator-supplied description of the T&C policy.</span></span>|
|<span data-ttu-id="508c4-151">title</span><span class="sxs-lookup"><span data-stu-id="508c4-151">title</span></span>|<span data-ttu-id="508c4-152">Cadena</span><span class="sxs-lookup"><span data-stu-id="508c4-152">String</span></span>|<span data-ttu-id="508c4-153">Título de los términos y condiciones proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="508c4-153">Administrator-supplied title of the terms and conditions.</span></span> <span data-ttu-id="508c4-154">Se muestra a los usuarios cuando se les solicita que acepten la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="508c4-154">This is shown to the user on prompts to accept the T&C policy.</span></span>|
|<span data-ttu-id="508c4-155">bodyText</span><span class="sxs-lookup"><span data-stu-id="508c4-155">bodyText</span></span>|<span data-ttu-id="508c4-156">Cadena</span><span class="sxs-lookup"><span data-stu-id="508c4-156">String</span></span>|<span data-ttu-id="508c4-157">Texto de cuerpo de los términos y condiciones proporcionado por el administrador, normalmente los propios términos.</span><span class="sxs-lookup"><span data-stu-id="508c4-157">Administrator-supplied body text of the terms and conditions, typically the terms themselves.</span></span> <span data-ttu-id="508c4-158">Se muestra a los usuarios cuando se les solicita que acepten la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="508c4-158">This is shown to the user on prompts to accept the T&C policy.</span></span>|
|<span data-ttu-id="508c4-159">acceptanceStatement</span><span class="sxs-lookup"><span data-stu-id="508c4-159">acceptanceStatement</span></span>|<span data-ttu-id="508c4-160">Cadena</span><span class="sxs-lookup"><span data-stu-id="508c4-160">String</span></span>|<span data-ttu-id="508c4-161">Explicación de los términos y condiciones proporcionada por el administrador, normalmente describe lo que implica aceptar los términos y condiciones de la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="508c4-161">Administrator-supplied explanation of the terms and conditions, typically describing what it means to accept the terms and conditions set out in the T&C policy.</span></span> <span data-ttu-id="508c4-162">Se muestra a los usuarios cuando se les solicita que acepten la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="508c4-162">This is shown to the user on prompts to accept the T&C policy.</span></span>|
|<span data-ttu-id="508c4-163">version</span><span class="sxs-lookup"><span data-stu-id="508c4-163">version</span></span>|<span data-ttu-id="508c4-164">Int32</span><span class="sxs-lookup"><span data-stu-id="508c4-164">Int32</span></span>|<span data-ttu-id="508c4-165">Entero que indica la versión actual de los términos.</span><span class="sxs-lookup"><span data-stu-id="508c4-165">Integer indicating the current version of the terms.</span></span> <span data-ttu-id="508c4-166">Aumenta cuando un administrador realiza un cambio en los términos y quiere que los usuarios tengan que volver a aceptar la directiva de TyC modificada.</span><span class="sxs-lookup"><span data-stu-id="508c4-166">Incremented when an administrator makes a change to the terms and wishes to require users to re-accept the modified T&C policy.</span></span>|



## <a name="response"></a><span data-ttu-id="508c4-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="508c4-167">Response</span></span>
<span data-ttu-id="508c4-168">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [termsAndConditions](../resources/intune-companyterms-termsandconditions.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="508c4-168">If successful, this method returns a `200 OK` response code and an updated [termsAndConditions](../resources/intune-companyterms-termsandconditions.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="508c4-169">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="508c4-169">Example</span></span>
### <a name="request"></a><span data-ttu-id="508c4-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="508c4-170">Request</span></span>
<span data-ttu-id="508c4-171">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="508c4-171">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="508c4-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="508c4-172">Response</span></span>
<span data-ttu-id="508c4-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="508c4-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





