---
title: tipo de enumeración binaryManagementConditionExpressionOperatorType
description: Operadores binarios compatibles para expresiones de condición de administración.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 141238fd90b6cae65ac50745d950d3d9d149280d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959415"
---
# <a name="binarymanagementconditionexpressionoperatortype-enum-type"></a><span data-ttu-id="37b39-103">tipo de enumeración binaryManagementConditionExpressionOperatorType</span><span class="sxs-lookup"><span data-stu-id="37b39-103">binaryManagementConditionExpressionOperatorType enum type</span></span>

> <span data-ttu-id="37b39-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="37b39-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="37b39-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="37b39-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="37b39-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="37b39-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="37b39-107">Operadores binarios compatibles para expresiones de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="37b39-107">Supported binary operators for management condition expressions.</span></span>
## <a name="members"></a><span data-ttu-id="37b39-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="37b39-108">Members</span></span>
|<span data-ttu-id="37b39-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="37b39-109">Member</span></span>|<span data-ttu-id="37b39-110">Valor</span><span class="sxs-lookup"><span data-stu-id="37b39-110">Value</span></span>|<span data-ttu-id="37b39-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="37b39-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="37b39-112">o</span><span class="sxs-lookup"><span data-stu-id="37b39-112">or</span></span>|<span data-ttu-id="37b39-113">0</span><span class="sxs-lookup"><span data-stu-id="37b39-113">0</span></span>|<span data-ttu-id="37b39-114">Se evalúa como un conjunto de operandos como true si y sólo si uno o varios de sus operandos están true.</span><span class="sxs-lookup"><span data-stu-id="37b39-114">Evaluates a set of operands as true if and only if one or more of its operands is true.</span></span>|
|<span data-ttu-id="37b39-115">y</span><span class="sxs-lookup"><span data-stu-id="37b39-115">and</span></span>|<span data-ttu-id="37b39-116">1</span><span class="sxs-lookup"><span data-stu-id="37b39-116">1</span></span>|<span data-ttu-id="37b39-117">Se evalúa como un conjunto de operandos como true sólo si todos sus operandos son true.</span><span class="sxs-lookup"><span data-stu-id="37b39-117">Evaluates a set of operands as true if and only if all of its operands are true.</span></span>|





