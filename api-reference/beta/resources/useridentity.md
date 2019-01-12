---
title: tipo de IdentidadDeUsuario
description: 'Para AD Azure access revisiones, este tipo representa una identidad de usuario de Azure AD para un revisor de una revisión de access.  '
localization_priority: Normal
author: dkershaw10
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 80e8cc68d4fc2f642be6c748b762fe47c7489d59
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932283"
---
# <a name="useridentity-type"></a><span data-ttu-id="82ac6-103">tipo de IdentidadDeUsuario</span><span class="sxs-lookup"><span data-stu-id="82ac6-103">userIdentity type</span></span>

> <span data-ttu-id="82ac6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="82ac6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="82ac6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="82ac6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="82ac6-106">Para el AD Azure [access revisa](accessreviews-root.md), este tipo representa una identidad de usuario de Azure AD para un revisor de una revisión de acceso.</span><span class="sxs-lookup"><span data-stu-id="82ac6-106">For the Azure AD [access reviews](accessreviews-root.md), this type represents an Azure AD user identity for a reviewer of an access review.</span></span>  
<span data-ttu-id="82ac6-107">En el contexto de un registro de auditoría de Azure AD, esto representa la información del usuario que inició o se ve afectada por una actividad de auditoría.</span><span class="sxs-lookup"><span data-stu-id="82ac6-107">In the context of an Azure AD audit log, this represents the user information that initiated or was affected by an audit activity.</span></span>

<span data-ttu-id="82ac6-108">Este tipo hereda de [identidad](identity.md) y tiene una propiedad adicional, el nombre principal de usuario del usuario.</span><span class="sxs-lookup"><span data-stu-id="82ac6-108">This type inherits from [identity](identity.md) and has one additional property, the user principal name of the user.</span></span>

## <a name="methods"></a><span data-ttu-id="82ac6-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="82ac6-109">Methods</span></span>

<span data-ttu-id="82ac6-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="82ac6-110">None.</span></span>  <span data-ttu-id="82ac6-111">Debe incluir los objetos de este tipo en el cuerpo de una solicitud al [crear un accessReview](../api/accessreview-create.md).</span><span class="sxs-lookup"><span data-stu-id="82ac6-111">You would include objects of this type in the body of a request when [creating an accessReview](../api/accessreview-create.md).</span></span>

## <a name="properties"></a><span data-ttu-id="82ac6-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="82ac6-112">Properties</span></span>
| <span data-ttu-id="82ac6-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="82ac6-113">Property</span></span>     | <span data-ttu-id="82ac6-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="82ac6-114">Type</span></span>   |<span data-ttu-id="82ac6-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="82ac6-115">Description</span></span>|
|:---------------|:--------|:----------|
| `displayName` | `String` | <span data-ttu-id="82ac6-116">Nombre para mostrar de la identidad.</span><span class="sxs-lookup"><span data-stu-id="82ac6-116">The identity's display name.</span></span> <span data-ttu-id="82ac6-117">Tenga en cuenta que esto es posible que no siempre esté disponible o actualizado.</span><span class="sxs-lookup"><span data-stu-id="82ac6-117">Note that this may not always be available or up-to-date.</span></span>    |
| `id`          | `String` | <span data-ttu-id="82ac6-118">Identificador único de la identidad.</span><span class="sxs-lookup"><span data-stu-id="82ac6-118">Unique identifier for the identity.</span></span>  |
| `ipAddress`| `String`| <span data-ttu-id="82ac6-119">Indica la dirección IP del cliente usada por el usuario que realiza la actividad (solo registro de auditoría).</span><span class="sxs-lookup"><span data-stu-id="82ac6-119">Indicates the client IP address used by user performing the activity (audit log only).</span></span>|
| `userPrincipalName`|`String` | <span data-ttu-id="82ac6-120">El atributo userPrincipalName del usuario.</span><span class="sxs-lookup"><span data-stu-id="82ac6-120">The userPrincipalName attribute of the user.</span></span> |

## <a name="remarks"></a><span data-ttu-id="82ac6-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="82ac6-121">Remarks</span></span>

<span data-ttu-id="82ac6-p104">En algunas circunstancias, puede que el identificador único del actor no esté disponible. En este caso, se devuelve la propiedad **displayName** de la identidad, pero faltará la propiedad **id** del recurso.</span><span class="sxs-lookup"><span data-stu-id="82ac6-p104">In some circumstances, the unique identifier for the actor may not be available. In this case, the **displayName** property for the identity will be returned, but the **id** property will be missing from the resource.</span></span>

## <a name="relationships"></a><span data-ttu-id="82ac6-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="82ac6-124">Relationships</span></span>

<span data-ttu-id="82ac6-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="82ac6-125">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="82ac6-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="82ac6-126">See also</span></span>

| <span data-ttu-id="82ac6-127">Método</span><span class="sxs-lookup"><span data-stu-id="82ac6-127">Method</span></span>           | <span data-ttu-id="82ac6-128">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82ac6-128">Return Type</span></span>    |<span data-ttu-id="82ac6-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="82ac6-129">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="82ac6-130">Obtener los revisores accessReview</span><span class="sxs-lookup"><span data-stu-id="82ac6-130">Get accessReview reviewers</span></span>](../api/accessreview-listreviewers.md) |       <span data-ttu-id="82ac6-131">colección de [IdentidadDeUsuario](useridentity.md)</span><span class="sxs-lookup"><span data-stu-id="82ac6-131">[userIdentity](useridentity.md) collection</span></span>| <span data-ttu-id="82ac6-132">Obtenga los revisores de un accessReview.</span><span class="sxs-lookup"><span data-stu-id="82ac6-132">Get the reviewers of an accessReview.</span></span> |
|[<span data-ttu-id="82ac6-133">Agregar revisor accessReview</span><span class="sxs-lookup"><span data-stu-id="82ac6-133">Add accessReview reviewer</span></span>](../api/accessreview-addreviewer.md) |      <span data-ttu-id="82ac6-134">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="82ac6-134">None.</span></span>   |   <span data-ttu-id="82ac6-135">Agregar un revisor a una accessReview.</span><span class="sxs-lookup"><span data-stu-id="82ac6-135">Add a reviewer to an accessReview.</span></span> |
|[<span data-ttu-id="82ac6-136">Quitar accessReview revisor</span><span class="sxs-lookup"><span data-stu-id="82ac6-136">Remove accessReview reviewer</span></span>](../api/accessreview-removereviewer.md) | <span data-ttu-id="82ac6-137">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="82ac6-137">None.</span></span>  |   <span data-ttu-id="82ac6-138">Quitar un revisor de un accessReview.</span><span class="sxs-lookup"><span data-stu-id="82ac6-138">Remove a reviewer from an accessReview.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="82ac6-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="82ac6-139">JSON representation</span></span>

<span data-ttu-id="82ac6-140">Aquí es una representación de JSON del tipo.</span><span class="sxs-lookup"><span data-stu-id="82ac6-140">Here is a JSON representation of the type.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
"displayName", "thumbnails"
  ],
  "@odata.type": "microsoft.graph.userIdentity"
}-->

```json
{
  "displayName": "string",
  "id": "string",
 "userPrincipalName": "String"
}

```

<!-- {
  "type": "#page.annotation",
  "description": "userIdentity type",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
