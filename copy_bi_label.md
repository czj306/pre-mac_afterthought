## 数据库复制

```javascript
function fallbackCopyTextToClipboard(text) {
  var textArea = document.createElement("textarea");
  textArea.value = text;
  // Avoid scrolling to bottom
  textArea.style.top = "0";
  textArea.style.left = "0";
  textArea.style.position = "fixed";
  document.body.appendChild(textArea);
  textArea.focus();
  textArea.select();
  try {
    var successful = document.execCommand('copy');
    var msg = successful ? 'successful' : 'unsuccessful';
    console.log('Fallback: Copying text command was ' + msg);
  } catch (err) {
    console.error('Fallback: Oops, unable to copy', err);
  }
  document.body.removeChild(textArea);
}

var button = document.createElement("button")
button.innerText = "文案复制"
button.addEventListener('click', (event) => {
  event.preventDefault();
  event.stopPropagation();
  let li = document.getElementsByClassName('FieldsRow__fieldsRowText__2wMe9')
  let iis = Object.keys(li).map(e => li[e].innerText).filter(e => e.indexOf('迁移的数据')===-1).sort((a, b) => a.localeCompare(b))
  let html = iis.join('\n')
  fallbackCopyTextToClipboard(html)

})

var b = document.getElementsByClassName('Sections__verticalLayout__2t4eC Sections__extraPadding__2cHWd')
button.setAttribute("class","ant-btn ant-btn-primary ant-btn-sm")
button.setAttribute("style", "position: absolute;right: 4rem;")

b[0].appendChild(button)
```



## 视图编辑复制

```javascript
function fallbackCopyTextToClipboard(text) {
  var textArea = document.createElement("textarea");
  textArea.value = text;

  // Avoid scrolling to bottom
  textArea.style.top = "0";
  textArea.style.left = "0";
  textArea.style.position = "fixed";

  document.body.appendChild(textArea);
  textArea.focus();
  textArea.select();

  try {
    var successful = document.execCommand('copy');
    var msg = successful ? 'successful' : 'unsuccessful';
    console.log('Fallback: Copying text command was ' + msg);
  } catch (err) {
    console.error('Fallback: Oops, unable to copy', err);
  }

  document.body.removeChild(textArea);
}

var button = document.createElement("button")
button.innerText = "文案复制"
button.addEventListener('click', (event) => {
  event.preventDefault();
  event.stopPropagation();
  let not = ['迁移的数据 (计数)', '度量值', '度量名称']
  let li = document.getElementsByClassName('tab-schema-field-label tab-unselectable')
  let iis = Object.keys(li).map(e => li[e].innerHTML).filter(e => !not.includes(e)).sort((a, b) => a.localeCompare(b))
  let html = iis.join('\n')
  fallbackCopyTextToClipboard(html)

})

var b = document.getElementsByClassName('tabAuthToolbarSpacerArea')
button.setAttribute("class","ant-btn ant-btn-primary ant-btn-sm")
button.setAttribute("style", "position: absolute;right: 4rem;")
b[0].appendChild(button)
```

