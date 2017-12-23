![example](https://user-images.githubusercontent.com/34774590/34322285-b211df28-e82b-11e7-9ba8-c418740f09ed.jpg)

# InputUploader

Use
------
First include in your HTML file the InputUploader project.
``` html
  <script type="text/javascript" src="path>/InputUploader/InputUploader.js"></script>
  <link rel="stylesheet" href="path/InputUploader/InputUploader.css" />  
  <script type="text/javascript" src="path/InputUploader/object-watch.js"></script>
  <script type="text/javascript" src="path/InputUploader/ImageResizer/ImageResizer.js"></script>
 ```
  
*if you want to use costume scrollbar design for -webkit- browsers add:*

``` html
    <link rel="stylesheet" href="path/InputUploader/scrollbar/Scrollbar.css" />  
```

Example
------ 
``` javascript
  var inpt = new InputUploader();
 ```
 *or with options passed*
 ``` javascript
  var inpt = new InputUploader({
      context: document.getElementById("container"),
      width: 300,
      height: 100,
      maxFiles: 5,
      resize: {maxHeight: 720, maxWidth: 1280},
      limitSize: '8mb',
   });
 ```
 
  Options
 ------
 | Option     | Type   | Description                                                                                |
 |------------|--------|--------------------------------------------------------------------------------------------|
 |context     |Element | The element to which the *InputUploader* should be appended.                               |
 |className   |String  | A class name to be added to the *InputUploader* for customizability.                       |
 |width       |int     | The *InputUploader* set width.                                                             |
 |height      |int     | The *InputUploader* set height.                                                            |
 |borderColor |String  | Set the color for the *InputUploader* outer border.                                        |
 |resize      |Object  | The options object for the *ImageResizer*. <br/>**false** for no resizing.                 |
 |maxFiles    |int     | The maximum number of files allowed.                                                       |
 |accept      |String  | Sets the *accept* attribute for the file selector.                                         |
 |label       |String  | HTML string to be set as the *file uploading tab* label.                                   |
 |limitSize   |String  | Set a total file size limit value as *size* + *Mb/M/Kb/K/B*. <br/> **false** for no limit  |
 |limitAlert  |Function| Callback function to be called when a over limit size alert should be fired.               |
