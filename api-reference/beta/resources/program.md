---
title: tipo de recurso de programa
description: 'En el anuncio de Azure access revisa la característica, un programa es un contenedor, manteniendo los controles de programa. Un inquilino puede tener uno o varios programas.  Cada control vincula una revisión de acceso a un programa, para que sea más fácil buscar relacionado acceso revisa.  '
ms.openlocfilehash: cb08d0edb7487be95e159ed5e2a2546a92e7bce7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090333"
---
# <a name="program-resource-type"></a><span data-ttu-id="e7243-105">tipo de recurso de programa</span><span class="sxs-lookup"><span data-stu-id="e7243-105">program resource type</span></span>

> <span data-ttu-id="e7243-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e7243-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e7243-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e7243-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e7243-108">En la característica de [acceso revisa](accessreviews-root.md) Azure AD, un programa es un contenedor, manteniendo los controles de programa.</span><span class="sxs-lookup"><span data-stu-id="e7243-108">In the Azure AD [access reviews](accessreviews-root.md) feature, a program is a container, holding program controls.</span></span> <span data-ttu-id="e7243-109">Un inquilino puede tener uno o varios programas.</span><span class="sxs-lookup"><span data-stu-id="e7243-109">A tenant can have one or more programs.</span></span>  <span data-ttu-id="e7243-110">Cada control vincula una revisión de acceso a un programa, para que sea más fácil buscar relacionado acceso revisa.</span><span class="sxs-lookup"><span data-stu-id="e7243-110">Each control links an access review to a program, to make it easier to locate related access reviews.</span></span>  

<span data-ttu-id="e7243-111">Cada inquilino que ha en-efectuar Azure AD revisiones de acceso tiene uno de los programas, `Default program`.</span><span class="sxs-lookup"><span data-stu-id="e7243-111">Each tenant that has on-boarded Azure AD access reviews has one program, `Default program`.</span></span>  <span data-ttu-id="e7243-112">Un administrador global puede crear programas adicionales, por ejemplo, para representar las iniciativas de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="e7243-112">A global administrator can create additional programs, for example to represent compliance initiatives.</span></span> 


## <a name="methods"></a><span data-ttu-id="e7243-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="e7243-113">Methods</span></span>

| <span data-ttu-id="e7243-114">Método</span><span class="sxs-lookup"><span data-stu-id="e7243-114">Method</span></span>           | <span data-ttu-id="e7243-115">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7243-115">Return Type</span></span>    |<span data-ttu-id="e7243-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7243-116">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e7243-117">Creación de programa</span><span class="sxs-lookup"><span data-stu-id="e7243-117">Create program</span></span>](../api/program-create.md) |   [<span data-ttu-id="e7243-118">programa</span><span class="sxs-lookup"><span data-stu-id="e7243-118">program</span></span>](program.md)   |   <span data-ttu-id="e7243-119">Crear un nuevo programa.</span><span class="sxs-lookup"><span data-stu-id="e7243-119">Create a new program.</span></span>|
|[<span data-ttu-id="e7243-120">Eliminar programa</span><span class="sxs-lookup"><span data-stu-id="e7243-120">Delete program</span></span>](../api/program-delete.md) |   <span data-ttu-id="e7243-121">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e7243-121">None.</span></span>   |   <span data-ttu-id="e7243-122">Eliminar un programa.</span><span class="sxs-lookup"><span data-stu-id="e7243-122">Delete a program.</span></span>|
|[<span data-ttu-id="e7243-123">Programas de lista</span><span class="sxs-lookup"><span data-stu-id="e7243-123">List programs</span></span>](../api/program-list.md) |  <span data-ttu-id="e7243-124">colección de [programa](program.md)</span><span class="sxs-lookup"><span data-stu-id="e7243-124">[program](program.md) collection</span></span>|   <span data-ttu-id="e7243-125">Obtener una colección de todos los programas.</span><span class="sxs-lookup"><span data-stu-id="e7243-125">Get a collection of all the programs.</span></span>|
|[<span data-ttu-id="e7243-126">ProgramControls de lista de un programa</span><span class="sxs-lookup"><span data-stu-id="e7243-126">List programControls of a program</span></span>](../api/program-listcontrols.md) |      <span data-ttu-id="e7243-127">colección de [programControl](programcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="e7243-127">[programControl](programcontrol.md) collection</span></span>| <span data-ttu-id="e7243-128">Obtener una colección de los controles de un programa.</span><span class="sxs-lookup"><span data-stu-id="e7243-128">Get a collection of the controls of a program.</span></span>|
|[<span data-ttu-id="e7243-129">Programa de actualización</span><span class="sxs-lookup"><span data-stu-id="e7243-129">Update program</span></span>](../api/program-update.md) |   [<span data-ttu-id="e7243-130">programa</span><span class="sxs-lookup"><span data-stu-id="e7243-130">program</span></span>](program.md)|  <span data-ttu-id="e7243-131">Actualizar un programa.</span><span class="sxs-lookup"><span data-stu-id="e7243-131">Update a program.</span></span>|

## <a name="permissions"></a><span data-ttu-id="e7243-132">Permissions</span><span class="sxs-lookup"><span data-stu-id="e7243-132">Permissions</span></span>

|<span data-ttu-id="e7243-133">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e7243-133">Permission type</span></span>                        | <span data-ttu-id="e7243-134">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e7243-134">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="e7243-135">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e7243-135">Delegated (work or school account)</span></span>     | <span data-ttu-id="e7243-136">ProgramControl.Read.All, ProgramControl.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e7243-136">ProgramControl.Read.All, ProgramControl.ReadWrite.All</span></span> |
|<span data-ttu-id="e7243-137">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e7243-137">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e7243-138">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e7243-138">Not supported.</span></span> |
|<span data-ttu-id="e7243-139">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e7243-139">Application</span></span>                            | <span data-ttu-id="e7243-140">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e7243-140">Not supported.</span></span> |


## <a name="properties"></a><span data-ttu-id="e7243-141">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e7243-141">Properties</span></span>
| <span data-ttu-id="e7243-142">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e7243-142">Property</span></span>     | <span data-ttu-id="e7243-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7243-143">Type</span></span>   |<span data-ttu-id="e7243-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7243-144">Description</span></span>|
|:---------------|:--------|:----------|
| `id`                        |`String`                              |  <span data-ttu-id="e7243-145">El identificador asignado a la característica del programa.</span><span class="sxs-lookup"><span data-stu-id="e7243-145">The feature-assigned identifier of the program.</span></span>                    |
| `displayName`               |`String`                              |  <span data-ttu-id="e7243-146">El nombre del programa.</span><span class="sxs-lookup"><span data-stu-id="e7243-146">The name of the program.</span></span>  <span data-ttu-id="e7243-147">Necesarios en crear.</span><span class="sxs-lookup"><span data-stu-id="e7243-147">Required on create.</span></span>                  |
| `description`               |`String`                              |  <span data-ttu-id="e7243-148">La descripción del programa.</span><span class="sxs-lookup"><span data-stu-id="e7243-148">The description of the program.</span></span>           |

## <a name="relationships"></a><span data-ttu-id="e7243-149">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e7243-149">Relationships</span></span>
| <span data-ttu-id="e7243-150">Relación</span><span class="sxs-lookup"><span data-stu-id="e7243-150">Relationship</span></span> | <span data-ttu-id="e7243-151">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7243-151">Type</span></span>   |<span data-ttu-id="e7243-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7243-152">Description</span></span>|
|:---------------|:--------|:----------|
| `controls`                  |[<span data-ttu-id="e7243-153">programControl</span><span class="sxs-lookup"><span data-stu-id="e7243-153">programControl</span></span>](programcontrol.md) | <span data-ttu-id="e7243-154">Controles asociados con el programa.</span><span class="sxs-lookup"><span data-stu-id="e7243-154">Controls associated with the program.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="e7243-155">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e7243-155">JSON representation</span></span>

<span data-ttu-id="e7243-156">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e7243-156">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.program"
}-->

```json
{
 "id": "string (identifier)",
 "displayName": "string",
 "description": "string"
}

```

<!-- {
  "type": "#page.annotation",
  "description": "program resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->