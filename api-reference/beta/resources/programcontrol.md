---
title: tipo de recurso programControl
description: En el anuncio de Azure access revisa la característica, el objeto de control de programa representa un control, vincular una revisión de acceso a un programa.
ms.openlocfilehash: 03e70ffdf0607eeb11abaf1b12065b4092294d23
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086150"
---
# <a name="programcontrol-resource-type"></a><span data-ttu-id="a7439-103">tipo de recurso programControl</span><span class="sxs-lookup"><span data-stu-id="a7439-103">programControl resource type</span></span>

> <span data-ttu-id="a7439-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a7439-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a7439-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a7439-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a7439-106">En la característica de [acceso revisa](accessreviews-root.md) Azure AD, el objeto de control de programa representa un control, vincular una revisión de acceso a un programa.</span><span class="sxs-lookup"><span data-stu-id="a7439-106">In the Azure AD [access reviews](accessreviews-root.md) feature, the program control object represents a control, linking an access review to a program.</span></span>


## <a name="methods"></a><span data-ttu-id="a7439-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="a7439-107">Methods</span></span>

| <span data-ttu-id="a7439-108">Método</span><span class="sxs-lookup"><span data-stu-id="a7439-108">Method</span></span>           | <span data-ttu-id="a7439-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7439-109">Return Type</span></span>    |<span data-ttu-id="a7439-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7439-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="a7439-111">Crear programControl</span><span class="sxs-lookup"><span data-stu-id="a7439-111">Create programControl</span></span>](../api/programcontrol-create.md) |     [<span data-ttu-id="a7439-112">programControl</span><span class="sxs-lookup"><span data-stu-id="a7439-112">programControl</span></span>](programcontrol.md) |   <span data-ttu-id="a7439-113">Agregar un programControl a un programa.</span><span class="sxs-lookup"><span data-stu-id="a7439-113">Add a programControl to a program.</span></span>|
|[<span data-ttu-id="a7439-114">Eliminar programControl</span><span class="sxs-lookup"><span data-stu-id="a7439-114">Delete programControl</span></span>](../api/programcontrol-delete.md) |     <span data-ttu-id="a7439-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a7439-115">None.</span></span>   |   <span data-ttu-id="a7439-116">Quitar un programControl de un programa.</span><span class="sxs-lookup"><span data-stu-id="a7439-116">Remove a programControl from a program.</span></span>|
|[<span data-ttu-id="a7439-117">Lista programControls</span><span class="sxs-lookup"><span data-stu-id="a7439-117">List programControls</span></span>](../api/programcontrol-list.md) | <span data-ttu-id="a7439-118">colección de [programControl](programcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="a7439-118">[programControl](programcontrol.md) collection</span></span>| <span data-ttu-id="a7439-119">Controles de lista a través de todos los programas en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="a7439-119">List controls across all programs in the tenant.</span></span>|

## <a name="permissions"></a><span data-ttu-id="a7439-120">Permissions</span><span class="sxs-lookup"><span data-stu-id="a7439-120">Permissions</span></span>

|<span data-ttu-id="a7439-121">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a7439-121">Permission type</span></span>                        | <span data-ttu-id="a7439-122">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a7439-122">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="a7439-123">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a7439-123">Delegated (work or school account)</span></span>     | <span data-ttu-id="a7439-124">ProgramControl.Read.All, ProgramControl.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a7439-124">ProgramControl.Read.All, ProgramControl.ReadWrite.All</span></span> |
|<span data-ttu-id="a7439-125">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a7439-125">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a7439-126">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a7439-126">Not supported.</span></span> |
|<span data-ttu-id="a7439-127">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a7439-127">Application</span></span>                            | <span data-ttu-id="a7439-128">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a7439-128">Not supported.</span></span> |

## <a name="properties"></a><span data-ttu-id="a7439-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a7439-129">Properties</span></span>
| <span data-ttu-id="a7439-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a7439-130">Property</span></span>     | <span data-ttu-id="a7439-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7439-131">Type</span></span>   |<span data-ttu-id="a7439-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7439-132">Description</span></span>|
|:---------------|:--------|:----------|
| `id`                     |`String`                | <span data-ttu-id="a7439-133">El identificador asignado a la característica del vínculo entre el programa y control</span><span class="sxs-lookup"><span data-stu-id="a7439-133">The feature-assigned identifier of the link between program and control</span></span>                                      |
| `programId`              |`String`                | <span data-ttu-id="a7439-134">El programId del programa de este control es una parte de.</span><span class="sxs-lookup"><span data-stu-id="a7439-134">The programId of the program this control is a part of.</span></span> <span data-ttu-id="a7439-135">Necesarios en crear.</span><span class="sxs-lookup"><span data-stu-id="a7439-135">Required on create.</span></span>                            |
| `controlId`              |`String`                | <span data-ttu-id="a7439-136">ControlId del control, en particular, el identificador de una revisión de access.</span><span class="sxs-lookup"><span data-stu-id="a7439-136">The controlId of the control, in particular the identifier of an access review.</span></span> <span data-ttu-id="a7439-137">Necesarios en crear.</span><span class="sxs-lookup"><span data-stu-id="a7439-137">Required on create.</span></span>                                                |
| `controlTypeId`          |`String`                | <span data-ttu-id="a7439-138">El programControlType identifica el tipo de control de programa: por ejemplo, se revisa un control de vinculación para acceso de invitado.</span><span class="sxs-lookup"><span data-stu-id="a7439-138">The programControlType identifies the type of program control - for example, a control linking to guest access reviews.</span></span> <span data-ttu-id="a7439-139">Necesarios en crear.</span><span class="sxs-lookup"><span data-stu-id="a7439-139">Required on create.</span></span> |
| `displayName`            |`String`                | <span data-ttu-id="a7439-140">El nombre del control.</span><span class="sxs-lookup"><span data-stu-id="a7439-140">The name of the control.</span></span>                                                             |
| `status`                 |`String`                | <span data-ttu-id="a7439-141">El estado de ciclo de vida del control.</span><span class="sxs-lookup"><span data-stu-id="a7439-141">The life cycle status of the control.</span></span>                                                 |
| `createdDateTime`        |`DateTimeOffset`        | <span data-ttu-id="a7439-142">La fecha de creación y la hora del control del programa.</span><span class="sxs-lookup"><span data-stu-id="a7439-142">The creation date and time of the program control.</span></span>                                        |
| `owner`                  |[<span data-ttu-id="a7439-143">IdentidadDeUsuario</span><span class="sxs-lookup"><span data-stu-id="a7439-143">userIdentity</span></span>](useridentity.md)   | <span data-ttu-id="a7439-144">El usuario que creó el control del programa.</span><span class="sxs-lookup"><span data-stu-id="a7439-144">The user who created the program control.</span></span>                                               |
| `resource`               |`programResource`       | <span data-ttu-id="a7439-145">El recurso, un grupo o una aplicación, el objetivo de la revisión de acceso del control de este programa.</span><span class="sxs-lookup"><span data-stu-id="a7439-145">The resource, a group or an app, targeted by this program control's access review.</span></span>                   |

## <a name="relationships"></a><span data-ttu-id="a7439-146">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a7439-146">Relationships</span></span>
| <span data-ttu-id="a7439-147">Relación</span><span class="sxs-lookup"><span data-stu-id="a7439-147">Relationship</span></span> | <span data-ttu-id="a7439-148">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7439-148">Type</span></span>   |<span data-ttu-id="a7439-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7439-149">Description</span></span>|
|:---------------|:--------|:----------|
| `program`                |[<span data-ttu-id="a7439-150">programa</span><span class="sxs-lookup"><span data-stu-id="a7439-150">program</span></span>](program.md)               | <span data-ttu-id="a7439-151">El programa de. que este control forma parte.</span><span class="sxs-lookup"><span data-stu-id="a7439-151">The program this control is part of.</span></span>                                                |

## <a name="see-also"></a><span data-ttu-id="a7439-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7439-152">See also</span></span>

| <span data-ttu-id="a7439-153">Método</span><span class="sxs-lookup"><span data-stu-id="a7439-153">Method</span></span>           | <span data-ttu-id="a7439-154">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7439-154">Return Type</span></span>    |<span data-ttu-id="a7439-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7439-155">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="a7439-156">ProgramControls de lista de un programa</span><span class="sxs-lookup"><span data-stu-id="a7439-156">List programControls of a program</span></span>](../api/program-listcontrols.md) |      <span data-ttu-id="a7439-157">colección de [programControl](programcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="a7439-157">[programControl](programcontrol.md) collection</span></span>| <span data-ttu-id="a7439-158">Obtener una colección de los controles de un programa.</span><span class="sxs-lookup"><span data-stu-id="a7439-158">Get a collection of the controls of a program.</span></span>|
|[<span data-ttu-id="a7439-159">Lista programControlTypes</span><span class="sxs-lookup"><span data-stu-id="a7439-159">List programControlTypes</span></span>](../api/programcontroltype-list.md) | <span data-ttu-id="a7439-160">colección de [programControlType](programcontroltype.md)</span><span class="sxs-lookup"><span data-stu-id="a7439-160">[programControlType](programcontroltype.md) collection</span></span>| <span data-ttu-id="a7439-161">Lista de tipos de control de programa.</span><span class="sxs-lookup"><span data-stu-id="a7439-161">List program control types.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="a7439-162">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a7439-162">JSON representation</span></span>

<span data-ttu-id="a7439-163">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a7439-163">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.programControl"
}-->

```json
{
 "id": "string (identifier)",
 "programId": "string (identifier)",
 "controlId": "string (identifier)",
 "controlTypeId": "string (identifier)",
 "displayName": "string",
 "status": "string",
 "createdDateTime": "string (timestamp)",
 "owner": "microsoft.graph.userIdentity",
 "resource":"microsoft.graph.programResource"
}

```

## <a name="the-programresource-complex-type"></a><span data-ttu-id="a7439-164">El tipo complejo programResource</span><span class="sxs-lookup"><span data-stu-id="a7439-164">The programResource complex type</span></span>

<span data-ttu-id="a7439-165">El recurso de programa, dentro de un objeto de control de programa, es una representación de una referencia a un objeto que es el destino de la revisión de access.</span><span class="sxs-lookup"><span data-stu-id="a7439-165">The program resource, contained within a program control object, is a representation of a reference to an object which is the target of the access review.</span></span>

<span data-ttu-id="a7439-166">Este tipo se hereda de `microsoft.graph.identity` y tiene una propiedad adicional:</span><span class="sxs-lookup"><span data-stu-id="a7439-166">This type inherits from `microsoft.graph.identity` and has one additional property:</span></span>

| <span data-ttu-id="a7439-167">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a7439-167">Property</span></span>     | <span data-ttu-id="a7439-168">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7439-168">Type</span></span>   |<span data-ttu-id="a7439-169">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7439-169">Description</span></span>|
|:---------------|:--------|:----------|
| `type`               |`String`  | <span data-ttu-id="a7439-170">Tipo del recurso, que indica si es un grupo o una aplicación.</span><span class="sxs-lookup"><span data-stu-id="a7439-170">Type of the resource, indicating whether it is a group or an app.</span></span> |     


<!-- {
  "type": "#page.annotation",
  "description": "programControl resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->