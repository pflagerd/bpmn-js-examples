## Usage

To get started copy the code below to a local file (e.g. hello-viewer.html):

```javascript
<html>
<head>
  <title>hello-viewer</title>
  <script src="https://unpkg.com/bpmn-js@8.2.0/dist/bpmn-viewer.development.js"></script>
</head>
<body>
  <script>
    let c = document.createElement('div');
    document.body.appendChild(c);

    let viewer = new BpmnJS({ container: c });

    fetch('https://cdn.staticaly.com/gh/bpmn-io/bpmn-js-examples/dfceecba/starter/diagram.bpmn')
            .then(response => response.text())
            .then(xml => viewer.importXML(xml));
    </script>
</html>
```

Now load the file using a browser (Chrome, Firefox, etc.) and you will see a BPMN diagram:

![1611957113924](../../bpmn-js/.md/README/1611957113924.png)

