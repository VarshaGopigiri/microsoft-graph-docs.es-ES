---
title: Crear termsAndConditions
description: Cree un objeto termsAndConditions.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 262390218470408edbf7d63ee00142c9b8e2b789
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972274"
---
# <a name="create-termsandconditions"></a><span data-ttu-id="e5507-103">Crear termsAndConditions</span><span class="sxs-lookup"><span data-stu-id="e5507-103">Create termsAndConditions</span></span>

> <span data-ttu-id="e5507-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e5507-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e5507-105">Cree un objeto [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).</span><span class="sxs-lookup"><span data-stu-id="e5507-105">Create a new [termsAndConditions](../resources/intune-companyterms-termsandconditions.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e5507-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e5507-106">Prerequisites</span></span>
<span data-ttu-id="e5507-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e5507-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e5507-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e5507-109">Permission type</span></span>|<span data-ttu-id="e5507-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e5507-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e5507-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e5507-111">Delegated (work or school account)</span></span>|<span data-ttu-id="e5507-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e5507-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="e5507-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e5507-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e5507-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e5507-114">Not supported.</span></span>|
|<span data-ttu-id="e5507-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e5507-115">Application</span></span>|<span data-ttu-id="e5507-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e5507-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e5507-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e5507-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/termsAndConditions
```

## <a name="request-headers"></a><span data-ttu-id="e5507-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e5507-118">Request headers</span></span>
|<span data-ttu-id="e5507-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e5507-119">Header</span></span>|<span data-ttu-id="e5507-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e5507-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e5507-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="e5507-121">Authorization</span></span>|<span data-ttu-id="e5507-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e5507-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e5507-123">Accept</span><span class="sxs-lookup"><span data-stu-id="e5507-123">Accept</span></span>|<span data-ttu-id="e5507-124">application/json</span><span class="sxs-lookup"><span data-stu-id="e5507-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e5507-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e5507-125">Request body</span></span>
<span data-ttu-id="e5507-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto termsAndConditions.</span><span class="sxs-lookup"><span data-stu-id="e5507-126">In the request body, supply a JSON representation for the termsAndConditions object.</span></span>

<span data-ttu-id="e5507-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto termsAndConditions.</span><span class="sxs-lookup"><span data-stu-id="e5507-127">The following table shows the properties that are required when you create the termsAndConditions.</span></span>

|<span data-ttu-id="e5507-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e5507-128">Property</span></span>|<span data-ttu-id="e5507-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5507-129">Type</span></span>|<span data-ttu-id="e5507-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5507-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e5507-131">id</span><span class="sxs-lookup"><span data-stu-id="e5507-131">id</span></span>|<span data-ttu-id="e5507-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="e5507-132">String</span></span>|<span data-ttu-id="e5507-133">Identificador único de la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="e5507-133">Unique identifier of the T&C policy.</span></span>|
|<span data-ttu-id="e5507-134">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e5507-134">createdDateTime</span></span>|<span data-ttu-id="e5507-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e5507-135">DateTimeOffset</span></span>|<span data-ttu-id="e5507-136">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="e5507-136">DateTime the object was created.</span></span>|
|<span data-ttu-id="e5507-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e5507-137">lastModifiedDateTime</span></span>|<span data-ttu-id="e5507-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e5507-138">DateTimeOffset</span></span>|<span data-ttu-id="e5507-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="e5507-139">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="e5507-140">displayName</span><span class="sxs-lookup"><span data-stu-id="e5507-140">displayName</span></span>|<span data-ttu-id="e5507-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="e5507-141">String</span></span>|<span data-ttu-id="e5507-142">Nombre proporcionado por el administrador de la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="e5507-142">Administrator-supplied name for the T&C policy.</span></span> |
|<span data-ttu-id="e5507-143">description</span><span class="sxs-lookup"><span data-stu-id="e5507-143">description</span></span>|<span data-ttu-id="e5507-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="e5507-144">String</span></span>|<span data-ttu-id="e5507-145">Descripción de la directiva de TyC proporcionada por el administrador.</span><span class="sxs-lookup"><span data-stu-id="e5507-145">Administrator-supplied description of the T&C policy.</span></span>|
|<span data-ttu-id="e5507-146">title</span><span class="sxs-lookup"><span data-stu-id="e5507-146">title</span></span>|<span data-ttu-id="e5507-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="e5507-147">String</span></span>|<span data-ttu-id="e5507-148">Título de los términos y condiciones proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="e5507-148">Administrator-supplied title of the terms and conditions.</span></span> <span data-ttu-id="e5507-149">Se muestra a los usuarios cuando se les solicita que acepten la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="e5507-149">This is shown to the user on prompts to accept the T&C policy.</span></span>|
|<span data-ttu-id="e5507-150">bodyText</span><span class="sxs-lookup"><span data-stu-id="e5507-150">bodyText</span></span>|<span data-ttu-id="e5507-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="e5507-151">String</span></span>|<span data-ttu-id="e5507-152">Texto de cuerpo de los términos y condiciones proporcionado por el administrador, normalmente los propios términos.</span><span class="sxs-lookup"><span data-stu-id="e5507-152">Administrator-supplied body text of the terms and conditions, typically the terms themselves.</span></span> <span data-ttu-id="e5507-153">Se muestra a los usuarios cuando se les solicita que acepten la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="e5507-153">This is shown to the user on prompts to accept the T&C policy.</span></span>|
|<span data-ttu-id="e5507-154">acceptanceStatement</span><span class="sxs-lookup"><span data-stu-id="e5507-154">acceptanceStatement</span></span>|<span data-ttu-id="e5507-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="e5507-155">String</span></span>|<span data-ttu-id="e5507-156">Explicación de los términos y condiciones proporcionada por el administrador, normalmente describe lo que implica aceptar los términos y condiciones de la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="e5507-156">Administrator-supplied explanation of the terms and conditions, typically describing what it means to accept the terms and conditions set out in the T&C policy.</span></span> <span data-ttu-id="e5507-157">Se muestra a los usuarios cuando se les solicita que acepten la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="e5507-157">This is shown to the user on prompts to accept the T&C policy.</span></span>|
|<span data-ttu-id="e5507-158">version</span><span class="sxs-lookup"><span data-stu-id="e5507-158">version</span></span>|<span data-ttu-id="e5507-159">Int32</span><span class="sxs-lookup"><span data-stu-id="e5507-159">Int32</span></span>|<span data-ttu-id="e5507-160">Entero que indica la versión actual de los términos.</span><span class="sxs-lookup"><span data-stu-id="e5507-160">Integer indicating the current version of the terms.</span></span> <span data-ttu-id="e5507-161">Aumenta cuando un administrador realiza un cambio en los términos y quiere que los usuarios tengan que volver a aceptar la directiva de TyC modificada.</span><span class="sxs-lookup"><span data-stu-id="e5507-161">Incremented when an administrator makes a change to the terms and wishes to require users to re-accept the modified T&C policy.</span></span>|



## <a name="response"></a><span data-ttu-id="e5507-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5507-162">Response</span></span>
<span data-ttu-id="e5507-163">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [termsAndConditions](../resources/intune-companyterms-termsandconditions.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e5507-163">If successful, this method returns a `201 Created` response code and a [termsAndConditions](../resources/intune-companyterms-termsandconditions.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e5507-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e5507-164">Example</span></span>
### <a name="request"></a><span data-ttu-id="e5507-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e5507-165">Request</span></span>
<span data-ttu-id="e5507-166">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e5507-166">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/termsAndConditions
Content-type: application/json
Content-length: 273

{
  "@odata.type": "#microsoft.graph.termsAndConditions",
  "displayName": "Display Name value",
  "description": "Description value",
  "title": "Title value",
  "bodyText": "Body Text value",
  "acceptanceStatement": "Acceptance Statement value",
  "version": 7
}
```

### <a name="response"></a><span data-ttu-id="e5507-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5507-167">Response</span></span>
<span data-ttu-id="e5507-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e5507-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 445

{
  "@odata.type": "#microsoft.graph.termsAndConditions",
  "id": "eefc80cf-80cf-eefc-cf80-fceecf80fcee",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "description": "Description value",
  "title": "Title value",
  "bodyText": "Body Text value",
  "acceptanceStatement": "Acceptance Statement value",
  "version": 7
}
```



