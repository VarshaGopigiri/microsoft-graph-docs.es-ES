---
title: Aplicar accessReview
description: 'En Azure AD tener acceso a la característica de revisiones, se aplican las decisiones de un accessReview completado.  El objeto de destino puede ser una revisión de acceso única o una instancia de una revisión periódica de access.  '
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: e230a9638e865fbca69448f3a7683b95db954598
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27951337"
---
# <a name="apply-accessreview"></a><span data-ttu-id="45fbe-104">Aplicar accessReview</span><span class="sxs-lookup"><span data-stu-id="45fbe-104">Apply accessReview</span></span>

> <span data-ttu-id="45fbe-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="45fbe-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="45fbe-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="45fbe-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="45fbe-107">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, se aplican las decisiones de un completado [accessReview](../resources/accessreview.md).</span><span class="sxs-lookup"><span data-stu-id="45fbe-107">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, apply the decisions of a completed [accessReview](../resources/accessreview.md).</span></span>  <span data-ttu-id="45fbe-108">El objeto de destino puede ser una revisión de acceso única o una instancia de una revisión periódica de access.</span><span class="sxs-lookup"><span data-stu-id="45fbe-108">The target object can be either a one-time access review, or an instance of a recurring access review.</span></span>  


<span data-ttu-id="45fbe-109">Una vez finalizada una revisión de access, ya sea porque alcanza la fecha de finalización o un administrador detuvo manualmente y aplicar automáticamente no se ha configurado para la revisión, puede llamar a aplicar para aplicar los cambios.</span><span class="sxs-lookup"><span data-stu-id="45fbe-109">After an access review is finished, either because it reached the end date or an administrator stopped it manually, and auto-apply wasn't configured for the review, you can call Apply to apply the changes.</span></span> <span data-ttu-id="45fbe-110">Hasta que se produzca aplicar, las decisiones para quitar los derechos de acceso no aparecen en el recurso de origen, por ejemplo, los usuarios conservan sus pertenencias a grupos.</span><span class="sxs-lookup"><span data-stu-id="45fbe-110">Until apply occurs, the decisions to remove access rights do not appear on the source resource, the users for instance retain their group memberships.</span></span> <span data-ttu-id="45fbe-111">Al llamar a aplicar, el resultado de la revisión se implementa mediante la actualización de la aplicación o el grupo.</span><span class="sxs-lookup"><span data-stu-id="45fbe-111">By calling apply, the outcome of the review is implemented by updating the group or application.</span></span> <span data-ttu-id="45fbe-112">Si se denegó el acceso de un usuario en la revisión, cuando un administrador llama a esta API, Azure AD quita su asignación pertenencia o aplicación.</span><span class="sxs-lookup"><span data-stu-id="45fbe-112">If a user's access was denied in the review, when an administrator calls this API, Azure AD removes their membership or application assignment.</span></span> 

<span data-ttu-id="45fbe-113">Después de una revisión de access haya terminado y aplicar automáticamente se configuran, a continuación, el estado de la revisión cambiará de completado a través de los estados intermedios y por último cambiará a estado se aplica.</span><span class="sxs-lookup"><span data-stu-id="45fbe-113">After an access review is finished, and auto-apply was configured, then the status of the review will change from Completed through intermediate states and finally will change to state Applied.</span></span> <span data-ttu-id="45fbe-114">Puede esperar ver los usuarios denegados, si alguna, eliminando desde el recurso de grupo integrantes o la aplicación de asignación en unos minutos.</span><span class="sxs-lookup"><span data-stu-id="45fbe-114">You should expect to see denied users, if any, being removed from the resource group membership or app assignment in a few minutes.</span></span>

<span data-ttu-id="45fbe-115">Un automático configurado aplicar la revisión, o si selecciona aplicar no tiene un efecto en un grupo que se origina en un directorio local o un grupo dinámico.</span><span class="sxs-lookup"><span data-stu-id="45fbe-115">A configured auto applying review, or selecting Apply doesn't have an effect on a group that originates in an on-premises directory or a dynamic group.</span></span> <span data-ttu-id="45fbe-116">Si desea cambiar un grupo que se origina local, descargue los resultados y aplicar esos cambios a la representación del grupo en ese directorio.</span><span class="sxs-lookup"><span data-stu-id="45fbe-116">If you want to change a group that originates on-premises, download the results and apply those changes to the representation of the group in that directory.</span></span>


## <a name="permissions"></a><span data-ttu-id="45fbe-117">Permisos</span><span class="sxs-lookup"><span data-stu-id="45fbe-117">Permissions</span></span>
<span data-ttu-id="45fbe-p107">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="45fbe-p107">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="45fbe-120">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="45fbe-120">Permission type</span></span>                        | <span data-ttu-id="45fbe-121">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="45fbe-121">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="45fbe-122">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="45fbe-122">Delegated (work or school account)</span></span>     | <span data-ttu-id="45fbe-123">AccessReview.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="45fbe-123">AccessReview.ReadWrite.All</span></span> |
|<span data-ttu-id="45fbe-124">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="45fbe-124">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="45fbe-125">No admitida.</span><span class="sxs-lookup"><span data-stu-id="45fbe-125">Not supported.</span></span> |
|<span data-ttu-id="45fbe-126">Aplicación</span><span class="sxs-lookup"><span data-stu-id="45fbe-126">Application</span></span>                            | <span data-ttu-id="45fbe-127">No admitida.</span><span class="sxs-lookup"><span data-stu-id="45fbe-127">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="45fbe-128">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="45fbe-128">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /accessReviews('<id>')/applyDecisions()
```
## <a name="request-headers"></a><span data-ttu-id="45fbe-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="45fbe-129">Request headers</span></span>
| <span data-ttu-id="45fbe-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="45fbe-130">Name</span></span>         | <span data-ttu-id="45fbe-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="45fbe-131">Type</span></span>        | <span data-ttu-id="45fbe-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="45fbe-132">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="45fbe-133">Autorización</span><span class="sxs-lookup"><span data-stu-id="45fbe-133">Authorization</span></span> | <span data-ttu-id="45fbe-134">string</span><span class="sxs-lookup"><span data-stu-id="45fbe-134">string</span></span> | <span data-ttu-id="45fbe-135">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="45fbe-135">Bearer \{token\}.</span></span> <span data-ttu-id="45fbe-136">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="45fbe-136">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="45fbe-137">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="45fbe-137">Request body</span></span>
<span data-ttu-id="45fbe-138">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="45fbe-138">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="45fbe-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="45fbe-139">Response</span></span>
<span data-ttu-id="45fbe-p109">Si se ejecuta correctamente, este método devuelve un código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="45fbe-p109">If successful, this method returns a `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="see-also"></a><span data-ttu-id="45fbe-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="45fbe-142">See also</span></span>

- [<span data-ttu-id="45fbe-143">Procedimiento para llevar a cabo una revisión de access</span><span class="sxs-lookup"><span data-stu-id="45fbe-143">How to complete an access review</span></span>](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-azure-ad-controls-complete-access-review)

## <a name="example"></a><span data-ttu-id="45fbe-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="45fbe-144">Example</span></span>
##### <a name="request"></a><span data-ttu-id="45fbe-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="45fbe-145">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "apply_accessReview"
}-->
```http
POST https://graph.microsoft.com/beta/accessReviews('2975E9B5-44CE-4E71-93D3-30F03B5AA992')/applyDecisions()
```
##### <a name="response"></a><span data-ttu-id="45fbe-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="45fbe-146">Response</span></span>
><span data-ttu-id="45fbe-p110">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="45fbe-p110">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-25 00:00:01 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Apply accessReview",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
