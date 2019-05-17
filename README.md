# Redactor Vue.js Component

Vue-redactor helps [Redactor](https://imperavi.com/redactor/) to work as a Vue.js component. The Redactor Vue component is under MIT license. 
However, to use this component, you should purchase a Redactor license. 

Please see [the buying page](https://imperavi.com/redactor/buy/) and [License Agreement](https://imperavi.com/redactor/license/).

## Compatibility

- Vue.js 2.x

## Intialization

### One Way Binding
```html
<html>
<head>
    <title>Redactor</title>
    <meta charset="utf-8">

    <!--css -->
    <link rel="stylesheet" href="/your-folder/redactor.css" />
</head>
<body>
    <div id="app">
        <Redactor v-model="content" :config="configOptions" />
        {{ content }}
    </div>

    <!-- redactor.js -->
    <script src="/your-folder/redactor.js"></script>

    <!-- vue.js -->
    <script src="https://cdn.jsdelivr.net/npm/vue"></script>

    <!-- redactor vue component -->
    <script src="/your-folder/vue-redactor.js"></script>

    <!-- app -->
    <script>
    new Vue({
        el: '#app',
        data() {
            return {
                content: '<h1>Hello and welcome</h1>',
                configOptions: {}
            }
        }
    });
    </script>
</body>
</html>
```

### Two Way Binding

```html
<html>
<head>
    <title>Redactor</title>
    <meta charset="utf-8">

    <!--css -->
    <link rel="stylesheet" href="/your-folder/redactor.css" />
</head>
<body>
    <div id="app">
        <Redactor v-model="content" placeholder="Type here..." :config="configOptions" />
        <textarea v-model="content"></textarea>
    </div>

    <!-- redactor.js -->
    <script src="/your-folder/redactor.js"></script>

    <!-- vue.js -->
    <script src="https://cdn.jsdelivr.net/npm/vue"></script>

    <!-- redactor vue component -->
    <script src="/your-folder/vue-redactor.js"></script>

    <!-- app -->
    <script>
    new Vue({
        el: '#app',
        data() {
            return {
                content: '<h1>Hello and welcome</h1>',
                configOptions: {}
            }
        }
    });
    </script>

</body>
</html>
```

### Call with options

```js
new Vue({
    el: '#app',
    data() {
        return {
            content: '<h1>Hello and welcome</h1>',
            configOptions: {
                plugins: ['table']
            }
        }
    }
});
```
