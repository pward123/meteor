# Npm.depends() support for git+sha urls

Meteor's Npm.depends() currently supports http/https github references. This is good enough for public repositories as well as local private repositories (i.e. github enterprise). However, this doesn't help if you're using standard private github repos.

This version of the meteor tools patches the Npm.depends() function to include support for git+sha npm references.

You'll still need to use the full SHA1 tag. This release just adds git+sha based urls in addition to the existing support for http/https.

Example:

```javascript
Npm.depends({
    "my-private-package": "git+ssh://git@github.com:my-git-user/my-private-package#8126acfe726a333abc71260da55a6242ffc8008b"
});
```

# meteor-tool

This is the Meteor command-line tool. Most of the code for it is in the [tools directory](https://github.com/meteor/meteor/tree/master/tools) of the Meteor repository.

The Meteor tool also includes testing functionality and example apps for the Meteor framework.

Read more about it on the [project page](https://www.meteor.com/tool)

