# React.js

Based on React 15.3

## Component

```js
var MyComponent = React.createClass({
  render: function(){
    // return a DOM element.
  }
});
```

If component needs to have a `render` function only, use a functional component.
```js
var MyComponent = function(props){
  // return a DOM element.
};
```

## Element

Javascript:
```js
React.createElement('p', {className: 'my-label'}, 'Hello World');
```

JSX:
```jsx
<p className='my-label'>Hello World</p>
```

## Mounting

```jsx
ReactDOM.render(
  <MyComponent />, // React.createElement(MyComponent, null)
  document.getElementById('container')
);
```

## Composition

```jsx
// class content omitted
var Header = React.createClass({}),
    Body = React.createClass({});

var Panel = React.createClass({
  render: function(){
    return (
      <div className='panel'>
        <Header />
        <Body />
      </div>
    );
  }
});
```

## Props

```jsx
var Label = React.createClass({
  render: function(){
    return (
      <span className='label'>{this.props.text}</span>
    );
  }
});

ReactDOM.render(
  <Label text='Hello World'/>,
  document.getElementById('container')
);
```

### PropTypes

```jsx
var MyTextField = React.createClass({
  
  propTypes: {
    value: React.PropTypes.string.isRequired,
    placeholder: React.PropTypes.string,
    onChange: React.PropTypes.func
  }
  
});
```

### Defaults

```jsx
React.createClass({
  
  getDefaultProps: function(){
    return {
      value: 'Default Value'
    };
  }
  
});
```

### `this.props.children`

```jsx
var SmallBox = React.createClass({
  render: function(){
    return (
      <div className='small-box'>
        {this.props.children}
      </div>
    );
  }
});

var BigBox = React.createClass({
  render: function(){
    return (
      <div className='big-box'>
        <SmallBox>
          <p>I'm accessible through this.props.children</p>
        </SmallBox>
      </div>
    );
  }
});
```

## Events

```jsx
var Link = React.createClass({
  render: function(){
    return (
      <a onClick={ this.handleClick }>Click Me!</a>
    );
  },
  
  handleClick: function(e){
    e.preventDefault();
    alert('Clicked!');
  }
});
```

## States

```jsx
var Link = React.createClass({
  getInitialState: function(){
    return {clicked: false};
  },
  
  render: function(){
    var clickedClass = this.state.clicked ? 'highlight' : '';
    
    return (
      <a className={ clickedClass } onClick={ this.handleClick }>Click Me!</a>
    );
  },
  
  handleClick: function(e){
    e.preventDefault();
    this.setState({clicked: true});
  }
});
```
