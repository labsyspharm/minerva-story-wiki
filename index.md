---
layout: home
---

Use Minerva Author to narrate high-resolution multichannel images to share with Minerva Story.

## Minerva Story

Minerva Story is a javascript web application based on [Openseadragon](https://openseadragon.github.io/). In addition to the navigation of large zoomable tiled images provided by Openseadragon, Minerva Story allows the display of text and figures that correspond to specific views of the image. The series of annotated image waypoints defines a story that guides users through a large image with many features otherwise noticable only to experts.

Minerva Story is designed for large-scale microscopy images. It is specifically targeted towards multichannel microsocpy images where there are more image channels than can be rendered simultaneously to the screen. Each point in a story corresponds to a rendered group of channels overlaid with one or more segmentation masks.

The application runs only as client-side javascript in a web browser. The code is built as a jekyll application to allow convenient binding of the configuration files and serving from github pages. The images must be served as a tiled image pyramid from an external web host such as a public bucket on AWS S3. 

## Minerva Author

Minerva Author is a javascript web application based on [Openseadragon](https://openseadragon.github.io/) that runs locally on your computer. Using a lightweight python (flask) backend, it opens an [OME TIFF](https://docs.openmicroscopy.org/ome-model/5.6.3/ome-tiff/) file in a viewer that allows you to group channels to render together with colors and ranges per channel. You can set the name of each channel as well as the name of each channel group.

Once you've set up renderable channel groups, you can begin to write the story. You can write a sequence of points in the story each with a name, a description, rectangular overlays, arrow overlays, and a specific view of a given channel group. Once you hit "save", the application will output a configuration file and tiled image pyramid compatible with Minerva Story.
