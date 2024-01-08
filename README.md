This repo demonstrates a strange issue with auto-imports for drizzle-orm related to https://github.com/drizzle-team/drizzle-orm/issues/1771.

To reproduce:

1. `pnpm i`
2. Go to `index.ts`
3. Try to auto-import anything from drizzle-orm (for instance `inArray`). It will not work. If you manually type it out, it works. Once you have one import in the file, other auto-imports work fine.
4. If you delete any of the following packages from the package.json, rerun `pnpm i`, then restart the TS server, auto-import works:

- `formik`
- `moment-timezone`
- `next-auth`
- `next-redux-wrapper`
- `openid-client`
- `react-redux`
- `react-smooth-dnd`
- `redux-persist`
- `redux-thunk`
- `tss-react`
