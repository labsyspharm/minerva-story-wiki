---
layout: home
---

Use Minerva Author to view your high-resolution multichannel images and narations with Minerva Story.

## Minerva Story

Minerva Story is a javascript web application based on [Openseadragon](https://openseadragon.github.io/). In addition to the navigation of large zoomable tiled images provided by Openseadragon, Minerva Story allows the display of text and figures that correspond to specific views of the image. The series of annotated image waypoints defines a story that guides users through a large image with many features otherwise noticable only to experts.

Minerva Story is designed for large-scale microscopy images. It is specifically targeted towards multichannel microsocpy images where there are more image channels than can be rendered simultaneously to the screen. Each point in a story corresponds to a rendered group of channels overlaid with one or more segmentation masks.

The application runs only on client-side javascript in a web browser. The code is built as a jekyll web application to allow convenient binding of the configuration files and serving from github pages. The images must be served from an external web host such as a public bucket on AWS S3. 

## Minerva Author

TODO
