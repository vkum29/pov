# <a href='./../readme.md'>POV</a> > <a href='./readme.md'>React</a> > Practice Guide

Tips for writing React(version 0.15) code

- Break your app into small composable view

Eg.
  Heading
    TITLE (H1,H2 ETC TAG)
    SUB_TITLE(PARAGRAPH TEXT OR H2)
    LOGO(IMAGE)

- Organize dependent views (parent and children) in a single folder

Eg. Table data
    > Table
      > Head
      > Body
        > Row
        > Data

- Write with ES6, its easy and better

Current browser support is very nice
  chrome - 97%
  firefox - 92%
  IE-Edge(13/14) - 95%

Transpiler like Babel with 71% support for es6 can be used for older browsers like IE 11 or less and others

- React component name starts with uppercase this distinguishes html element(starting with lower case).

- Keep DATA in one place (Somethign like STORE mentioned in FLUX pattern)

- Try to minimize writing to scope and use dynamic calculations in ReactClass's render function.
  Code wrtten inside render always gets executed when component is render

Eg Temporary data manipulation etc

  export class AppComponent extends React.Component {
    constructor(){}
    ...
    render() {
      /* Get only uncompleted todo items*/
      Todos = this.filter((item)=>{
        return !item.isComplete;
      });
      
      /* Get markup*/
      Todos.map((item)=>{
        return <li className="todo-item">item.desc</li>
      });
      return (
        <ul>
          {Todos}
        </ul>
      )
    }
  }

- Use LifeCycle Hooks like componentWillMount to attach/bind events and componentWillUnMount to deattach events if any

- bind this to function in constructor once this will avoid binding it every where
eg
  export class AppComponent extends React.Component {
    constructor(){
      ...
      this.getAll = this.getAll.bind(this)
      ...
    }
    ...
    getAll() {}
    ...
  }

- We can use shouldComponentUpdate to hook decision for dom rendering returning false will not render any changes in state to DOM.
