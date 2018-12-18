---
title: tipo de enumeración secureAssessmentAccountType
description: Tipo de cuentas que se permiten en Windows10SecureAssessment ConfigurationAccount.
author: tfitzmac
ms.openlocfilehash: faf504410336bdc491c29b676aaa1b57cd0a5ee2
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27362226"
---
# <a name="secureassessmentaccounttype-enum-type"></a><span data-ttu-id="66954-103">tipo de enumeración secureAssessmentAccountType</span><span class="sxs-lookup"><span data-stu-id="66954-103">secureAssessmentAccountType enum type</span></span>

> <span data-ttu-id="66954-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="66954-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="66954-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="66954-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="66954-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="66954-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="66954-107">Tipo de cuentas que se permiten en Windows10SecureAssessment ConfigurationAccount.</span><span class="sxs-lookup"><span data-stu-id="66954-107">Type of accounts that are allowed for Windows10SecureAssessment ConfigurationAccount.</span></span>
## <a name="members"></a><span data-ttu-id="66954-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="66954-108">Members</span></span>
|<span data-ttu-id="66954-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="66954-109">Member</span></span>|<span data-ttu-id="66954-110">Valor</span><span class="sxs-lookup"><span data-stu-id="66954-110">Value</span></span>|<span data-ttu-id="66954-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="66954-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="66954-112">azureADAccount</span><span class="sxs-lookup"><span data-stu-id="66954-112">azureADAccount</span></span>|<span data-ttu-id="66954-113">0</span><span class="sxs-lookup"><span data-stu-id="66954-113">0</span></span>|<span data-ttu-id="66954-114">Indica una cuenta de Azure AD en formato de AzureAD\ username@tenant.com.</span><span class="sxs-lookup"><span data-stu-id="66954-114">Indicates an Azure AD account in format of AzureAD\username@tenant.com.</span></span>|
|<span data-ttu-id="66954-115">domainAccount</span><span class="sxs-lookup"><span data-stu-id="66954-115">domainAccount</span></span>|<span data-ttu-id="66954-116">1</span><span class="sxs-lookup"><span data-stu-id="66954-116">1</span></span>|<span data-ttu-id="66954-117">Indica una cuenta de dominio en el formato de dominio\usuario o user@domain.com.</span><span class="sxs-lookup"><span data-stu-id="66954-117">Indicates a domain account in format of domain\user or user@domain.com.</span></span>|
|<span data-ttu-id="66954-118">localAccount</span><span class="sxs-lookup"><span data-stu-id="66954-118">localAccount</span></span>|<span data-ttu-id="66954-119">2</span><span class="sxs-lookup"><span data-stu-id="66954-119">2</span></span>|<span data-ttu-id="66954-120">Indica una cuenta local en formato de nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="66954-120">Indicates a local account in format of username.</span></span>|





