---
title: tipo de enumeración secureAssessmentAccountType
description: Tipo de cuentas que se permiten en Windows10SecureAssessment ConfigurationAccount.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 9e5ae78b5df3636e738cf21beece269e6fa7b81a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959261"
---
# <a name="secureassessmentaccounttype-enum-type"></a><span data-ttu-id="25983-103">tipo de enumeración secureAssessmentAccountType</span><span class="sxs-lookup"><span data-stu-id="25983-103">secureAssessmentAccountType enum type</span></span>

> <span data-ttu-id="25983-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="25983-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="25983-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="25983-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="25983-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="25983-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="25983-107">Tipo de cuentas que se permiten en Windows10SecureAssessment ConfigurationAccount.</span><span class="sxs-lookup"><span data-stu-id="25983-107">Type of accounts that are allowed for Windows10SecureAssessment ConfigurationAccount.</span></span>
## <a name="members"></a><span data-ttu-id="25983-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="25983-108">Members</span></span>
|<span data-ttu-id="25983-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="25983-109">Member</span></span>|<span data-ttu-id="25983-110">Valor</span><span class="sxs-lookup"><span data-stu-id="25983-110">Value</span></span>|<span data-ttu-id="25983-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="25983-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="25983-112">azureADAccount</span><span class="sxs-lookup"><span data-stu-id="25983-112">azureADAccount</span></span>|<span data-ttu-id="25983-113">0</span><span class="sxs-lookup"><span data-stu-id="25983-113">0</span></span>|<span data-ttu-id="25983-114">Indica una cuenta de Azure AD en formato de AzureAD\ username@tenant.com.</span><span class="sxs-lookup"><span data-stu-id="25983-114">Indicates an Azure AD account in format of AzureAD\username@tenant.com.</span></span>|
|<span data-ttu-id="25983-115">domainAccount</span><span class="sxs-lookup"><span data-stu-id="25983-115">domainAccount</span></span>|<span data-ttu-id="25983-116">1</span><span class="sxs-lookup"><span data-stu-id="25983-116">1</span></span>|<span data-ttu-id="25983-117">Indica una cuenta de dominio en el formato de dominio\usuario o user@domain.com.</span><span class="sxs-lookup"><span data-stu-id="25983-117">Indicates a domain account in format of domain\user or user@domain.com.</span></span>|
|<span data-ttu-id="25983-118">localAccount</span><span class="sxs-lookup"><span data-stu-id="25983-118">localAccount</span></span>|<span data-ttu-id="25983-119">2</span><span class="sxs-lookup"><span data-stu-id="25983-119">2</span></span>|<span data-ttu-id="25983-120">Indica una cuenta local en formato de nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="25983-120">Indicates a local account in format of username.</span></span>|





