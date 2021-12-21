#### What's this PR do?
Allows `@theoremlegal.com` users to:
* Create products not tied to organizations
* See and edit all product
* Automatically join any organization as a hidden teammate
#### Where should the reviewer start?
`<AdminApps />` and `<OrganizationProvider />`
#### How should this be manually tested?
Log in as a `@theoremlegal` account // join a vendor // make products in the admin pane
#### Any background context you want to provide?
* Products can only be created as an admin when the user's current organization is a vendor. This is because of how closely tied `create product logic` is to `vendor org logic`
* Whenever an admin creates a product **outside** of the admin editor (e.g. the vendor's normal homepage) it will _always_ be a test product. This is for Al and I
* Admin products created from the admin panel are **never** test products
* I did not automatically redirect to the admin panel as asked in [#288](https://user-images.githubusercontent.com/62047446/146984842-86692f02-8b1c-4dd1-8338-caa875a9811c.png) for two reasons:
1. This would be really annoying for me and Al
2. For some reason, it's dependance on `useUser` and `useOrganization` sometimes results in `null` being injected into the path. It seems this happens when the user accesses the component more quickly than other parts of the app. **Please note when this behavior occurs for you**
#### What task remain that are related to this PR?
* I think this could be more secure with user-types - currently it just looks at the users email for `@theoremlegal.com` when checking for admin privileges (or hiding a team user in the DOM)
* I think the sorting of products in the admin list could be better achieved via graphQl / the results of graphQl should also be paginated. 

[#1] Outlines ideas on how this project could be continued based on roles.
#### What are the relevant tickets?
close [#288](https://user-images.githubusercontent.com/62047446/146984842-86692f02-8b1c-4dd1-8338-caa875a9811c.png)
#### Screenshots (if appropriate)
![image](https://user-images.githubusercontent.com/62047446/138971391-ba8f3670-c238-4f3f-89b4-5f3069b4ef7a.png)
![image](https://user-images.githubusercontent.com/62047446/138971462-82783b06-315e-425a-a166-df563ea068df.png)

