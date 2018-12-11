# quantum-form

Quickly and cleanly add React forms using Twitter Bootstrap for styling.  

At a glance
- Dependency free!
- ES6
- Style with Bootstrap CSS
- Use with React.js

## Usage

Import as you need.  

`import { Input } from "quantum-form";`

### Bootstrap

Use Twitter Bootstrap to get the full styling of quantum-form. The CSS should be imported some way or another, as it is using Bootstrap classNames.

### File Sample

```js
import React from "react";
import { Input } from "quantum-form";

export default class User extends React.Component{
  constructor(){
    super();
    this.state = {
      firstName: ""
    }
  }

  handleChange = e => {
    this.setState({
      [e.target.id]: e.target.value
    })
  }

  render() {
    return (
      <div>
        <Input text="First Name" id="firstName" placeholder="Enter name..." changeCallback={this.handleChange} />
        <Input text="Last Name" id="lastName" placeholder="Enter name..." changeCallback={this.handleChange} />
      </div>
    )
  }
}


```

## Components

### Input

| prop | type | description |
| --- | --- | --- |
| `title` | "string" | Label for the form field |
| `id` | string | Field name for this.state |
| `placeholder` | string | Placeholder text for the input field |
| `changeCallback` | function | Callback that references `onChange` function in parent |


```js
import { Input } from "quantum-form"

<Input id="firstName" title="First Name" placeholder="Enter name..." changeCallback={this.handleChange} />
```


### Select

| prop | type | description |
| --- | --- | --- |
| `title` | "string" | Label for the form field |
| `id` | string | Field name for this.state |
| `values` | array | Array like so: `["A", "B"]` |
| `changeCallback` | function | Callback that references `onChange` function in parent |

```js
import { Select } from "quantum-form";

<Select id="degreeType" title="Degree Type" values={["B.A.", "B.S."]} changeCallback={this.handleChange} />
```

### Start and End Date

| prop | type | description |
| --- | --- | --- |
| `changeCallback` | function | Callback that references `onChange` function in parent |

```js
import { StartAndEndDate } from "quantum-form";

this.state = {
  startDate: "",
  endDate: ""
};

<StartAndEndDate changeCallback={this.handleChange} />
```
