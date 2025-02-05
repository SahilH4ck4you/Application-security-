## Googl Dorks
```bash
site: target.com inurl:index.php?option=com
site: target.com inurl:Itemid= -intext:Joomla
```
*This dork searches for a vulnerable Joomla component where we can inject our XSS payload.*


## Work On 4.0 to 4.2.7
https://vulncheck.com/blog/joomla-for-rce

## Joomla API endpoint

```bash
/api/index.php/v1/config/application?public=true
/api/index.php/v1/users?public=true
v1/banners
v1/banners/:id
v1/banners
v1/banners/:id
v1/banners/:id
v1/banners/clients
v1/banners/clients/:id
v1/banners/clients
v1/banners/clients/:id
v1/banners/clients/:id
v1/banners/categories
v1/banners/categories/:id
v1/banners/categories
v1/banners/categories/:id
v1/banners/categories/:id
v1/banners/:id/contenthistory
v1/banners/:id/contenthistory/keep
v1/banners/:id/contenthistory
v1/config/application
v1/config/application
v1/config/:component_name
v1/config/:component_name
v1/contacts/form/:id
v1/contacts
v1/contacts/:id
v1/contacts
v1/contacts/:id
v1/contacts/:id
v1/contacts/categories
v1/contacts/categories/:id
v1/contacts/categories
v1/contacts/categories/:id
v1/contacts/categories/:id
v1/fields/contacts/contact
v1/fields/contacts/contact/:id
```
