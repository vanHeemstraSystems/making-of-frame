making-of-frame
# Making of Frame

Based on "Fully Automated npm publish using GitHub Actions and Semantic Release" at https://www.youtube.com/watch?v=QZdY4XYbqLI 

**WARNING**: In order for the automation to successfully push changes to the repository, make sure you have set the following at your repository's "Settings" > "Actions" > "General":

Workflow permissions

- [Checked]: Read and write permissions
- [Unchecked]: Read repository contents and packages permissions

If the option is disabled, you can enable that option under ORGANIZATION settings not REPO settings.

Organizations's "Settings" > "Actions" > "General":

Workflow permissions

- [Checked]: Read and write permissions
- [Unchecked]: Read repository contents and packages permissions

# Executive Summary

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
@creations_global/frame
```

**NOTE**: On npm the organization name is not creations-global, but creations_global (as creations-global was no longer available).

Or go directly to https://www.npmjs.com/package/@creations_global/frame

To install the node module package use the following:

```
$ npm i @creations_global/frame
```

## 100 - Introduction

See [README.md](./100/README.md)

## 200 - Requirements

See [README.md](./200/README.md)

## 300 - Buidling Our Application

See [README.md](./300/README.md)

## 400 - Conclusion

See [README.md](./400/README.md)
