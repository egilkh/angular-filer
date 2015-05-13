# angular-filer
A simple and reusable file load and save (JSON) for AngularJS. Perfect for use in Cordova/Phonecap projects.

* Promise based.
* It takes the data and serializes it to JSON before writing. 
* It takes the file and de-serializes it into an object before resolving.

## Example

```javascript
angular.module('MahApp', ['eh'])
.controller(['ehFiler', 
  function (ehFiler) {
    ehFiler.load('mah-file.json')
    .then(function (obj) {
      // Use object.
    })
    .catch(function (err) {
      // Handle errors.
    });
  }]);
  ```
  
  ## API
