# Hosting Test - GitHub Pages with Git LFS

This is a test of hosting a Hugo project on GitHub Pages with Git LFS.

## Source

All components are imported from the [`jmooring/hugo-module-feature-test`][] module. See its [README][] file for details.

## Using Git LFS

1. Install [git-lfs](https://git-lfs.com/).
1. Create a local repository with `git init`.
1. Configure Git LFS to manage various file types.

    ```sh
    git lfs track "*.gif"
    git lfs track "*.jpeg"
    git lfs track "*.jpg"
    git lfs track "*.png"
    git lfs track "*.webp"
    ```

The last step will either create a `.gitattributes` file or modify an existing `.gitattributes` file. Make sure that the `.gitattributes` file is tracked in your repository.

Files committed _after_ the above steps will be stored in LFS.

[`jmooring/hugo-module-feature-test`]: https://github.com/jmooring/hugo-module-feature-test
[README]: https://github.com/jmooring/hugo-module-feature-test?tab=readme-ov-file#readme
