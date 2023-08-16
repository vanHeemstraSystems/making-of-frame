# 2300 - Test storybook

Open the repository in gitpod by following this URL https://gitpod.io/new/#https://github.com/creations-global/frame/blob/main/README.md or clicking on the Gitpod button along the top of the page.

Gitpod will automatically build a development environment for you, using the code from the repository.

In Gitpod development environment you can use the integrated terminal to execute commands.

Gitpod will by default run the script ```start``` in package.json and therefor set the development environment to watch for code changes. Hence, open a separate terminal session to edit your files.

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

Alternatively, you can test creating a **pull request** by creating a **new feature**, by changing a file, followed by this command (replace name-your-feature-here with an appropriate text):

```
$ git add . && git checkout -b feat/name-your-feature-here
```

You will be prompted as follows:

```
Switched to a new branch 'feat/name-your-feature-here'
```

Next, run:

```
$ git add . && npm run commit && git push
```

Commitizen will automatically run git-cz. When prompted, answer as follows:

```
? Select the type of change that you're committing: feat: A new feature
```

Continue with answering the prompts as you see fit.

Lastly, run this command:

```
$ git push --set-upstream origin feat/name-your-feature-here
```

When opening the repository in the browser at https://github.com/creations-global/frame click the button that will show labeled **Compare pull request**.

You will be presented with a window called "Open a pull request". In the bottom of the text field click on the button labeled **Create pull request**.

As expected, on every pull request, the GitHub Action automatically runs to verify the quality of the change against all OS types and Node versions set in ```.github/workflows/publish.yml```. Wait for the checks to have passed successfully.

**WARNING**: Instead of clicking on the **Merge pull request** button directly, click on the drop-down menu of this button and choose **Rebase and merge**, then click **Rebase and merge**. Otherwise, you would loose all the previous commit messages and semantic release will not pick it up.

Next, click on the **Confirm rebase and merge** button.

If all goes well, you will be prompted that the pull request has been successfully merged and closed. Hooray!!

If you check the publish.yml GitHub action, you will see that the ```publish``` instruction has been skipped, as the change was on a ```feature``` branch, instead of the ```main``` branch.

However, since we merged the change into the ```main``` branch, a new GitHub action has started automatically which will also include the ```publish``` instruction, as it is on the ```main``` branch.

**NOTE**: Currently publishing to NPM fails as it cannot find https://registry.npmjs.org/@creations-global%2fframe  This needs to be fixed ...
