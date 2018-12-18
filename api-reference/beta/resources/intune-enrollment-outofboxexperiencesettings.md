---
title: tipo de recurso outOfBoxExperienceSettings
description: Fuera de la experiencia del cuadro Configuración
author: tfitzmac
ms.openlocfilehash: 545fbe5c27063397a4d08c40729227804ebfc56d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27308410"
---
# <a name="outofboxexperiencesettings-resource-type"></a><span data-ttu-id="8fee5-103">tipo de recurso outOfBoxExperienceSettings</span><span class="sxs-lookup"><span data-stu-id="8fee5-103">outOfBoxExperienceSettings resource type</span></span>

> <span data-ttu-id="8fee5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8fee5-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8fee5-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8fee5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8fee5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8fee5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8fee5-107">Fuera de la experiencia del cuadro Configuración</span><span class="sxs-lookup"><span data-stu-id="8fee5-107">Out of box experience setting</span></span>
## <a name="properties"></a><span data-ttu-id="8fee5-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8fee5-108">Properties</span></span>
|<span data-ttu-id="8fee5-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8fee5-109">Property</span></span>|<span data-ttu-id="8fee5-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="8fee5-110">Type</span></span>|<span data-ttu-id="8fee5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fee5-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8fee5-112">hidePrivacySettings</span><span class="sxs-lookup"><span data-stu-id="8fee5-112">hidePrivacySettings</span></span>|<span data-ttu-id="8fee5-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="8fee5-113">Boolean</span></span>|<span data-ttu-id="8fee5-114">Mostrar u ocultar opciones de privacidad para los usuarios</span><span class="sxs-lookup"><span data-stu-id="8fee5-114">Show or hide privacy settings to user</span></span>|
|<span data-ttu-id="8fee5-115">hideEULA</span><span class="sxs-lookup"><span data-stu-id="8fee5-115">hideEULA</span></span>|<span data-ttu-id="8fee5-116">Boolean</span><span class="sxs-lookup"><span data-stu-id="8fee5-116">Boolean</span></span>|<span data-ttu-id="8fee5-117">Mostrar u ocultar los términos de licencia para el usuario</span><span class="sxs-lookup"><span data-stu-id="8fee5-117">Show or hide EULA to user</span></span>|
|<span data-ttu-id="8fee5-118">userType</span><span class="sxs-lookup"><span data-stu-id="8fee5-118">userType</span></span>|[<span data-ttu-id="8fee5-119">windowsUserType</span><span class="sxs-lookup"><span data-stu-id="8fee5-119">windowsUserType</span></span>](../resources/intune-enrollment-windowsusertype.md)|<span data-ttu-id="8fee5-120">Tipo de usuario.</span><span class="sxs-lookup"><span data-stu-id="8fee5-120">Type of user.</span></span> <span data-ttu-id="8fee5-121">Los valores posibles son: `administrator` y `standard`.</span><span class="sxs-lookup"><span data-stu-id="8fee5-121">Possible values are: `administrator`, `standard`.</span></span>|
|<span data-ttu-id="8fee5-122">deviceUsageType</span><span class="sxs-lookup"><span data-stu-id="8fee5-122">deviceUsageType</span></span>|[<span data-ttu-id="8fee5-123">windowsDeviceUsageType</span><span class="sxs-lookup"><span data-stu-id="8fee5-123">windowsDeviceUsageType</span></span>](../resources/intune-enrollment-windowsdeviceusagetype.md)|<span data-ttu-id="8fee5-124">Tipo de autenticación de combinación AAD.</span><span class="sxs-lookup"><span data-stu-id="8fee5-124">AAD join authentication type.</span></span> <span data-ttu-id="8fee5-125">Los valores posibles son: `singleUser` y `shared`.</span><span class="sxs-lookup"><span data-stu-id="8fee5-125">Possible values are: `singleUser`, `shared`.</span></span>|
|<span data-ttu-id="8fee5-126">skipKeyboardSelectionPage</span><span class="sxs-lookup"><span data-stu-id="8fee5-126">skipKeyboardSelectionPage</span></span>|<span data-ttu-id="8fee5-127">Boolean</span><span class="sxs-lookup"><span data-stu-id="8fee5-127">Boolean</span></span>|<span data-ttu-id="8fee5-128">Si el conjunto y, a continuación, omitir la selección de teclado página si se establecen el idioma y región</span><span class="sxs-lookup"><span data-stu-id="8fee5-128">If set, then skip the keyboard selection page if Language and Region are set</span></span>|
|<span data-ttu-id="8fee5-129">hideEscapeLink</span><span class="sxs-lookup"><span data-stu-id="8fee5-129">hideEscapeLink</span></span>|<span data-ttu-id="8fee5-130">Boolean</span><span class="sxs-lookup"><span data-stu-id="8fee5-130">Boolean</span></span>|<span data-ttu-id="8fee5-131">Si se establece en true, a continuación, el usuario no se puede iniciar a través de con una cuenta diferente, en el inicio de sesión de compañía</span><span class="sxs-lookup"><span data-stu-id="8fee5-131">If set to true, then the user can't start over with different account, on company sign-in</span></span>|

## <a name="relationships"></a><span data-ttu-id="8fee5-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8fee5-132">Relationships</span></span>
<span data-ttu-id="8fee5-133">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8fee5-133">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8fee5-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8fee5-134">JSON Representation</span></span>
<span data-ttu-id="8fee5-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8fee5-135">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.outOfBoxExperienceSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.outOfBoxExperienceSettings",
  "hidePrivacySettings": true,
  "hideEULA": true,
  "userType": "String",
  "deviceUsageType": "String",
  "skipKeyboardSelectionPage": true,
  "hideEscapeLink": true
}
```





