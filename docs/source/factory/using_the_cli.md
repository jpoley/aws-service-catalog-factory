Using the CLI
=============

When you install ```aws-service-catalog-factory``` you install a command line tool ```servicecatalog-factory```.

When you bootstrap the framework and upgrade it you use the cli tool to perform these actions.

There are other commands that you may find useful:

## nuke-product-version
You can use the ```servicecatalog-factory``` cli to remove a product from AWS Service Catalog and to remove
the AWS CodePipeline that was generated by this library.  To use it, you will need your portofolio name,
product name and product version - all of which is available to view from your AWS Service Catalog console.

Once you have the details you can run the following command:
```bash
servicecatalog-factory nuke-product-version example-simple-central-it-team-portfolio account-iam v1
```  

## delete-stack-from-all-regions
You can delete a stack from every region using the following command:
```bash
servicecatalog-factory delete-stack-from-all-regions stack-name
```
Please note, this will only delete the stack from the regions you have specifed in your config.


## fix-issues
Whilst developing your products you may find AWS CloudFormation stacks in states you cannot work with.  
If this happens the fix-issues command will try to resolve it for you.  It will prompt you to confirm
anything it does within your account before it does it so give it a try when you get stuck.

```bash
servicecatalog-factory fix-issues ServiceCatalogFactory/portfolios
``` 