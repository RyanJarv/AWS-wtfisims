# wtf aws

#### SendMessage vs BatchSendMessage

*TODO: Confirm this*

We all know the APIs don't always match one to one with IAM permissions, seems SendMessage and BatchSendMessage might
be one of these cases. Just maybe though, since apparently this depends on if you are using a resource policy vs an
IAM policy, because the BatchSendMessage is only valid in the former.

[Pointed out thanks to @sumodirjo on Twitter](https://twitter.com/sumodirjo/status/1433246681605320705?s=20)


