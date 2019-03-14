# xs3p XSD documentation generator

This stylesheet transforms XSD (XML Schema Definition) files into 
human-readable documentation in HTML format.

Features:
 - [Bootstrap](https://getbootstrap.com "Bootstrap homepage") HTML toolkit
 - Output of UTF-8 encoded files
 - Output of HTML5
 - [Markdown](https://daringfireball.net/projects/markdown/ "Markdown homepage")
   formatting support in `<documentation>` elements, powered by
   [markdown-it](https://github.com/markdown-it/markdown-it "markdown-it homepage")

## Usage

1. Add the following definition to your XSD file immediately following the 
   `<?xml version="1.0" encoding="UTF-8"?>` or similar element:
   ```xml
   <?xml-stylesheet type="text/xsl" href="xs3p.xsl"?>
   ```
2. In your XSD, adjust the `xs3p.xsl` file location to point to the XSL 
   file in your target environment (filesystem or HTTP).
3. Open the XSD in a browser that permits accessing data in the local 
   filesystem (e.g. Firefox) or place both files on an HTTP server and 
   access the XSD via HTTP.

### Known issues

 * There is currently no way to inline the Bootstrap and jQuery sources, thus
   those files must be fetched when viewing the documentation. Their URLs can
   be set, though, so you could serve them locally if offline viewing is a
   requirement.
