[![Published on npm](https://img.shields.io/badge/npm-published-blue.svg)](https://www.npmjs.com/package/@telecomsante/pdf-viewer)
![](https://img.shields.io/badge/polymer-3.x-blue.svg)
![npm package](https://img.shields.io/badge/npm%20package-3.0.0.pre.1-green.svg)
![](https://img.shields.io/badge/licence-ISC-brightgreen.svg)


# &lt;pdf-viewer&gt;

`pdf-viewer` is a simple viewer, without any decoration, based on the [Mozilla's pdfjs library](https://github.com/mozilla/pdfjs-dist). Buttons have to be created by the parent page or component.

the component is written using es6 syntax, and polymer 2.x.

> __Nota :__ the pdfjs library uses XMLHttpRequest to load the pdf documents. So, you may encountered CORS problem, if you try to load a document from another origin. A solution could be to use a proxy to serve your documents, you could take advantage to use for example the project [CORS Anywhere](https://github.com/Rob--W/cors-anywhere).

Features
 - Next/Previous page
 - Zoom
 - Polymer 3.x
 - Dynamically change document without page reloading
 - Works in IE11, IOS, Android (chrome)
 - Works in Chrome, Firefox, Safari

![][demo]

Basic usage :

```html
<pdf-viewer   
  src="https://www.w3.org/TR/1998/REC-html40-19980424/html40.pdf"
  initial-zoom="fit-width",
  mode="double",
  page="5"></pdf-viewer>
```

# Using in polymer app

the file `bower_components/pdfjs-dist/build/pdf.worker.min.js` must be added to `extradependencies` section into the `polymer.json` file.

If for some reasons, bower components are installed in another folder, be aware to pass as attribute `PDFJS_workerSrc` the full path to the `pdf.worker.min.js` file.

The component is licensed under the [ISC License](LICENSE.md)

[demo]: https://raw.githubusercontent.com/telecomsante/pdf-viewer/HEAD/demo.gif