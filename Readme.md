# Static Web hosting from Azure Blob

## Notes
- Unfortunately, Azure storage accounts do not yet have the option to import your own SSL certificates. That means, if we want to enable HTTPS for our static website custom domains, we have to use the Azure Content Delivery Network.
- ne of the key features of Azure CDN is its HTTPS custom domain support, and that’s exactly the reason why we’re using it in this guide. 

## Steps
- Resource Group: 
- storage account:
    - enable static-website capability
        - $web folder will be automatically created once the static-website capabiltiy is enabled
        - upload files (index.html and error404.html) to this $web directory
        - now the you able to access the site.
    - create CDN profile 
- Enable custom domain (after adding a cname to the CDN endpoint)
    - enable HTTPS for custome domain (with TLS1.2 and CDN managed key)
    

### url endpoints
- https://mustaticwebhost.z13.web.core.windows.net/

## References
- https://itnext.io/the-only-guide-you-need-for-a-static-website-in-azure-part-2-host-your-static-site-in-azure-9114b7069db2
