# Android-Studio-live-template

### Introduce
&emsp;Live Template of Android Studio for some famous lib
&emsp;Welcome to replenish

### Support Lib

- RxJava
- Glide

### Install


&emsp;Live templates are stored in the following location:
- Windows: <your home directory>\.<product name><version number>\config\templates

- Linux: ~/.<product name><version number>/config/templates

- OS X: ~/Library/Preferences/<product name><version number>/templates

&emsp;Once you found it, copy xml file in which template that you like into it


### RxJava.xml
> 助记法则：动词+名词
> 代码片段会自动进行缩进，并且导入需要的包名并且去掉类名前的包名。

#### List
- `cob`: "create the Observable by Observable.create" 
- `job`: "create observable by Observable.just"
- `fob`: "create observable by Observable.from"
- `csub`: "create the Subscriber"
- `mp1`: "map with func1"
- `ft1`: "filter with func1"
- `fmp1`: "flatmap with func1"
- `na0`: "create an Action0 object"
- `na1`: "create an Action1 object"
- `obmain`: "observeOn(AndroidSchedulers.mainThread())"
- `subio`: "subscribeOn(Schedulers.io())"

#### Detail
- `cob`: "create the Observable by Observable.create" 

``` java
rx.Observable<$T$> $variable$ = rx.Observable.create(
    new rx.Observable.OnSubscribe<$T$>() {
        @Override
        public void call(rx.Subscriber<? super $T$> sub) {
            $start$
            sub.onCompleted();
        }
    }
);
```
- `job`: "create observable by Observable.just"

``` java
rx.Observable<$T$> observable = rx.Observable.just($input$);
```
- `fob`: "create observable by Observable.from"

``` java
rx.Observable observable = rx.Observable.from($input$);
```
- `csub`: "create the Subscriber"

```java
Subscriber<$T$> $variable$ = new Subscriber<$T$>() {
    @Override
    public void onNext($T$ s) {
        
    }

    @Override
    public void onCompleted() {
        
    }

    @Override
    public void onError(Throwable e) {
        
    }
};
```
- `mp1`: "map with func1"

``` java
 .map(new rx.functions.Func1<$T1$, $T2$>() {
        @Override
        public $T1$ call($T2$ param) {
            
        }
    })
```
- `ft1`: "filter with func1"
```java
.filter(new rx.functions.Func1<$T$, Boolean>() {
        @Override
        public Boolean call($T$ param) {
            
            return true;
        }
    })
```
- `fmp1`: "flatmap with func1"
``` java
.flatMap(new rx.functions.Func1<$T1$, rx.Observable<$T2$>>() {
        @Override
        public rx.Observable<$T2$> call($T1$ token) {
            $input$
        }
    })
```
- `na0`: "create an Action0 object"
``` java
new rx.functions.Action0() {
    @Override
    public void call() {
        $input$
    }
};
```
- `na1`: "create an Action1 object"
``` java
new rx.functions.Action1<$T$>() {
    @Override
    public void call($T$ param) {
        $input$
    }
};
```
- `obmain`: "observeOn(AndroidSchedulers.mainThread())"
``` java
.observeOn(rx.android.schedulers.AndroidSchedulers.mainThread())
```
- `subio`: "subscribeOn(Schedulers.io())"
``` java
.subscribeOn(rx.Schedulers.io())
```

### Glide

- `glideinto`: "Glide.with().load("").into();"

### AndroidXMLExtend

- `txall`: "android:text ,android:text_color and android:text_size" 
- `txc`: "android:text_color"
- `txs`: "android:text_size"
- `txsc`: "android:text_size and android:text_color"
