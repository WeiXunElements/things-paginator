# things-paginator


Example:

```html
      <template is="dom-bind">

        <mercury-paginator limit="15" items="{{items}}"></mercury-paginator>

        <div class="div-table">
            <div class="head-row">
                <div class="div-cell">Id</div>
                <div class="div-cell">Item name</div>
                <div class="div-cell">Description</div>
            </div>

            <template id="items" is="dom-repeat" items="{{items}}">
                <div class="div-row">
                    <div class="div-cell">{{item.id}}</div>
                    <div class="div-cell">{{item.name}}</div>
                    <div class="div-cell">{{item.description}}</div>
                </div>
            </template>
        </div>

      </template>
```

*****
</br></br>


## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install

## Playing With Your Element

If you wish to work on your element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polymer-cli

And you can run it via:

    polymer serve

Once running, you can preview your element at
`http://localhost:8080/components/things-alarm/`, where `things-alarm` is the name of the directory containing it.
