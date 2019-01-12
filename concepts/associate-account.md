---
title: Asociar la cuenta de Office 365 a Azure AD para crear y administrar aplicaciones
description: 'Para autenticar las aplicaciones mediante Microsoft Azure Active Directory (Azure AD), debe registrarlas en Azure AD. Aquí es donde se almacena la información de las aplicaciones y de la cuenta de usuario de Office 365. Para administrar Azure AD a través de Azure Portal, necesita una suscripción a Microsoft Azure. Puede usar el portal en Microsoft Azure para administrar usuarios, roles y aplicaciones. '
localization_priority: Normal
ms.openlocfilehash: 815cc80fa8d25f52ac05a1bf80f9e9dfa89b9b4d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27880160"
---
# <a name="associate-your-office-365-account-with-azure-ad-to-create-and-manage-apps"></a><span data-ttu-id="bc308-106">Asociar la cuenta de Office 365 a Azure AD para crear y administrar aplicaciones</span><span class="sxs-lookup"><span data-stu-id="bc308-106">Associate your Office 365 account with Azure AD to create and manage apps</span></span>

<span data-ttu-id="bc308-107">Para autenticar las aplicaciones mediante Microsoft Azure Active Directory (Azure AD), debe registrarlas en Azure AD.</span><span class="sxs-lookup"><span data-stu-id="bc308-107">To authenticate your applications using Microsoft Azure Active Directory (Azure AD), you need to register them in Azure AD.</span></span> <span data-ttu-id="bc308-108">Aquí es donde se almacena la información de las aplicaciones y de la cuenta de usuario de Office 365.</span><span class="sxs-lookup"><span data-stu-id="bc308-108">This is where Office 365 user account and application information is stored.</span></span> <span data-ttu-id="bc308-109">Para administrar Azure AD a través de Azure Portal, necesita una suscripción a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bc308-109">To manage Azure AD through the Azure portal, you need a Microsoft Azure subscription.</span></span> <span data-ttu-id="bc308-110">Puede usar el portal en Microsoft Azure para administrar usuarios, roles y aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="bc308-110">You can use the portal in Microsoft Azure to manage users, roles, and apps.</span></span> 

<span data-ttu-id="bc308-111">En este artículo se muestra cómo asociar la cuenta de Office 365 a Azure AD para crear y administrar aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="bc308-111">This article shows you how to associate your Office 365 account with Azure AD to create and manage apps.</span></span>

 ><span data-ttu-id="bc308-p103">**Nota:** En este artículo, se usa Azure AD como proveedor de autenticación de su aplicación. Si usa el punto de conexión v2.0 de Azure AD, no será necesario realizar este paso. Para obtener más información, consulte [Autenticación de aplicaciones con Microsoft Graph](auth-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bc308-p103">**Note:** This article uses Azure AD as the authentication provider for your app. If you're using the Azure AD v2.0 endpoint, you don't need to perform this step. For more information, see [App authentication with Microsoft Graph](auth-overview.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bc308-115">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bc308-115">Prerequisites</span></span>

<span data-ttu-id="bc308-116">**Cuenta de Office 365 para empresas**</span><span class="sxs-lookup"><span data-stu-id="bc308-116">**Office 365 for business account**</span></span>

<span data-ttu-id="bc308-117">Si no tiene una cuenta de Office 365 para empresas, realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="bc308-117">If you don't have an existing Office 365 for business account, you can:</span></span>

- <span data-ttu-id="bc308-118">Regístrese en uno de los [planes de Office 365 para empresas](https://products.office.com/es-ES/business/compare-office-365-for-business-plans) enumerados anteriormente, o</span><span class="sxs-lookup"><span data-stu-id="bc308-118">Sign up for an [Office 365 for business plans](https://products.office.com/es-ES/business/compare-office-365-for-business-plans) listed above, or</span></span>
- <span data-ttu-id="bc308-119">[Únase al programa Office 365 Developer y consiga una suscripción gratuita de 1 año a Office 365](https://aka.ms/devprogramsignup).</span><span class="sxs-lookup"><span data-stu-id="bc308-119">[Join the Office 365 Developer Program and get a free 1 year subscription to Office 365](https://aka.ms/devprogramsignup).</span></span>

<span data-ttu-id="bc308-120">**Suscripción a Microsoft Azure**</span><span class="sxs-lookup"><span data-stu-id="bc308-120">**Microsoft Azure subscription**</span></span> 

- <span data-ttu-id="bc308-121">Si tiene una suscripción de Microsoft Azure, puede asociarla con su suscripción de Office 365 para empresas.</span><span class="sxs-lookup"><span data-stu-id="bc308-121">If you can have an existing Microsoft Azure subscription, you can associate your Office 365 for business subscription with it.</span></span> 

- <span data-ttu-id="bc308-122">De lo contrario, deberá crear una suscripción de Azure y asociarla con la cuenta de Office 365 para así poder registrar y administrar aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="bc308-122">Otherwise, you'll need to create a new Azure subscription and associate it with your Office 365 account in order to register and manage apps.</span></span>


<!---<a name="bk_AssociateExistingAzureSubscription"> </a>-->

## <a name="to-associate-an-existing-azure-subscription-with-your-office-365-account"></a><span data-ttu-id="bc308-123">Para asociar una suscripción de Azure existente con la cuenta de Office 365</span><span class="sxs-lookup"><span data-stu-id="bc308-123">To associate an existing Azure subscription with your Office 365 account</span></span>


1. <span data-ttu-id="bc308-124">Inicie sesión en [Microsoft Azure Portal](https://portal.azure.com) con sus credenciales de Azure existentes (por ejemplo, un identificador de Microsoft como user@live.com).</span><span class="sxs-lookup"><span data-stu-id="bc308-124">Log on to the  [Microsoft Azure portal](https://portal.azure.com) with your existing Azure credentials (for example, your Microsoft ID such as user@live.com).</span></span>
        
2. <span data-ttu-id="bc308-125">Seleccione el nodo **Active Directory**. Después, seleccione la pestaña **Directorio** y, en la parte inferior de la pantalla, haga clic en **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="bc308-125">Select the  **Active Directory** node, then select the **Directory** tab and, at the bottom of the screen, select **New**.</span></span> 
     
4. <span data-ttu-id="bc308-126">En el menú **Nuevo**, seleccione **Active Directory**  >  **Directorio**  >  **Creación personalizada**.</span><span class="sxs-lookup"><span data-stu-id="bc308-126">On the **New** menu, select **Active Directory** > **Directory** > **Custom Create**.</span></span>
    
5. <span data-ttu-id="bc308-p104">En **Agregar directorio**, en el cuadro desplegable **Directorio**, seleccione **Usar directorio existente**. Active **Todo listo para cerrar sesión** y seleccione la casilla en la esquina inferior derecha.</span><span class="sxs-lookup"><span data-stu-id="bc308-p104">In **Add directory**, in the **Directory** dropdown box, select  **Use existing directory**. Check **I am ready to be signed out**, and then select the check mark in the lower-right corner.</span></span> 
    
    <span data-ttu-id="bc308-129">Regresará a Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="bc308-129">This brings you back to the Azure portal.</span></span>
        
3. <span data-ttu-id="bc308-130">Inicie sesión con su cuenta de Office 365.</span><span class="sxs-lookup"><span data-stu-id="bc308-130">Log in with your Office 365 account information.</span></span> 
    
    <span data-ttu-id="bc308-131">Se le preguntará si desea usar su directorio con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc308-131">You will be prompted whether to use your directory with Azure.</span></span> 
    
    ><span data-ttu-id="bc308-132">**Importante:** Para poder asociar su cuenta de Office 365 a Azure AD, necesitará una cuenta de Office 365 para empresas con privilegios de administrador global.</span><span class="sxs-lookup"><span data-stu-id="bc308-132">**Important:** To associate your Office 365 account with Azure AD, you'll need  an Office 365 business account with global administrator privileges.</span></span> 
    
        
4. <span data-ttu-id="bc308-133">Seleccione **Continuar** y luego **Cerrar sesión ahora**.</span><span class="sxs-lookup"><span data-stu-id="bc308-133">Select  **continue**, and then **Sign out now**.</span></span>
        
5. <span data-ttu-id="bc308-p105">Cierre el explorador y vuelva a abrir el [portal](https://manage.windowsazure.com). Si no lo hace, obtendrá un mensaje de acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="bc308-p105">Close the browser and reopen the  [portal](https://manage.windowsazure.com). Otherwise, you will get an access denied error.</span></span>
    
        
6. <span data-ttu-id="bc308-p106">Vuelva a iniciar sesión con sus credenciales de Azure existentes (por ejemplo, un identificador de Microsoft como user@live.com). Vaya al nodo de **Active Directory**; su cuenta de Office 365 debería aparecer ahora en **Directorio**.</span><span class="sxs-lookup"><span data-stu-id="bc308-p106">Log on again with your existing Azure credentials (for example, your Microsoft ID such as user@live.com). Go to the  **Active Directory** node and, under **Directory**, you should now see your Office 365 account listed.</span></span>
    

<!--<a name="bk_AssociateNewAzureSubscription"> </a>-->

## <a name="to-create-a-new-azure-subscription-and-associate-it-with-your-office-365-account"></a><span data-ttu-id="bc308-138">Cómo crear una nueva suscripción a Azure y asociarla a su cuenta de Office 365</span><span class="sxs-lookup"><span data-stu-id="bc308-138">To create a new Azure subscription and associate it with your Office 365 account</span></span>


1. <span data-ttu-id="bc308-p107">Inicie sesión en Office 365. Desde la página **Inicio**, seleccione el icono **Administrador** para abrir el Centro de administración de Office 365.</span><span class="sxs-lookup"><span data-stu-id="bc308-p107">Log on to Office 365. From the **Home** page, select the **Admin** icon to open the Office 365 admin center.</span></span>
2. <span data-ttu-id="bc308-141">En el lado izquierdo de la página de menú, desplácese hacia abajo hasta **Administrador** y seleccione **Azure AD**.</span><span class="sxs-lookup"><span data-stu-id="bc308-141">In the menu page along the left side of the page, scroll down to **Admin** and select **Azure AD**.</span></span>

    ><span data-ttu-id="bc308-142">**Importante:** Para abrir el Centro de administración de Office 365 y obtener acceso a Azure AD, necesitará una cuenta de Office 365 para empresas con privilegios de administrador global.</span><span class="sxs-lookup"><span data-stu-id="bc308-142">**Important:** To open the Office 365 admin center, and access Azure AD, you'll need  an Office 365 business account with global administrator privileges.</span></span> 
    
3. <span data-ttu-id="bc308-143">Cree una suscripción.</span><span class="sxs-lookup"><span data-stu-id="bc308-143">Create a new subscription.</span></span>
        
    <span data-ttu-id="bc308-p108">Si está usando una versión de prueba de Office 365, verá un mensaje en el que se le indica que Azure AD está limitado a clientes con servicios de pago. Puede crear una suscripción de prueba de 30 días gratuita, pero deberá realizar algunos pasos adicionales:</span><span class="sxs-lookup"><span data-stu-id="bc308-p108">If you're using a trial version of Office 365, you'll see a message telling you that Azure AD is limited to customers with paid services. You can still create a trial 30-day Azure subscription at no charge, but you'll need to perform a few extra steps:</span></span>
    
    1. <span data-ttu-id="bc308-146">Seleccione su país o región y elija **Suscripción a Azure**.</span><span class="sxs-lookup"><span data-stu-id="bc308-146">Select your country or region, and then choose **Azure subscription**.</span></span>
    2. <span data-ttu-id="bc308-p109">Escriba su información personal. Con fines de verificación, escriba un número de teléfono en el que podamos contactar con usted y especifique si prefiere recibir un mensaje de texto o una llamada.</span><span class="sxs-lookup"><span data-stu-id="bc308-p109">Enter your personal information. For verification purposes, enter a telephone number at which you can be reached, and specify whether you want to be sent a text message or called.</span></span>
    3. <span data-ttu-id="bc308-149">Una vez que reciba el código de verificación, escríbalo y elija **Comprobar código**.</span><span class="sxs-lookup"><span data-stu-id="bc308-149">When you receive your verification code, enter it and choose **Verify code**.</span></span>
    4. <span data-ttu-id="bc308-150">Escriba la información de pago, revise el contrato y seleccione **Suscribirse**.</span><span class="sxs-lookup"><span data-stu-id="bc308-150">Enter payment information, check the agreement, and select **Sign up**.</span></span>
        
        <span data-ttu-id="bc308-151">No se efectuará ningún cargo en su tarjeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="bc308-151">Your credit card will not be charged.</span></span>
        
        <span data-ttu-id="bc308-152">No cierre ni actualice el explorador mientras se crea la suscripción a Azure.</span><span class="sxs-lookup"><span data-stu-id="bc308-152">Do not close or refresh your browser while your Azure subscription is being created.</span></span>
            
4. <span data-ttu-id="bc308-153">Una vez creada la suscripción a Azure, elija **Portal**.</span><span class="sxs-lookup"><span data-stu-id="bc308-153">When your Azure subscription is created, choose  **Portal**.</span></span>
        
5. <span data-ttu-id="bc308-p110">Se iniciará el paseo por Azure. Puede verlo o elegir **X** para cerrarlo.</span><span class="sxs-lookup"><span data-stu-id="bc308-p110">The Azure Tour appears. You can view it, or choose  **X** to close it.</span></span>
        
    <span data-ttu-id="bc308-p111">Ahora, debería ver todos los elementos de su suscripción a Azure. El directorio que se muestra incluye el nombre de su espacio empresarial de Office 365.</span><span class="sxs-lookup"><span data-stu-id="bc308-p111">You should now see all items in your Azure subscription. It lists a directory with the name of your Office 365 tenant.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc308-158">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="bc308-158">See also</span></span>
- [<span data-ttu-id="bc308-159">Conceptos básicos del registro de aplicaciones en Azure AD</span><span class="sxs-lookup"><span data-stu-id="bc308-159">Basics of Registering an Application in Azure AD</span></span>](https://azure.microsoft.com/es-ES/documentation/articles/active-directory-authentication-scenarios/#basics-of-registering-an-application-in-azure-ad)
- [<span data-ttu-id="bc308-160">Agregar, actualizar o quitar una aplicación en Azure AD</span><span class="sxs-lookup"><span data-stu-id="bc308-160">Add, update, or remove an application in Azure AD</span></span>](https://azure.microsoft.com/es-ES/documentation/articles/active-directory-integrating-applications/)
