## Repository for reproduce issue of @nx/js@17.2.8

[@nx/js:node executor](https://nx.dev/packages/js/executors/node#watch) don't work properly with option `"watch": false` when `"runBuildTargetDependencies": true`

When run command `npx nx run server:serve` and then change file `apps/server/src/main.ts` started rebuild server and terminate command with next message:

```text
>  NX  File change detected. Restarting...


> nx run server:build  [local cache]

Compiling TypeScript files for project "server"...
Done compiling TypeScript files for project "server".

 ——————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————

 >  NX   Successfully ran target build for project server

   Nx read the output from the cache instead of running the command for 1 out of 1 tasks.


 ——————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————

 >  NX   Successfully ran target serve for project server
```
