# things-paginator

## 이는 화면이나 그리드에서 데이터 페이지를 추가하는 용도로 사용되는 컴포넌트이다.

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

    // id가 paginator-container인 element에 paginator 추가
    Polymer.dom(this.$['paginator-container']).appendChild(paginator);
```

*****
</br></br>


## Dependencies

element의 종속성은 [Bower](http://bower.io/)를 통해 관리되며, 아래의 방법을 통해 설치할 수 있다.

    npm install -g bower

다음, element의 종속성을 다운로드한다.

    bower install

## Playing With Your Element

element를 독립적으로 처리하려면 [Polyserve](https://github.com/PolymerLabs/polyserve)를 사용하여 element의 bower 의존성을 유지하도록 하며, 이는 아래의 방법을 통해 설치할 수 있다.

    npm install -g polymer-cli

그리고, 아래의 방법을 통해 실행할 수 있다.

    polymer serve

element를 실행한 경우, `things-paginator`이 디렉토리 이름으로 포함되어 있는 `http://localhost:8080/components/things-paginator/`를 통해 이를 미리 확인할 수 있다. 
