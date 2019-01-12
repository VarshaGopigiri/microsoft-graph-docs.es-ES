---
title: Crear managedEBookCategory
description: Crear un nuevo objeto managedEBookCategory.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: f86f3570f63a6aa3982e9cb2ffbf659d1a9a752c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990253"
---
# <a name="create-managedebookcategory"></a><span data-ttu-id="04fe5-103">Crear managedEBookCategory</span><span class="sxs-lookup"><span data-stu-id="04fe5-103">Create managedEBookCategory</span></span>

> <span data-ttu-id="04fe5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="04fe5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="04fe5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="04fe5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="04fe5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="04fe5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="04fe5-107">Crear un nuevo objeto [managedEBookCategory](../resources/intune-books-managedebookcategory.md) .</span><span class="sxs-lookup"><span data-stu-id="04fe5-107">Create a new [managedEBookCategory](../resources/intune-books-managedebookcategory.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="04fe5-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="04fe5-108">Prerequisites</span></span>
<span data-ttu-id="04fe5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="04fe5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="04fe5-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="04fe5-111">Permission type</span></span>|<span data-ttu-id="04fe5-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="04fe5-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="04fe5-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="04fe5-113">Delegated (work or school account)</span></span>|<span data-ttu-id="04fe5-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="04fe5-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="04fe5-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="04fe5-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="04fe5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="04fe5-116">Not supported.</span></span>|
|<span data-ttu-id="04fe5-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="04fe5-117">Application</span></span>|<span data-ttu-id="04fe5-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="04fe5-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="04fe5-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="04fe5-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBookCategories
POST /deviceAppManagement/managedEBooks/{managedEBookId}/categories
```

## <a name="request-headers"></a><span data-ttu-id="04fe5-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="04fe5-120">Request headers</span></span>
|<span data-ttu-id="04fe5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04fe5-121">Header</span></span>|<span data-ttu-id="04fe5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="04fe5-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="04fe5-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="04fe5-123">Authorization</span></span>|<span data-ttu-id="04fe5-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="04fe5-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="04fe5-125">Accept</span><span class="sxs-lookup"><span data-stu-id="04fe5-125">Accept</span></span>|<span data-ttu-id="04fe5-126">application/json</span><span class="sxs-lookup"><span data-stu-id="04fe5-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="04fe5-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="04fe5-127">Request body</span></span>
<span data-ttu-id="04fe5-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto managedEBookCategory.</span><span class="sxs-lookup"><span data-stu-id="04fe5-128">In the request body, supply a JSON representation for the managedEBookCategory object.</span></span>

<span data-ttu-id="04fe5-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el managedEBookCategory.</span><span class="sxs-lookup"><span data-stu-id="04fe5-129">The following table shows the properties that are required when you create the managedEBookCategory.</span></span>

|<span data-ttu-id="04fe5-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="04fe5-130">Property</span></span>|<span data-ttu-id="04fe5-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="04fe5-131">Type</span></span>|<span data-ttu-id="04fe5-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="04fe5-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="04fe5-133">id</span><span class="sxs-lookup"><span data-stu-id="04fe5-133">id</span></span>|<span data-ttu-id="04fe5-134">String</span><span class="sxs-lookup"><span data-stu-id="04fe5-134">String</span></span>|<span data-ttu-id="04fe5-135">La clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="04fe5-135">The key of the entity.</span></span>|
|<span data-ttu-id="04fe5-136">displayName</span><span class="sxs-lookup"><span data-stu-id="04fe5-136">displayName</span></span>|<span data-ttu-id="04fe5-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="04fe5-137">String</span></span>|<span data-ttu-id="04fe5-138">El nombre de la categoría del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="04fe5-138">The name of the eBook category.</span></span>|
|<span data-ttu-id="04fe5-139">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="04fe5-139">lastModifiedDateTime</span></span>|<span data-ttu-id="04fe5-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="04fe5-140">DateTimeOffset</span></span>|<span data-ttu-id="04fe5-141">La fecha y hora que se modificó por última vez el ManagedEBookCategory.</span><span class="sxs-lookup"><span data-stu-id="04fe5-141">The date and time the ManagedEBookCategory was last modified.</span></span>|



## <a name="response"></a><span data-ttu-id="04fe5-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="04fe5-142">Response</span></span>
<span data-ttu-id="04fe5-143">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [managedEBookCategory](../resources/intune-books-managedebookcategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="04fe5-143">If successful, this method returns a `201 Created` response code and a [managedEBookCategory](../resources/intune-books-managedebookcategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="04fe5-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="04fe5-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="04fe5-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="04fe5-145">Request</span></span>
<span data-ttu-id="04fe5-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="04fe5-146">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/managedEBookCategories
Content-type: application/json
Content-length: 166

{
  "@odata.type": "#microsoft.graph.managedEBookCategory",
  "displayName": "Display Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```

### <a name="response"></a><span data-ttu-id="04fe5-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="04fe5-147">Response</span></span>
<span data-ttu-id="04fe5-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="04fe5-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 215

{
  "@odata.type": "#microsoft.graph.managedEBookCategory",
  "id": "3c71fb14-fb14-3c71-14fb-713c14fb713c",
  "displayName": "Display Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```





