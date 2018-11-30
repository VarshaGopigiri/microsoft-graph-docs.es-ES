---
title: tipo de recurso programControlType
description: 'En el anuncio de Azure access revisa la característica, el tipo de control de programa se utiliza cuando el control se asocia un control a un programa, para indicar el tipo de revisión de access es para.  '
ms.openlocfilehash: 8fc406648d8f8c943920507a5734f47d2add1b4c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087124"
---
# <a name="programcontroltype-resource-type"></a><span data-ttu-id="9aaa8-103">tipo de recurso programControlType</span><span class="sxs-lookup"><span data-stu-id="9aaa8-103">programControlType resource type</span></span>

> <span data-ttu-id="9aaa8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9aaa8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9aaa8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9aaa8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9aaa8-106">En la característica de [acceso revisa](accessreviews-root.md) Azure AD, el tipo de control de programa se usa al asociar un control a un programa, para indicar el tipo de revisión de acceso para que es el control.</span><span class="sxs-lookup"><span data-stu-id="9aaa8-106">In the Azure AD [access reviews](accessreviews-root.md) feature, the program control type is used when associating a control to a program, to indicate the type of access review the control is for.</span></span>  

<span data-ttu-id="9aaa8-107">Los objetos de tipo de control de programa se generan automáticamente cuando el onboards el inquilino de para usar el acceso de administrador global revisa la característica.</span><span class="sxs-lookup"><span data-stu-id="9aaa8-107">The program control type objects are automatically generated when the global administrator onboards the tenant to use the access reviews feature.</span></span>  <span data-ttu-id="9aaa8-108">No se puede crear ningún tipo de control de programa adicionales.</span><span class="sxs-lookup"><span data-stu-id="9aaa8-108">No additional program control types can be created.</span></span>


## <a name="methods"></a><span data-ttu-id="9aaa8-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="9aaa8-109">Methods</span></span>

| <span data-ttu-id="9aaa8-110">Método</span><span class="sxs-lookup"><span data-stu-id="9aaa8-110">Method</span></span>           | <span data-ttu-id="9aaa8-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9aaa8-111">Return Type</span></span>    |<span data-ttu-id="9aaa8-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="9aaa8-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="9aaa8-113">Lista programControlTypes</span><span class="sxs-lookup"><span data-stu-id="9aaa8-113">List programControlTypes</span></span>](../api/programcontroltype-list.md) | <span data-ttu-id="9aaa8-114">colección de [programControlType](programcontroltype.md)</span><span class="sxs-lookup"><span data-stu-id="9aaa8-114">[programControlType](programcontroltype.md) collection</span></span>| <span data-ttu-id="9aaa8-115">Lista de tipos de control de programa.</span><span class="sxs-lookup"><span data-stu-id="9aaa8-115">List program control types.</span></span> |

## <a name="properties"></a><span data-ttu-id="9aaa8-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9aaa8-116">Properties</span></span>
| <span data-ttu-id="9aaa8-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9aaa8-117">Property</span></span>     | <span data-ttu-id="9aaa8-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="9aaa8-118">Type</span></span>   |<span data-ttu-id="9aaa8-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="9aaa8-119">Description</span></span>|
|:---------------|:--------|:----------|
| `id`                     |`String`                | <span data-ttu-id="9aaa8-120">El identificador asignado a la función del tipo de control de programa</span><span class="sxs-lookup"><span data-stu-id="9aaa8-120">The feature-assigned identifier of the program control type</span></span>                                      |
| `displayName`            |`String`                | <span data-ttu-id="9aaa8-121">El nombre del tipo de control de programa</span><span class="sxs-lookup"><span data-stu-id="9aaa8-121">The name of the program control type</span></span>                                                             |


## <a name="relationships"></a><span data-ttu-id="9aaa8-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9aaa8-122">Relationships</span></span>

<span data-ttu-id="9aaa8-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9aaa8-123">None.</span></span>


## <a name="see-also"></a><span data-ttu-id="9aaa8-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="9aaa8-124">See also</span></span>

| <span data-ttu-id="9aaa8-125">Método</span><span class="sxs-lookup"><span data-stu-id="9aaa8-125">Method</span></span>           | <span data-ttu-id="9aaa8-126">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9aaa8-126">Return Type</span></span>    |<span data-ttu-id="9aaa8-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="9aaa8-127">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="9aaa8-128">Crear programControl</span><span class="sxs-lookup"><span data-stu-id="9aaa8-128">Create programControl</span></span>](../api/programcontrol-create.md) |     [<span data-ttu-id="9aaa8-129">programControl</span><span class="sxs-lookup"><span data-stu-id="9aaa8-129">programControl</span></span>](programcontrol.md) |   <span data-ttu-id="9aaa8-130">Agregar un programControl a un programa.</span><span class="sxs-lookup"><span data-stu-id="9aaa8-130">Add a programControl to a program.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="9aaa8-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9aaa8-131">JSON representation</span></span>

<span data-ttu-id="9aaa8-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9aaa8-132">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.programControlType"
}-->

```json
{
 "id": "string (identifier)",
 "displayName": "string"
}

```

<!-- {
  "type": "#page.annotation",
  "description": "programControlType resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
