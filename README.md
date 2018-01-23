# icerainzz
# How to publish packages to NPM 

---
## Create a User Account
To publish, you must be a user on the npm registry. If you aren't a user, create an account by using **npm adduser**.You also can [sign up][1] on the site.If you created a user account on the site, use **npm login** to access your account from your terminal.
### test:

 1. Type **npm whoami** from a terminal to see if you are already logged in (technically, this also means that your credentials have been stored locally).
 2. Check that your username has been added to the registry at https://npmjs.com/~username.
##github create project
 3. On [github][2],create a project and clone to local PC
 4. The terminal enters the project folder, executes the **npm init** command, builds the module's description file, and the system prompts you to enter the required information.

    >  The **name** field defines the name your package will have in the registry and people will install your package over the name you define.
    
    > The **version** tag defines the version of your package. You really should consider using semver. Because maybe a lot of people will use yourpackage. And there is no worse feeling then breaking peoples production code because you introduce breaking changes but only change the patch version of your package. �
    
    > In the **description** field you should add a quick and on-pointdescription, about your package. People will read it if they search for your package on npmjs.org
    
    > In the **author** field you add your name and e-mail, so people know who published the package. It's common to add it in the form of `Name<e-mail>`.
 
    > I guess the **license** field is one of the most forgotten fields. People often think it's not that important. However if you want people to use your package, maybe even in bigger projects you definitely should add a license. So they know if they can use it in commercial projects,what are the restrictions and so on.
    > 
    > You should also add the **repository** field, with a link to the github repo and you can also add the **bugs** field with the link to the github issues page. So people can report bugs and know where to request features.
    > 
    > You can also add **keywords** which help people to find your package if they search for something on npmjs.org.

##Publish
Use **npm publish** to publish the package.
#Congratulations on Publishing!
##Updating Your Package
###How To Update the Version Number
When you make changes, you can update the package using **npm version <update_type>**.

where <update_type> is one of the [semantic versioning][3] release types, patch, minor, or major.

This command will change the version number in **package.json**.

Note: this will also add a tag with the updated release number to your git repository if you have linked one to your npm account.

After updating the [version number][4], run **npm publish** again.

Test: Go to https://npmjs.com/package/<package>. The package number should be updated.

###How to Update the Read Me File
The README displayed on the site will not be updated unless a new version of your package is published, so you need to **run npm version** patch and **npm publish** to update the documentation displayed on the site.




    



 


  [1]: https://www.npmjs.com/signup
  [2]: https://github.com "github"
  [3]: https://docs.npmjs.com/getting-started/semantic-versioning
  [4]: https://docs.npmjs.com/cli/version
