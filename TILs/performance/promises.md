# Promises

## Performance degradation of event loops caused by GraphQL and Promises

The combination of GraphQL and NodeJS can result in an increased latency, since

- promise overhead - the modular structure of GraphQL can increase the number of promises and/or the number of DB queries. E.g. when you have to `await` in a for loop

  - This snippet helps us find out how promise-heavy our code is

    ```jsx
    import async_hooks from 'async_hooks';

    let count = 0;

    const hook = async_hooks.createHook({
      init(asyncId: number, type: string) {
        if (type === 'PROMISE') {
          count++;
        }
      },
    });

    hook.enable();

    setInterval(() => {
      console.log(`Promise count: ${count}`);
    }, 1000);
    ```

- promises add workload to event loop
- event loop can block the app (How to detect this? By using NodeJS perf hooks, check CPU profiles)

Things to try to avoid creating unnecessary promises

- Eslint rule `require-await`
- Avoid using libraries that assume every field resolve is async and construct many promises
- Write one-shot resolvers to for performance sensitive queries (return all the fields in one resolver)
- Avoid heavy nested async/await and keep functions simple. One should not load and use data at the same time. Keeping the goal of a function simple also makes it more testable and readable
