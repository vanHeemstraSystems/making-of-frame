# 2300 - Test storybook

Open the repository in gitpod by following this URL or clicking on the Gitpod button along the top of the page.

Gitpod will automatically build a development environment for you, using the code from the repository.

In Gitpod development environment you can use the integrated terminal to execute commands.

To commit changes after making file changes run the following command:

```
$ git add .
$ npx cz
```

This will trigger *commitizen (cz)* and you will be prompted to describe your change. 

Follow with ```git push```.

Our Github Actions workflow with automatically build a package from the source code and publish it to npm.

You can see the latest releases in the Github repository at https://github.com/creations-global/frame/releases

After a successful publish of the package to npm, you can view the package on npmjs.com by entering the following in the search on https://npmjs.com:

```
@creations-global/frame
```

Or go directly to https://www.npmjs.com/package/@creations-global/frame

To install the node module package use the following:

```
$ npm i @creations-global/frame
```
