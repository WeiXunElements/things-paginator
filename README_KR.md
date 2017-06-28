# things-paginator

## 화면이나 그리드에서 데이터의 페이지 추가용으로 사용되는 컴포넌트

Example:

```js
    // Add Paginator Element
    var paginator = document.createElement('things-paginator');
    paginator.id = 'paginator';
    paginator.limit = this.limit;
    paginator.currentPage = this.currentPage;
    paginator.totalCount = this.totalCount;
    paginator.pageStartIdx = this.pageStartIdx;
    paginator.pageEndIdx = this.pageEndIdx;
    this.$.paginator = paginator;

    var me = this;

    // Add Event Listener things-paginator's properties changed
    paginator.addEventListener("current-page-changed", function(ev) {
      me.currentPage = this.currentPage;
    });

    paginator.addEventListener("page-limit-changed", function(ev) {
      me.limit = ev.detail.limit;
    });

    paginator.addEventListener("total-page-changed", function(ev) {
      me.showPaginator = (me.paginatable) && (this.totalPage && this.totalPage >= 1);
    });

    paginator.addEventListener("page-start-idx-changed", function(ev) {
      me.pageStartIdx = this.pageStartIdx;
    });

    paginator.addEventListener("page-end-idx-changed", function(ev) {
      me.pageEndIdx = this.pageEndIdx;
    });

    // id가 paginator-container인 Element에 paginator 추가
    Polymer.dom(this.$['paginator-container']).appendChild(paginator);
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
`http://localhost:8080/components/things-paginator/`, where `things-paginator` is the name of the directory containing it.
