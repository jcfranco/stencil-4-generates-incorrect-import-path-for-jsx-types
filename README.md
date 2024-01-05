# stencil-4-generates-incorrect-import-path-for-jsx-types

This shows that Stencil 4 + [React wrappers](https://github.com/ionic-team/stencil-ds-output-targets/tree/main/packages/react-output-target) generates an incorrect import path, which causes an error when building the wrappers (per the [React output target example](https://github.com/ionic-team/stencil-ds-output-targets/tree/main/packages/example-project/component-library-react)).

## Steps to reproduce

1. Clone this repo
2. `npm install`
3. `npm run build`

This will produce the following error:

```cli
      src/components.ts(6,15): error TS2305: Module '"component-library/dist/components"' has no exported member 'JSX'.
       npm ERR! Lifecycle script `tsc` failed with error:
       npm ERR! Error: command failed
       npm ERR!   in workspace: component-library-react@4.20.69
       npm ERR!   at location: /.../stencil-4-generates-incorrect-import-path-for-jsx-types/packages/component-library-react
       npm ERR! Lifecycle script `build` failed with error:
       npm ERR! Error: command failed
       npm ERR!   in workspace: component-library-react@4.20.69
       npm ERR!   at location: /.../stencil-4-generates-incorrect-import-path-for-jsx-types/packages/component-library-react
```
