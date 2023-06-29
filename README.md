## Repository for reproduce issue of @nx/js@16.4.0

[@nx/js:node executor](https://nx.dev/packages/js/executors/node#watch) don't work properly with option `"watch": false`

When run command `npx nx run server:serve` and then change file `apps/server/src/main.ts` started rebuild server and terminate command with next message:

```bash
>  NX  File change detected. Restarting...


 —————————————————————————————————————————————————————————————————

 >  NX   Successfully ran target serve for project server

 *  Terminal will be reused by tasks, press any key to close it.
```
