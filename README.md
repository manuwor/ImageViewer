# ImageViewer

ImageViewer is a library that enables a user to visualize an image in fullscreen. Besides the typical pinch and double tap to zoom, we also provide a vertical swipe to dismiss. Finally, we try to mimic the displacement of the image from its current container into fullscreen, being this feature its main selling point. In our context, you can imagine an image as part of an article and when it's taped, the image being animated into fullscreen.

#### Usage


```swift

let imageProvider: ImageProvider = ... 

let buttonConfiguration = ButtonStateAssets(normalImage:UIImage(named: "normalImage"), highlightedImage:UIImage(named: "highlightedImage"))
let configuration = ImageViewerConfiguration(imageSize: size, closeButtonAssets: buttonConfiguration)

let imageViewer = ImageViewer(imageProvider: imageProvider, configuration: configuration, displacedView: displacedView)

imageViewer.show()
```

* `imageProvier`: An object that conforms to the `ImageProvider protocol
* `configuration`: Contains information about the assets that will be used for the close button and the image to be displayed's size
* `displacedView`: The view that is about to be displayed in fullscreen. 


## License
ImageViewer is licensed under the MIT License, Version 2.0. [View the license file](LICENSE)

Copyright (c) 2015 MailOnline
