# "Static" Directory

The "static" directory can be used to store any non-xml local content, for example images and prefabricated PDF. You may use subdirectories.

## Images in PDF
On inserting images into PDF, this directory serves as the local root path to the XSLT processor. So you can either use an absolute path (URL) or a relative (local) path that refers to this directory.

## Images in Email Body

If the email-body has a content type like text/html; charset=utf-8 then it may include tags such as `<img src="cid:foo/bar.jpg">`. The tag is most commonly an <img> but can be any tag.
The system then searches in the static directory for any file with that path. The file is included with the image, as a “related” multi-part part, meaning the file is available to the HTML document when its rendered in the email client.

## Return Static Files
Instead of returning content from xslt transformation, you may also return "prefabricated" content from this directory. The syntax `<response-from-static filename="path-to-file"/>` returns a file from this directory.