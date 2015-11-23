React Packery Component
=======================

[![npm version](https://badge.fury.io/js/react-packery-component.svg)](http://badge.fury.io/js/react-packery-component)

#### Introduction:
A [React.js](https://facebook.github.io/react/) [Packery](http://packery.metafizzy.co/) component. (Also available as a [mixin](https://github.com/eiriklv/react-packery-mixin) if needed)

#### Support
React >= 0.14.x

#### Live demo:
[hearsay.me](http://www.hearsay.me)

#### Usage:

* The component bundles Packery, so no additional dependencies needed!
* You can optionally include Packery as a script tag if there should be any reason for doing so:
`<script src='//cdnjs.cloudflare.com/ajax/libs/packery/1.3.0/packery.pkgd.min.js' />`

* To use the component just require the module and inject `React`
* Example code:

```js
var React = require('react');
var Packery = require('react-packery-component')(React);

var packeryOptions = {
    transitionDuration: 0
};

var Gallery = React.createClass({
    render: function () {
        var childElements = this.props.elements.map(function(element){
           return (
                <li className="image-element-class">
                    <img src={element.src} />
                </li>
            );
        });

        return (
            <Packery
                className={'my-gallery-class'} // default ''
                elementType={'ul'} // default 'div'
                options={packeryOptions} // default {}
                disableImagesLoaded={false} // default false
            >
                {childElements}
            </Packery>
        );
    }
});

module.exports = Gallery;
```
