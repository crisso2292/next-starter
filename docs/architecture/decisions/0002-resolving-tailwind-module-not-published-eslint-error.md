# tailwindcss ESLint: "tailwindcss" is not published.(node/no-unpublished-import

* Date: 2024-02-23

## Context and Problem Statement

After adding `gts` to the project, the ESLint error `tailwindcss` is not published is shown. This is because eslint
thinks that typescript is not recognizing the `tailwindcss` package.
![](/Users/cristhiansoria/Documents/dev/projects/personal/next-starter/docs/doc-images/tailwindcss-error.png)

# Solution

The solution is to move the `talwindcss` package from `devDependencies` to `dependencies` in the `package.json` file.

## Decision Driver

Dev Dependencies are not recognized by our linter setup as a published package. We need tailwindcss in the
devDependencies anyway to work wih the project.
