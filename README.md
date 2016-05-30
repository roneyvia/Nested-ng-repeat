# Nested-ng-repeat

```
<script type="text/javascript" ng:autobind src="http://code.angularjs.org/0.9.18/angular-0.9.18.js"></script>

<ul ng:controller="Cntl">
    <li ng:repeat="item in data">
        {{item.name}} has children:
        <ul>
            <li ng:repeat="child in item.children">{{child.name}} has grant-children: 
                <ul><li ng:repeat="gch in child.children">{{gch.name}}</li></ul>
            </li>
        </ul>
    </li>
</ul>
```

```javascript
function Cntl() {
    this.data = [{
        name: '1',
        children: [{
            name: '11',
            children: [{
                name: '111'}, {
                name: '112'}]}, {
            name: '12',
            children: [{
                name: '121'}, {
                name: '122'}]}]}, {
        name: '2',
        children: [{
            name: '21'}, {
            name: '22'}]}];
}
```
