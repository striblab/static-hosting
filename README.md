# Hosting on static

Some general files and patterns for the `static.startribune.com` site

## Files for root

Some files for the root of `static.startribune.com`. Overall, we just want to have a note and a 404. And by default, have a nofollow robots.txt for search engines (not for security), and then make exceptions.

## Publishing

You can publish this, if you have the [awscli](https://aws.amazon.com/cli/) installed:

```
aws s3 sync ./index/ s3://static.startribune.com/ --acl="public-read" --exclude="*.DS_Store*"
```
