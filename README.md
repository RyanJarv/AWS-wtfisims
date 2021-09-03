# wtf aws

### Goal

Would like this to be a compilation of behaviors in AWS that are surprising and interesting. These should be about design decisions in AWS that can be described in a short paragraph, not one off bugs or complicated issues that can't easily be summed up.

I feel like when I read lists like this for programming languages you end up getting a bit better idea how the language really works behind the scenes, so if people where able to read this and feel like they have a better idea of how AWS really works I think that would be pretty cool. But this goal is somewhat secondary to the list simply being interesting to read.

#### Ideas for this list (WIP)
* AWS resource policy magic (ARN <-> AROA conversions)
  * Convert AROA to arn's (ref: https://twitter.com/__steele/status/1433212318465159171?s=20)
  * Enumerating valid ARN's (ref: bunch of stuff)
* List actions don't just list stuff.
  * ListFunctions returns environment variables, which often contains secrets. 
* Parameters with that have `name` in the name don't actually take a name as the argument.
  * events:PutRule EventBusName iirc
* AWS actions don't map one to one with IAM actions
  * It's also not immediately obvious in what cases this happens.
* Anyone with access to the IMDS service can intercept SSM sessions for that instancce.
  *  Can sum this up with the credentials are the only way SSM identifies a connection from a host.
* S3 AllAuthenticatedUsers means *all* AWS users across *all* accounts.
  *  It's old but it checks out.
* There are six different ways of managing S3 permissions.
  * Bucket ACLs
  * Object ACLs
  * Bucket Policy
  * IAM Policy
  * RAM (something added for s3 in outposts recently, forget what exactly)
  * Public blocks (or whatever the name of those block options are)


