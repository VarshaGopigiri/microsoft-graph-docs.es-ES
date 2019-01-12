---
title: Uso de sugerencias de orden en Planner
description: '`)'
author: TarkanSevilmis
localization_priority: Normal
ms.prod: planner
ms.openlocfilehash: 03b2ec61d267e0c04c6ba6360bb28bb04bffda54
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923484"
---
# <a name="using-order-hints-in-planner"></a><span data-ttu-id="6d7c0-103">Uso de sugerencias de orden en Planner</span><span class="sxs-lookup"><span data-stu-id="6d7c0-103">Using order hints in Planner</span></span>

<span data-ttu-id="6d7c0-p101">Los objetos de Planner identifican sus criterios de ordenación por sugerencias de ordenación. Los valores de sugerencias de ordenación son cadenas. Los clientes pueden ordenar las cadenas basándose en el valor ordinal de su caracteres para identificar el orden de los elementos. Se comparan los caracteres desde el principio de la cadena hasta que se detecta una diferencia en los valores ordinales de caracteres o termina una cadena, en cuyo caso se colocará la cadena más corta antes que la más larga. Los valores pueden contener cualquier carácter entre ordinales 32 (espacio) y 126 (`~`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-p101">Objects in Planner identify their sort order by order hints. The order hint values are strings. The clients can sort the strings based on ordinal value of characters in them to identify the order of items. The characters are compared from the beginning of the string, until a difference is encountered in the ordinal values of characters, or one string ends, in which case the shorter string would be sorted before the longer. The values can contain any character between ordinals 32 (space) and 126 (`~`)</span></span>

<span data-ttu-id="6d7c0-p102">Por ejemplo, un elemento con la sugerencia de ordenación `a` (valor ordinal 97) se colocaría antes que otro con la sugerencia de ordenación `z` (valor ordinal 122). Por ejemplo, un elemento con la sugerencia de ordenación `abc` (valores ordinales 97, 98 y 99) se colocaría antes que otro con la sugerencia de ordenación `abd` (valores ordinales 97, 98, 100). Un elemento con la sugerencia de ordenación `a` se colocaría antes que otro con la sugerencia de ordenación `ab` puesto que todos los caracteres existentes son los mismos, y `a` es más corta.</span><span class="sxs-lookup"><span data-stu-id="6d7c0-p102">As an example, an item with order hint `a` (ordinal value 97) would be placed before another item with order hint `z` (ordinal value 122). An item with order hint `abc` (ordinal values 97, 98, 99), would be placed before another item with order hint `abd` (ordinal values 97, 98, 100). An item with order hint `a` would be placed before another item with order hint `ab` since all existing characters are the same, and `a` is shorter.</span></span>

<span data-ttu-id="6d7c0-p103">Se calculan los valores de todas las sugerencias de ordenación por el servicio. Para reordenar elementos, el cliente puede especificar la sugerencia de ordenación para el elemento que se ha movido entre dos elementos. Para ello, debe establecer la sugerencia de ordenación en el valor siguiente: `<previous order hint> <next order hint>!`, donde `<previous order hint>` debe sustituirse por la sugerencia de ordenación del elemento que precede a la nueva ubicación deseada y `<next order hint>` debe sustituirse por la sugerencia de ordenación del elemento que viene después de la nueva localización deseada. Hay un carácter de espacio entre estos valores de sugerencia de ordenación, y el valor completo se añade como sufijo con `!`. Si un elemento no está presente, debe utilizarse una cadena vacía en su lugar. Este valor también puede estar compuesto de cálculos previos y puede utilizarse en el cliente para ordenar elementos de forma exacta como el servicio que devuelve sugerencias de ordenación. Una vez que el cliente envía estos valores en una actualización, el servicio calculará un valor pequeño que ordene en la ubicación deseada.</span><span class="sxs-lookup"><span data-stu-id="6d7c0-p103">The values for all order hints are calculated by the service. The client can reorder items by specifying the order hint for the item that got moved between two items with by setting the order hint to the following value: `<previous order hint> <next order hint>!`, where `<previous order hint>` is to be replaced by the order hint of the item that comes before the new desired location, and `<next order hint>` is to be replaced by the order hint of the item that comes after the new desired location. There is a space character between these order hint values, and the entire value is suffixed with `!`. If either item isn't present, empty string should be used instead. This value can also be composed of previous calculations, and can be used in the client to sort items exactly like service returned order hints. Once the client sends these values in an update, the service will calculate a short value that sorts in the desired location.</span></span>

<span data-ttu-id="6d7c0-118">**Tenga en cuenta** que, en los ejemplos siguientes, los valores actuales de sugerencia de ordenación se sitúan entre comillas simples (`'`) para mayor claridad, sin embargo estas no forman parte de los datos y no se deben enviar al servicio.</span><span class="sxs-lookup"><span data-stu-id="6d7c0-118">**Please note** that in the following examples the actual order hint values are surrounded in single quote characters (`'`) for clarity, however these are not part of the data, and must not be sent to the service.</span></span>
 
<span data-ttu-id="6d7c0-119">Como ejemplo, considere la siguiente lista de sugerencias de ordenación ya ordenadas:</span><span class="sxs-lookup"><span data-stu-id="6d7c0-119">As an example, consider the following list of sorted order hints:</span></span>

1. <span data-ttu-id="6d7c0-120">Elemento 1 (sugerencia de ordenación: `'5637'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-120">Item 1 (Order Hint: `'5637'`)</span></span>
2. <span data-ttu-id="6d7c0-121">Elemento 2 (sugerencia de ordenación: `'adhg'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-121">Item 2 (Order Hint: `'adhg'`)</span></span>

<span data-ttu-id="6d7c0-122">Colocar un elemento 3 antes del elemento 1, después, colocar un elemento 4 entre los elementos 1 y 2 y, luego, colocar un elemento 5 después de un elemento 2 crearía las siguientes sugerencias de ordenación en el cliente.</span><span class="sxs-lookup"><span data-stu-id="6d7c0-122">Placing an Item 3 before Item 1, then placing item 4 between Item 1 and Item 2, and then placing item 5 after Item 2, would create the following order hints on the client.</span></span> 

1. <span data-ttu-id="6d7c0-123">Elemento 3 (sugerencia de ordenación: `' 5637!'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-123">Item 3 (Order Hint: `' 5637!'`)</span></span>
2. <span data-ttu-id="6d7c0-124">Elemento 1 (sugerencia de ordenación: `'5637'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-124">Item 1 (Order Hint: `'5637'`)</span></span>
3. <span data-ttu-id="6d7c0-125">Elemento 4 (sugerencia de ordenación: `'5637 adhg!'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-125">Item 4 (Order Hint: `'5637 adhg!'`)</span></span>
4. <span data-ttu-id="6d7c0-126">Elemento 2 (sugerencia de ordenación: `'adhg'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-126">Item 2 (Order Hint: `'adhg'`)</span></span>
5. <span data-ttu-id="6d7c0-127">Elemento 5 (sugerencia de ordenación: `'adhg !'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-127">Item 5 (Order Hint: `'adhg !'`)</span></span>

<span data-ttu-id="6d7c0-128">A continuación, mover un elemento 1 al final de la lista generaría:</span><span class="sxs-lookup"><span data-stu-id="6d7c0-128">Then, moving item 1 to the end of the list would generate:</span></span>

1. <span data-ttu-id="6d7c0-129">Elemento 3 (sugerencia de ordenación: `' 5637!'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-129">Item 3 (Order Hint: `' 5637!'`)</span></span>
2. <span data-ttu-id="6d7c0-130">Elemento 4 (sugerencia de ordenación: `'5637 adhg!'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-130">Item 4 (Order Hint: `'5637 adhg!'`)</span></span>
3. <span data-ttu-id="6d7c0-131">Elemento 2 (sugerencia de ordenación: `'adhg'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-131">Item 2 (Order Hint: `'adhg'`)</span></span>
4. <span data-ttu-id="6d7c0-132">Elemento 5 (sugerencia de ordenación: `'adhg !'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-132">Item 5 (Order Hint: `'adhg !'`)</span></span>
5. <span data-ttu-id="6d7c0-133">Elemento 1 (sugerencia de ordenación: `'adhg ! !'`) </span><span class="sxs-lookup"><span data-stu-id="6d7c0-133">Item 1 (Order Hint: `'adhg ! !'`)</span></span>

<span data-ttu-id="6d7c0-134">Finalmente, mover un elemento 5 entre los elementos 3 y 4 generaría:</span><span class="sxs-lookup"><span data-stu-id="6d7c0-134">Finally moving Item 5 between Item 3 and Item 4 would generate:</span></span>

1. <span data-ttu-id="6d7c0-135">Elemento 3 (sugerencia de ordenación: `' 5637!'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-135">Item 3 (Order Hint: `' 5637!'`)</span></span>
2. <span data-ttu-id="6d7c0-136">Elemento 5 (sugerencia de ordenación: `' 5637! 5637 adhg!!'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-136">Item 5 (Order Hint: `' 5637! 5637 adhg!!'`)</span></span>
3. <span data-ttu-id="6d7c0-137">Elemento 4 (sugerencia de ordenación: `'5637 adhg!'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-137">Item 4 (Order Hint: `'5637 adhg!'`)</span></span>
4. <span data-ttu-id="6d7c0-138">Elemento 2 (sugerencia de ordenación: `'adhg'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-138">Item 2 (Order Hint: `'adhg'`)</span></span>
5. <span data-ttu-id="6d7c0-139">Elemento 1 (sugerencia de ordenación: `'adhg ! !'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-139">Item 1 (Order Hint: `'adhg ! !'`)</span></span>

<span data-ttu-id="6d7c0-p104">Una vez que estos cambios en los valores de sugerencia de ordenación se envíen al servicio mediante solicitudes de revisión, el servicio calculará los valores adecuados que mantengan el orden pretendido por el cliente. El cliente puede obtener de inmediato los valores si se especifica la preferencia `return=representation` en las solicitudes `PATCH`. Los valores para el caso anterior pueden tener la apariencia siguiente (los valores reales pueden diferir).</span><span class="sxs-lookup"><span data-stu-id="6d7c0-p104">Once these changes to order hint values are sent to the service in patch requests, the service will calculate proper values that keep the order intended by the client. The client can obtain the values immediate if `return=representation` preference is specified in the `PATCH` requests. The values for the case above may look like the following (the actual values may differ).</span></span> 

1. <span data-ttu-id="6d7c0-143">Elemento 3 (sugerencia de ordenación: `'432b'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-143">Item 3 (Order Hint: `'432b'`)</span></span>
2. <span data-ttu-id="6d7c0-144">Elemento 5 (sugerencia de ordenación: `'6F"#'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-144">Item 5 (Order Hint: `'6F"#'`)</span></span>
3. <span data-ttu-id="6d7c0-145">Elemento 4 (sugerencia de ordenación: `'7A$6'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-145">Item 4 (Order Hint: `'7A$6'`)</span></span>
4. <span data-ttu-id="6d7c0-146">Elemento 2 (sugerencia de ordenación: `'adhg'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-146">Item 2 (Order Hint: `'adhg'`)</span></span>
5. <span data-ttu-id="6d7c0-147">Elemento 1 (sugerencia de ordenación: `'de5%'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-147">Item 1 (Order Hint: `'de5%'`)</span></span>

<span data-ttu-id="6d7c0-p105">Se pueden especificar las sugerencias de ordenación para crear el primer elemento en la lista como ` !`, puesto que en este caso no existe ni un elemento anterior ni uno posterior. Sin embargo, esto no es necesario dado que el servicio generará automáticamente todos los valores de sugerencia de ordenación de elementos si no se especifican durante la creación del elemento. El ejemplo siguiente muestra que las sugerencias de ordenación se deben utilizar al colocar elementos en una lista previamente vacía. Agregue el primer elemento:</span><span class="sxs-lookup"><span data-stu-id="6d7c0-p105">Order Hints can be specified for creating the first item in the list as ` !`, since neither a previous or a next item exists in that case, however this is unnecessary, as the service will auto-generate values for all order hint values on items if they are not specified during creation of the item. Following example illustrates the order hints should be used when placing items in a previously empty list. Add the first item:</span></span>

1. <span data-ttu-id="6d7c0-151">Elemento 1 (sugerencia de ordenación: `' !'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-151">Item 1 (Order Hint: `' !'`)</span></span>

<span data-ttu-id="6d7c0-152">Agregue el segundo elemento en la parte superior:</span><span class="sxs-lookup"><span data-stu-id="6d7c0-152">Add the second item to top:</span></span>

1. <span data-ttu-id="6d7c0-153">Elemento 2 (sugerencia de ordenación: `'  !!'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-153">Item 2 (Order Hint: `'  !!'`)</span></span>
2. <span data-ttu-id="6d7c0-154">Elemento 1 (sugerencia de ordenación: `' !'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-154">Item 1 (Order Hint: `' !'`)</span></span>

<span data-ttu-id="6d7c0-155">Agregar el tercer elemento en la parte inferior:</span><span class="sxs-lookup"><span data-stu-id="6d7c0-155">Add the third item to bottom:</span></span>

1. <span data-ttu-id="6d7c0-156">Elemento 2 (sugerencia de ordenación: `'  !!'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-156">Item 2 (Order Hint: `'  !!'`)</span></span>
2. <span data-ttu-id="6d7c0-157">Elemento 1 (sugerencia de ordenación: `' !'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-157">Item 1 (Order Hint: `' !'`)</span></span>
3. <span data-ttu-id="6d7c0-158">Elemento 3 (sugerencia de ordenación: `' ! !'`)</span><span class="sxs-lookup"><span data-stu-id="6d7c0-158">Item 3 (Order Hint: `' ! !'`)</span></span>







