# angular-filer

A simple and reusable file load and save (JSON) service for AngularJS. Perfect for use in Cordova/Phonecap projects.

## Notes
* Promise based API.
* Serializes the data before saving it as JSON.
* Deserializes the file before resolving. 

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
The service provides 2 methods `load` and `save`.

### `load (filename)`
Loads `filename` from the filesystem, deserializes it and resolves the promise with the deserialized object.

### `save (obj, filename)`
Saves `obj` into `filename` in the filesystem. Will serialize (angular.toJson) `obj` before saving it.
