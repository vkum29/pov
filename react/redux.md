# <a href='./../readme.md'>POV</a> > <a href='./readme.md'>React</a> > REDUX

REDUX is another pattern to create application using React.

Redux uses immutable javascript to provide non modified state. Idea is never to modify existing state but to always create new state representing current form. This becomes more fruitful in application where one needs to quickly switch between various state of application.

* It's a commonly used guideline for React.

## Pros

* Scalable for large application where history of application state is needed.

## Application

* TO be applied in application where we need stack of current and previous state of application.

Redux application components

## Action - Event Directory ~ similar to FLUX

- These events are sent to reducers for handling
- Action are triggered mostly from Components

## Reducers - State creator

- Handles actions
- Creates new data to represent state
- Forward this new data to store.
- In flux reducers doesn't exist and store does this job too.
- There is main reducer which simply dispatches events to each reducers creating new state.

> CombineReducer from redux package is used to combine various reducers of application

## Stores - Data (collection) ~ Similar to FLUX

- Stores the data representing the state of application
- Informs Providers of state change.
- In flux state changes are forwarded to React Components as we don't have providers.

> createStore from redux package is used to create a store from combined reducer.

## Providers - Component Wrapper

- They take the state from stores and passes it to React Components as props
- This is allowed to let component not directly use the store but have it as props so there is one point of management.

> Provider from react-redux package are used to add wrapper around application component and pass state as props from store.

## Components - View manager ~ Similar to FLUX

Components are properly categorized into smart component and dumb component

> Component from React package is used to create them.

### Smart Component

- Knows about framework and how to interact with it.
- Stores the data in its state for manipulation and forwards same to dumb components.

> Uses connect from redux-react package to grab props provided by provider and get state from it
> bindActionCreators from redux package is used to add actions to the component

### Dumb Component

- Takes a format of data and works on it and does not know which framework is being used.
- Works purely on props passed to it.

## In action

<a href='https://github.com/vkum29/todo-list-react/blob/redux'>To-do React app</a>

- Snapshot: <img src='https://github.com/vkum29/todo-list-react/blob/redux/app-snapshot.png' width=200 height=200/>
