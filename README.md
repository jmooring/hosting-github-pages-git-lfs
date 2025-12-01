# Hosting Test - GitHub Pages with Git LFS

This is a test of hosting a Hugo site on GitHub Pages with Git LFS.

This site:

1. Includes content from a Hugo module
1. Transpiles Sass to CSS using Dart Sass
1. Performs vendor prefixing of CSS rules using the postcss, postcss-cli, and autoprefixer Node.js packages
1. Processes CSS files using the tailwindcss and @tailwindcss-cli Node.js packages
1. Encodes images to the WebP format to verify that we're using Hugo's extended edition
1. Includes a content file named hugö.md to verify that the Git `core.quotepath` setting is `false` [^1]

[^1]: See [issue #9810](https://github.com/gohugoio/hugo/issues/9810). Git's `core.quotepath` setting is `false` if `/tests/hugö` has a non-zero "last modified" date.

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
