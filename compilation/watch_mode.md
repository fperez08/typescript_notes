Now, let's have a look at how we can watch multiple files in TypeScript.

Let's say we have a more complex project with multiple TypeScript files. To compile all TypeScript files in the project and watch for changes, we can use the `--watch` or `-w` option with a wildcard `*` to include all TypeScript files in the compilation. Here's an example:

```bash
tsc --init
tsc -w
```

In this example, the `--init` flag initializes a `tsconfig.json` file if you don't have one already. After that, the `-w` flag starts the TypeScript compiler in watch mode.

Now, TypeScript will watch for changes in all TypeScript files in the project and recompile them whenever there's a modification.

Remember that in a larger project, it's common to have a `tsconfig.json` file that specifies compiler options and includes/excludes files. In that case, you can run `tsc -w` without the need for additional flags.

This approach allows you to develop more efficiently, as any changes you make in any TypeScript file will trigger automatic compilation without having to specify each file individually.
