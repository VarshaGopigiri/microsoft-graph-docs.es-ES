<span data-ttu-id="830a4-p116">Los mismos [permisos](./permissions_reference.md) necesarios para leer de o escribir en un recurso específico, también son necesarios para hacerlo en cualquier extensión de datos de dicho recurso.  Por ejemplo, para que una aplicación pueda actualizar el perfil del usuario que ha iniciado sesión con datos personalizados de la misma, esta debe tener el permiso *User.ReadWrite.all*.</span><span class="sxs-lookup"><span data-stu-id="830a4-p116">The same [permissions](./permissions_reference.md) that are required to read from or write to a specific resource are also required to read from or write to any extensions data on that resource.  For example, for an app to be able to update the signed-in user's profile with custom app data, the app must have been granted the *User.ReadWrite.All* permission.</span></span>

Los mismos [permisos](./permissions_reference.md) necesarios para leer de o escribir en un recurso específico, también son necesarios para hacerlo en cualquier extensión de datos de dicho recurso.  Por ejemplo, para que una aplicación pueda actualizar el perfil del usuario que ha iniciado sesión con datos personalizados de la misma, esta debe tener el permiso *User.ReadWrite.all*.

<span data-ttu-id="830a4-229">Además, para crear y administrar definiciones de extensión de esquema, una aplicación debe contar con el permiso *Directory.AccessAsUser.All*.</span><span class="sxs-lookup"><span data-stu-id="830a4-229">Additionally, to create and manage schema extension definitions, an application must be granted the *Directory.AccessAsUser.All* permission.</span></span>

## <a name="data-limits"></a><span data-ttu-id="830a4-230">Límites de datos</span><span class="sxs-lookup"><span data-stu-id="830a4-230">Data limits</span></span>

### <a name="open-extension-limits"></a><span data-ttu-id="830a4-231">Límites de extensión abiertos</span><span class="sxs-lookup"><span data-stu-id="830a4-231">Open extension limits</span></span>
<span data-ttu-id="830a4-232">Los límites siguientes se aplican a los recursos de directorio (como **user**, **group**, **device**):</span><span class="sxs-lookup"><span data-stu-id="830a4-232">The following limits apply to directory resources (such as **user**, **group**, **device**):</span></span>

- <span data-ttu-id="830a4-233">Cada extensión abierta puede tener hasta 2 KB de datos (incluida la propia definición de extensión).</span><span class="sxs-lookup"><span data-stu-id="830a4-233">Each open extension can have up to 2KB of data (including the extension definition itself).</span></span>
- <span data-ttu-id="830a4-234">Una aplicación puede agregar hasta dos extensiones abiertas por cada instancia del recurso.</span><span class="sxs-lookup"><span data-stu-id="830a4-234">An application can add up to two open extensions per resource instance.</span></span>

### <a name="schema-extension-limits"></a><span data-ttu-id="830a4-235">Límites de extensión del esquema</span><span class="sxs-lookup"><span data-stu-id="830a4-235">Schema extension limits</span></span>
<span data-ttu-id="830a4-236">Una aplicación no puede crear más de cinco definiciones de **extensión del esquema**.</span><span class="sxs-lookup"><span data-stu-id="830a4-236">An application may create no more than five **schema extension** definitions.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="830a4-237">Limitaciones conocidas</span><span class="sxs-lookup"><span data-stu-id="830a4-237">Known limitations</span></span>

<span data-ttu-id="830a4-238">Para ver las limitaciones conocidas al usar las extensiones, consulte la [sección de extensiones](known_issues.md#extensions) del artículo de problemas conocidos.</span><span class="sxs-lookup"><span data-stu-id="830a4-238">For known limitations using extensions, see the [extensions section](known_issues.md#extensions) in the known issues article.</span></span>

## <a name="see-also"></a><span data-ttu-id="830a4-239">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="830a4-239">See also</span></span>

[<span data-ttu-id="830a4-240">Dominios de Office 365</span><span class="sxs-lookup"><span data-stu-id="830a4-240">Office 365 domains</span></span>](https://technet.microsoft.com/en-us/library/office-365-domains.aspx)

[<span data-ttu-id="830a4-241">Agregar y comprobar un dominio para un inquilino de Office 365</span><span class="sxs-lookup"><span data-stu-id="830a4-241">Adding and verifying a domain for an Office 365 tenant</span></span>](http://office365support.ca/adding-and-verifying-a-domain-for-the-new-office-365/)


## <a name="next-steps"></a><span data-ttu-id="830a4-242">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="830a4-242">Next steps</span></span>

<span data-ttu-id="830a4-243">Vea un ejemplo que utiliza una extensión abierta para ampliar el recurso de **usuario** con datos de perfil móvil personalizados:</span><span class="sxs-lookup"><span data-stu-id="830a4-243">See an example that uses an open extension to extend the **user** resource with custom roaming profile data:</span></span>

[<span data-ttu-id="830a4-244">Agregar datos personalizados a los usuarios mediante extensiones abiertas</span><span class="sxs-lookup"><span data-stu-id="830a4-244">Add custom data to users using open extensions</span></span>](extensibility_open_users.md)

<span data-ttu-id="830a4-245">Vea un ejemplo que utiliza una extensión de esquema para ampliar el recurso de **grupo** con datos de curso de aprendizaje:</span><span class="sxs-lookup"><span data-stu-id="830a4-245">See an example that uses a schema extension to extend the **group** resource with training course data:</span></span>

[<span data-ttu-id="830a4-246">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="830a4-246">Add custom data to groups using schema extensions</span></span>](extensibility_schema_groups.md)

