A slightly modified version of https://www.npmjs.com/package/@rbxts/roact-rodux that adds a third argument to the connect function which returns the actions that happened in order to mutate the state:

```
interface StoreChangedSignal<S> {
    connect(
      handler: (newState: Readonly<S>, oldState: Readonly<S>, actions: Array<AnyAction>) => void,
    ): void;
  }
```