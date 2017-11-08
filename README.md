Forked from https://github.com/gitim/react-native-sortable-list.

I maintain this only for myself.

Please submit any patches upstream. Thanks!

---

## Sortable list view for react-native

### Installation
```bash
npm i @hawkrives/react-native-sortable-list
```

### Examples
- [Basic](https://github.com/gitim/react-native-sortable-list/tree/master/examples/Basic)


### API
#### Props
- **data** (Object) data source
- **order** (Array) an array of keys from data, the order of keys from the array will be used to initial rows order
- **style** (Object, Array)
- **contentContainerStyle** (Object, Array) these styles will be applied to the inner scroll view content container
- **sortingEnabled** (boolean) when false, rows are not sortable. The default value is true.
- **scrollEnabled** (boolean) when false, the content does not scrollable. The default value is true.<br /><br />
- **renderRow** (function)<br />
`({key, index, data, disabled, active}) => renderable`<br />
Takes a row key, row index, data entry from the data source and its statuses disabled, active and should return a renderable component to be rendered as the row.<br /><br />
- **onChangeOrder** (function)<br />
`(nextOrder) => void`<br />
Called when rows were reordered, takes an array of rows keys of the next rows order.
- **onActivateRow** (function)<br />
`(key) => void`<br />
Called when a row was activated (user long tapped).
- **onReleaseRow** (function)<br />
`(key) => void`<br />
Called when the active row was released.

#### Methods
- **scrollBy(dy?, animated?)** scrolls by a given y offset, either immediately or with a smooth animation
- **scrollTo(y?, animated?)** scrolls to a given y offset, either immediately or with a smooth animation
- **scrollToRowKey(key, animated?)** scrolls to a given row key, either immediately or with a smooth animation
