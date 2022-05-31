## Introduction
This is a modified version of the ML Kit Showcase Android app which is hosted in https://github.com/googlesamples/mlkit
Base on the quote, "DON'T reinvent the wheel" this source code is chosen to demonstrate how real time object detection and recognition works, as it is. 

The underlying custom model used is the TensorFlow Lite model, is trained to identify cereal brands.

This architecture is old and not compliant to the popular Clean Architecture principals. There is a WIP I initiated is hosted here https://github.com/prageek/Recognize

# ML Kit Vision Showcase App with Material Design

This app demonstrates how to build an end-to-end user experience with
[Google ML Kit APIs](https://developers.google.com/ml-kit/guides) and following the
[new Material for ML design guidelines](https://material.io/design/machine-learning/).

The goal of this app is to showcase the camera preview and perform following use case. The following use cases are covered:
* “cereal” brand search using the Object Detection & Tracking API - An end to end workflow for object detection and search using a custom TensorFlow Lite model


<img src="screenshots/live_odt.gif" width="256"/> 

## Steps to run the app

* Clone this repo locally
* Build and run it on an Android device

## How to use the app

This app supports Live Camera based object detection. In this case cereal brands.

### Live Camera scenario

It uses the camera preview as input and contains object detection & custom classification. There's also a Settings page to
allow you to configure several options:
- Camera
  - Preview Size - Specify the preview size of rear camera manually (Default size is chose appropriately based on screen size)
- Object detection
    - Enable Multiple Objects -- Enable multiple objects to be detected at once.
    - Enable classification -- Enable coarse classification

### Static Image scenario

During this scenario, the app will prompt the user to select an image from the “Image Picker” (gallery), detect objects in the selected image, and then perform visual search on those objects. There are well designed UI components (overlay dots, card carousel etc.) to indicate the detected objects and search results.

### Visual Search

Please note that the visual search functionality in this app will not work since there is no real search backend setup for this repository. However, it should be easy to hook up your  own search service (e.g. [Product Search](https://cloud.google.com/vision/product-search/docs)) by only replacing the [SearchEngine](https://github.com/googlesamples/mlkit/blob/master/android/material-showcase/app/src/main/java/com/google/mlkit/md/productsearch/SearchEngine.kt) class implementation.


## License
© Google, 2020. Licensed under an [Apache-2](./LICENSE) license.
