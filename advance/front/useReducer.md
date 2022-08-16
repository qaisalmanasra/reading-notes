# useReducer

An alternative to useState. Accepts a reducer of type (state, action) => newState, and returns the current state paired with a dispatch method. (If you’re familiar with Redux, you already know how this works.)

useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.

### Specifying the initial state


There are two different ways to initialize useReducer state. The simplest way is to pass the initial state as a second argument:

```
const [state, dispatch] = useReducer(
    reducer,
    {count: initialCount}
  );
```

### Lazy initialization


Also it is possible to create the initial state lazily. To do this, pass an init function as the third argument. The initial state will be set to init(initialArg).

It lets extract the logic for calculating the initial state outside the reducer. This is also handy for resetting the state later in response to an action:

```
function init(initialCount) {
  return {count: initialCount};
}

function reducer(state, action) {
  switch (action.type) {
    case 'increment':
      return {count: state.count + 1};
    case 'decrement':
      return {count: state.count - 1};
    case 'reset':
      return init(action.payload);
    default:
      throw new Error();
  }
}

function Counter({initialCount}) {
  const [state, dispatch] = useReducer(reducer, initialCount, init);
  return (
    <>
      Count: {state.count}
      <button
        onClick={() => dispatch({type: 'reset', payload: initialCount})}>
        Reset
      </button>
      <button onClick={() => dispatch({type: 'decrement'})}>-</button>
      <button onClick={() => dispatch({type: 'increment'})}>+</button>
    </>
  );
}
```

### Bailing out of a dispatch


If you return the same value from a Reducer Hook as the current state, React will bail out without rendering the children or firing effects. (React uses the Object.is comparison algorithm.)

Note that React may still need to render that specific component again before bailing out. That shouldn’t be a concern because React won’t unnecessarily go “deeper” into the tree. If you’re doing expensive calculations while rendering, you can optimize them with useMemo.

### **[useReducer hook](https://reactjs.org/docs/hooks-reference.html#usereducer)**
### **[Ultimate Guide to useReducer](https://blog.logrocket.com/react-usereducer-hook-ultimate-guide/)**