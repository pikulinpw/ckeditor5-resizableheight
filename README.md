# CKEditor 5 ResizableHeight Plugin

Optimize your CKEditor 5 editing space with the ResizableHeight plugin. This plugin adds the ability to set the height of the editor and also change its size. Adds the ability to resize.
This plugin is compatible with various browsers including Chrome, Firefox, Safari, Edge and Internet Explorer, among others. It supports both the latest and older versions of these browsers and is optimized for devices such as iPhone, iPad, Android devices and desktop computers.

![ResizableHeight Plugin Screenshot](screenshot.png)

## Support the Author

If you find this plugin useful, consider supporting the author to create and maintain more open-source projects. Every contribution, however big or small, is very valuable.

[![Support with PayPal](https://img.shields.io/badge/Support-PayPal-blue.svg)](https://www.paypal.com/donate/?hosted_button_id=CY8NAWG5PKTC2)

## Prerequisites

Before you begin, ensure you have the following dependencies installed:

- [CKEditor 5 Core](https://www.npmjs.com/package/@ckeditor/ckeditor5-core)

Install them using npm:

```bash
npm install --save @ckeditor/ckeditor5-core
```

## Features

- Dynamically adjust the height of the CKEditor instance for custom editing.
- Adds the ability to resize the editor.
- Set specific height options or let the plugin determine the height based on the content.
- Seamless integration with CKEditor 5.

## Installation

1. **Using npm**:

   ```bash
   npm install @pikulinpw/ckeditor5-resizableheight
   ```

2. **Manual Installation**:

    - Clone or download this repository.
    - Add it to your CKEditor 5 build using the standard Webpack module imports.

## Usage

1. Add `'ResizableHeight'` to your editor's plugin list:

```javascript
import ResizableHeight from '@pikulinpw/ckeditor5-resizableheight';

ClassicEditor
    .create(document.querySelector('#editor'), {
        plugins: [ ..., ResizableHeight, ...],
        toolbar: [ ..., ...]
    })
    .then(editor => {
        console.log(editor);
    })
    .catch(error => {
        console.error(error.stack);
    });
```

## Configuration

The ResizableHeight plugin provides several configuration options to customize the editor's behavior. You can specify these options either in the CKEditor configuration object or directly through HTML attributes on the editor's element.

### Using CKEditor Configuration:

- `resize`: A boolean value that determines whether the editor should be resizable. Default is `true`.
- `height`: Specifies the initial height of the editor. It can be any valid CSS height value.
- `minHeight`: Specifies the minimum height to which the editor can be resized. It can be any valid CSS height value.
- `maxHeight`: Specifies the maximum height to which the editor can be resized. It can be any valid CSS height value.

```javascript
import ResizableHeight from '@pikulinpw/ckeditor5-resizableheight';

ClassicEditor
    .create(document.querySelector('#editor'), {
        plugins: [ ..., ResizableHeight, ...],
        ResizableHeight: {
            resize: false,
            height: '500px',
            minHeight: '100px',
            maxHeight: '1000px'
        }
    })
    .then(editor => {
        console.log(editor);
    })
    .catch(error => {
        console.error(error.stack);
    });
```

### Using HTML Attributes:

You can also set the height, minimum height, and maximum height using the `data-height`, `data-minheight`, and `data-maxheight` attributes respectively on the editor's HTML element:

```html
<div id="editor" data-height="500px" data-minheight="100px" data-maxheight="1000px">...</div>
```

By using these attributes, you can define the height and its constraints directly in the HTML, without modifying the JavaScript configuration.

## Customization

You can customize the appearance and behavior of the ResizableHeight plugin by tweaking the source code. All the necessary files (including styles) are available in the source code.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE.md) file for details.

## Feedback and Contributions

Feedback, bug reports, and pull requests are welcome. Feel free to [open an issue](https://github.com/pikulinpw/ckeditor5-resizableheight/issues) or submit a pull request if you have something to contribute.