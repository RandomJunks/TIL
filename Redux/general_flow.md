<!-- general flow of redux -->

## Control flow of Redux

__Redux has (always) a single store. (root-store)__

1. Whenever you want to replace the state in the store, you dispatch an action.

2. The action is caught by one or more reducers.

3. The reducer/s create a new state that combines the old state, and the dispatched action.

4. The store subscribers are notified that there is a new state.

## Roles of components/containers/actions/action creators/store in redux 

- __Store__ - holds the state, and when a new action arrives runs the dispatch -> middleware -> reducers pipeline, and notifies subscribers when the state is replaced by a new one.

- __Components__ - dumb view parts which are not aware of the state directly. Also known as presentational components.

- __Containers__ - pieces of the view that are aware of the state using react-redux. Also known as smart components, and higher order components

- __Actions__ - same as flux - command pattern with type and payload.

- __Action creators__ - DRY way of creating actions (not strictly necessary)



## Differences between redux, redux-thunk, and react-redux.

__redux__ : main library (independent from React)

__redux-thunk__: a redux middleware which helps you with async actions

__react-redux__: connects your redux store with ReactComponents









_resource(s):_
- https://stackoverflow.com/questions/38405571/what-are-differences-between-redux-react-redux-redux-thunk
