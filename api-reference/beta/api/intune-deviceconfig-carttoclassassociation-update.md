---
title: Actualizar cartToClassAssociation
description: Actualizar las propiedades de un objeto cartToClassAssociation.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a140aa3e14895cf0fc7dd5ca2be54afdb1d86052
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27967682"
---
# <a name="update-carttoclassassociation"></a><span data-ttu-id="94b95-103">Actualizar cartToClassAssociation</span><span class="sxs-lookup"><span data-stu-id="94b95-103">Update cartToClassAssociation</span></span>

> <span data-ttu-id="94b95-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="94b95-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="94b95-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="94b95-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="94b95-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="94b95-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="94b95-107">Actualizar las propiedades de un objeto [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md) .</span><span class="sxs-lookup"><span data-stu-id="94b95-107">Update the properties of a [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="94b95-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="94b95-108">Prerequisites</span></span>
<span data-ttu-id="94b95-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="94b95-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="94b95-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="94b95-111">Permission type</span></span>|<span data-ttu-id="94b95-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="94b95-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="94b95-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="94b95-113">Delegated (work or school account)</span></span>|<span data-ttu-id="94b95-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="94b95-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="94b95-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="94b95-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="94b95-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="94b95-116">Not supported.</span></span>|
|<span data-ttu-id="94b95-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="94b95-117">Application</span></span>|<span data-ttu-id="94b95-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="94b95-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="94b95-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="94b95-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/cartToClassAssociations/{cartToClassAssociationId}
```

## <a name="request-headers"></a><span data-ttu-id="94b95-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="94b95-120">Request headers</span></span>
|<span data-ttu-id="94b95-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94b95-121">Header</span></span>|<span data-ttu-id="94b95-122">Valor</span><span class="sxs-lookup"><span data-stu-id="94b95-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="94b95-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="94b95-123">Authorization</span></span>|<span data-ttu-id="94b95-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="94b95-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="94b95-125">Accept</span><span class="sxs-lookup"><span data-stu-id="94b95-125">Accept</span></span>|<span data-ttu-id="94b95-126">application/json</span><span class="sxs-lookup"><span data-stu-id="94b95-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="94b95-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="94b95-127">Request body</span></span>
<span data-ttu-id="94b95-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md) .</span><span class="sxs-lookup"><span data-stu-id="94b95-128">In the request body, supply a JSON representation for the [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md) object.</span></span>

<span data-ttu-id="94b95-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md).</span><span class="sxs-lookup"><span data-stu-id="94b95-129">The following table shows the properties that are required when you create the [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md).</span></span>

|<span data-ttu-id="94b95-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="94b95-130">Property</span></span>|<span data-ttu-id="94b95-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="94b95-131">Type</span></span>|<span data-ttu-id="94b95-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="94b95-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="94b95-133">id</span><span class="sxs-lookup"><span data-stu-id="94b95-133">id</span></span>|<span data-ttu-id="94b95-134">String</span><span class="sxs-lookup"><span data-stu-id="94b95-134">String</span></span>|<span data-ttu-id="94b95-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="94b95-135">Key of the entity.</span></span>|
|<span data-ttu-id="94b95-136">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="94b95-136">createdDateTime</span></span>|<span data-ttu-id="94b95-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="94b95-137">DateTimeOffset</span></span>|<span data-ttu-id="94b95-138">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="94b95-138">DateTime the object was created.</span></span>|
|<span data-ttu-id="94b95-139">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="94b95-139">lastModifiedDateTime</span></span>|<span data-ttu-id="94b95-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="94b95-140">DateTimeOffset</span></span>|<span data-ttu-id="94b95-141">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="94b95-141">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="94b95-142">version</span><span class="sxs-lookup"><span data-stu-id="94b95-142">version</span></span>|<span data-ttu-id="94b95-143">Int32</span><span class="sxs-lookup"><span data-stu-id="94b95-143">Int32</span></span>|<span data-ttu-id="94b95-144">Versión de la CartToClassAssociation.</span><span class="sxs-lookup"><span data-stu-id="94b95-144">Version of the CartToClassAssociation.</span></span>|
|<span data-ttu-id="94b95-145">displayName</span><span class="sxs-lookup"><span data-stu-id="94b95-145">displayName</span></span>|<span data-ttu-id="94b95-146">String</span><span class="sxs-lookup"><span data-stu-id="94b95-146">String</span></span>|<span data-ttu-id="94b95-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94b95-147">Admin provided name of the device configuration.</span></span>|
|<span data-ttu-id="94b95-148">descripción</span><span class="sxs-lookup"><span data-stu-id="94b95-148">description</span></span>|<span data-ttu-id="94b95-149">String</span><span class="sxs-lookup"><span data-stu-id="94b95-149">String</span></span>|<span data-ttu-id="94b95-150">Descripción de la CartToClassAssociation proporcionada por el administrador.</span><span class="sxs-lookup"><span data-stu-id="94b95-150">Admin provided description of the CartToClassAssociation.</span></span>|
|<span data-ttu-id="94b95-151">deviceCartIds</span><span class="sxs-lookup"><span data-stu-id="94b95-151">deviceCartIds</span></span>|<span data-ttu-id="94b95-152">Colección String</span><span class="sxs-lookup"><span data-stu-id="94b95-152">String collection</span></span>|<span data-ttu-id="94b95-153">Identificadores de carros de dispositivo que se asociará con clases.</span><span class="sxs-lookup"><span data-stu-id="94b95-153">Identifiers of device carts to be associated with classes.</span></span>|
|<span data-ttu-id="94b95-154">classroomIds</span><span class="sxs-lookup"><span data-stu-id="94b95-154">classroomIds</span></span>|<span data-ttu-id="94b95-155">Colección String</span><span class="sxs-lookup"><span data-stu-id="94b95-155">String collection</span></span>|<span data-ttu-id="94b95-156">Identificadores de aulas que se asociará con carros de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94b95-156">Identifiers of classrooms to be associated with device carts.</span></span>|



## <a name="response"></a><span data-ttu-id="94b95-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="94b95-157">Response</span></span>
<span data-ttu-id="94b95-158">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="94b95-158">If successful, this method returns a `200 OK` response code and an updated [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="94b95-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="94b95-159">Example</span></span>
### <a name="request"></a><span data-ttu-id="94b95-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="94b95-160">Request</span></span>
<span data-ttu-id="94b95-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="94b95-161">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/cartToClassAssociations/{cartToClassAssociationId}
Content-type: application/json
Content-length: 274

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "displayName": "Display Name value",
  "description": "Description value",
  "deviceCartIds": [
    "Device Cart Ids value"
  ],
  "classroomIds": [
    "Classroom Ids value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="94b95-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="94b95-162">Response</span></span>
<span data-ttu-id="94b95-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="94b95-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 443

{
  "@odata.type": "#microsoft.graph.cartToClassAssociation",
  "id": "9bdc58dd-58dd-9bdc-dd58-dc9bdd58dc9b",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "displayName": "Display Name value",
  "description": "Description value",
  "deviceCartIds": [
    "Device Cart Ids value"
  ],
  "classroomIds": [
    "Classroom Ids value"
  ]
}
```





