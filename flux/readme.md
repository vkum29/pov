# <a href='./../readme.md'>POV</a> > FLUX

FLUX is architectural guideline for client-side web application.

* It's common guideline used with React.
* It complements React's composable view components by utilizing a unidirectional data flow.

## Pros

* Since it is a guideline we can start using it immediately.
* Easy to learn.

Flux pattern revolves around four things

## Actions - Event Directory

- Dispatches Events to the Dispatcher

> Uses Dispatcher.dispatch to notify dispatcher about which event occured

## Components - React components

- Composable views created using react.

> Made using React.createClass or React.component

## Stores - Data (collection)

- Listens to all dispatched events but acts on specific as needed

> Uses Dispatcher.register to start reciving events

- Class storing and updating data and inform's component whenever data changes

> Uses emit to inform component of state change

- Returns new instance only once and then existing instance (Singleton pattern)

## Dispatcher - Event publisher

- Transfer all requests to all its client.

> Creates a new instance of simple Flux dispatcher

Dispatcher is the only function made avilable in flux npm and that is all we need to convert our simple react views to flux based application.

## In action

<a href='https://github.com/vkum29/todo-list-react'>To-do React app</a>

- Snapshot: <img src='https://github.com/vkum29/todo-list-react/blob/flux/app-snapshot.png' width=200 height=200/>

