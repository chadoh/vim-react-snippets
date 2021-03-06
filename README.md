# Vim React Snippets

A Vim snippet library for React in ES6. You may also want to check out [vim-es2015-snippets](https://github.com/epilande/vim-es2015-snippets).

Requires [UltiSnips](https://github.com/SirVer/ultisnips).

![vim-react-snippets](https://i.imgur.com/MXdHJRN.gif)

This is a permanent fork of [epilande/vim-react-snippets](https://github.com/epilande/vim-react-snippets), tweaked to fit my (@chadoh's) preferences. Some changes from @epilande's version:

* No semicolons at ends of lines
* No empty constructor
* No `function` keyword
* No `styles` import

## Installation

Using [vim-plug](https://github.com/junegunn/vim-plug):

```vim
" ES2015 code snippets (Optional)
Plug 'chadoh/vim-es2015-snippets'

" React code snippets
Plug 'chadoh/vim-react-snippets'

" Ultisnips
Plug 'SirVer/ultisnips'

" Trigger configuration (Optional)
" let g:UltiSnipsExpandTrigger="<C-l>"
```

## Usage
In a JavaScript or JSX file, type a trigger name while in Insert mode, then press Ultisnips trigger key. In my case I have it mapped to `<C-l>`.

For example, let's say we have `ListItem.js`

In Insert mode

```javascript
rfc<C-l>
```

Will expand to

```javascript
import React from 'react'
import PropTypes from 'prop-types'

const ListItem = ({  }) => {
  return (
    <div>
      
    </div>
  )
}

ListItem.defaultProps = {}

ListItem.propTypes = {
}

export default ListItem
```

Then use <kbd>ctrl</kbd>+<kbd>j</kbd> and <kbd>ctrl</kbd>+<kbd>k</kbd> to move between tabstops, as shown in the gif above. Learn more about this UltiSnips feature in [its README](https://github.com/SirVer/ultisnips).

Check out [`UltiSnips/javascript.snippets`](UltiSnips/javascript.snippets) to see all snippets.


## Snippets

#### Skeleton

| Trigger  | Content |
| -------: | ------- |
| `rrcc→`  | React Redux Class Component |
| `rcc→`   | React Class Component |
| `rfc→`   | React Functional Component |
| `rsc→`   | React Styled Component |
| `rsci→`   | React Styled Component Interpolation |


#### Lifecycle

| Trigger  | Content |
| -------: | ------- |
| `cwm→`   | `componentWillMount() {...}` |
| `cdm→`   | `componentDidMount() {...}` |
| `cwrp→`  | `componentWillReceiveProps(nextProps) {...}` |
| `scup→`  | `shouldComponentUpdate(nextProps, nextState) {...}` |
| `cwup→`  | `componentWillUpdate(nextProps, nextState) {...}` |
| `cdup→`  | `componentDidUpdate(prevProps, prevState) {...}` |
| `cwu→`   | `componentWillUnmount() {...}` |
| `ren→`   | `render() {...}` |


#### PropTypes

| Trigger    | Content |
| -------:   | ------- |
| `pt→`      | `propTypes {...}` |
| `pt.a→`    | `PropTypes.array` |
| `pt.b→`    | `PropTypes.bool` |
| `pt.f→`    | `PropTypes.func` |
| `pt.n→`    | `PropTypes.number` |
| `pt.o→`    | `PropTypes.object` |
| `pt.s→`    | `PropTypes.string` |
| `pt.no→`   | `PropTypes.node` |
| `pt.e→`    | `PropTypes.element` |
| `pt.io→`   | `PropTypes.instanceOf` |
| `pt.one→`  | `PropTypes.oneOf` |
| `pt.onet→` | `PropTypes.oneOfType (Union)` |
| `pt.ao→`   | `PropTypes.arrayOf (Instances)` |
| `pt.oo→`   | `PropTypes.objectOf` |
| `pt.sh→`   | `PropTypes.shape` |
| `ir→`      | `isRequired` |

#### Others

| Trigger  | Content |
| -------: | ------- |
| `props→` | `this.props` |
| `state→` | `this.state` |
| `set→`   | `this.setState(...)` |
| `dp→`    | `defaultProps {...}` |
| `cn→`    | `className` |
| `ref→`   | `ref` |
| `pp→`    | `${props => props}` |
