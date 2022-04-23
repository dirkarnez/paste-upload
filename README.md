paste-upload
============
### TODO
- [ ] Make it a chrome plugin

### Shortcut
```javascript
(function(){
  const inputFiles = Array.from(document.getElementsByTagName("input")).filter(i => i.type == "file");
  if (inputFiles.length > 1) {
    alert("More than one file input");
    return;
  }
  window.addEventListener('paste', e => {
    inputFiles[0].files = e.clipboardData.files;
  });
})();
```
