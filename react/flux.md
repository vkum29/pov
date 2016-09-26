# <a href='./../readme.md'>POV</a> > <a href='./readme.md'>React</a> > FLUX

FLUX is architectural guideline for client-side web application.

* It's common guideline used with React.
* It complements React's compossible view components by utilizing a unidirectional data flow.

## Pros

* Since it is a guideline we can start using it immediately.
* Easy to learn.

Flux pattern revolves around four things

## Actions - Event Directory

- Dispatches Events to the Dispatcher

> Uses Dispatcher.dispatch to notify dispatcher about which event occurred

## Components - React components

- Compossible views created using react.

> Made using React.createClass or React.component

## Stores - Data (collection)

- Listens to all dispatched events but acts on specific as needed

> Uses Dispatcher.register to start receiving events

- Class storing and updating data and inform's component whenever data changes

> Uses emit to inform component of state change

- Returns new instance only once and then existing instance (Singleton pattern)

## Dispatcher - Event publisher

- Transfer all requests to all its client.

> Creates a new instance of simple Flux dispatcher

Dispatcher is the only function made available in flux npm and that is all we need to convert our simple react views to flux based application.

## In action

<a href='https://github.com/vkum29/todo-react/tree/Flux'>To-do React app</a>

- Snapshot: <img src='https://github.com/vkum29/todo-react/blob/Flux/todo-react.png' width=200 height=200/>
