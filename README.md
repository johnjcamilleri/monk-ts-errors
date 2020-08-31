#  monk-ts-errors

Minimal working example to show typing errors with Monk 7.3.1.
See https://github.com/Automattic/monk/issues/316

## Reproducing errors

```
npm run build
```

## Output
```
node_modules/monk/index.d.ts:45:22 - error TS2314: Generic type 'FindOneOptions<T>' requires 1 type argument(s).

45   type FindOptions = FindOneOptions & { rawCursor?: boolean };
                        ~~~~~~~~~~~~~~

node_modules/monk/index.d.ts:203:16 - error TS2314: Generic type 'FindOneOptions<T>' requires 1 type argument(s).

203       options: FindOneOptions & { rawCursor: true },
                   ~~~~~~~~~~~~~~

node_modules/monk/index.d.ts:210:16 - error TS2314: Generic type 'FindOneOptions<T>' requires 1 type argument(s).

210       options: FindOneOptions,
                   ~~~~~~~~~~~~~~

node_modules/monk/index.d.ts:216:17 - error TS2314: Generic type 'FindOneOptions<T>' requires 1 type argument(s).

216       options?: FindOneOptions
                    ~~~~~~~~~~~~~~

node_modules/monk/index.d.ts:220:16 - error TS2314: Generic type 'FindOneOptions<T>' requires 1 type argument(s).

220       options: FindOneOptions,
                   ~~~~~~~~~~~~~~

node_modules/monk/index.d.ts:226:17 - error TS2314: Generic type 'FindOneAndDeleteOption<T>' requires 1 type argument(s).

226       options?: FindOneAndDeleteOption
                    ~~~~~~~~~~~~~~~~~~~~~~

node_modules/monk/index.d.ts:230:16 - error TS2314: Generic type 'FindOneAndDeleteOption<T>' requires 1 type argument(s).

230       options: FindOneAndDeleteOption,
                   ~~~~~~~~~~~~~~~~~~~~~~

node_modules/monk/index.d.ts:238:17 - error TS2314: Generic type 'FindOneAndUpdateOption<T>' requires 1 type argument(s).

238       options?: FindOneAndUpdateOption & { replaceOne?: false }
                    ~~~~~~~~~~~~~~~~~~~~~~

node_modules/monk/index.d.ts:243:17 - error TS2314: Generic type 'FindOneAndUpdateOption<T>' requires 1 type argument(s).

243       options?: FindOneAndUpdateOption & { replaceOne?: false },
                    ~~~~~~~~~~~~~~~~~~~~~~

node_modules/monk/index.d.ts:250:17 - error TS2314: Generic type 'FindOneAndReplaceOption<T>' requires 1 type argument(s).

250       options?: FindOneAndReplaceOption & { replaceOne: true }
                    ~~~~~~~~~~~~~~~~~~~~~~~

node_modules/monk/index.d.ts:255:16 - error TS2314: Generic type 'FindOneAndReplaceOption<T>' requires 1 type argument(s).

255       options: FindOneAndReplaceOption & { replaceOne: true },
                   ~~~~~~~~~~~~~~~~~~~~~~~
```

## Workaround

```
npm install monk@7.3.0
```
