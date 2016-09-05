# EDM Boilerplate

- Set "Height" and "Width" on all TD's that have a fixed height and width
- All links must have the `target="_blank"`
- All images must have the `alt` attribute, even if it is empty
- To get images to display as a block in Outlook 365 you must wrap the `<img />` in a `<div>`, as it strips out `style="display: block;"` from all images
- To remove the blue border around images that are links use the following:

```
<div>
    <a href="http://example.com" target="_blank">
        <img border="0" height="25" style="display: block;" src="img/image.jpg" width="25" />
    </a>
</div>
```

- If you just need an image without a link around it use the following:

```
<div>
    <img height="25" src="img/image.jpg" style="display: block;" width="79" />
</div>
```

- All use of colours must be in full hex `#xxxxxx` not shorthand `#xxx`
- Do not use a "spacer.gif", if you need a blank `<td>` use the following:

```
<tr>
    <td height="desiredHeight" style="line-height: 1px; font-size: 1px;" width="desiredWidth"></td>
</tr>
```

- To remove the blue links on iOS devices like (Today) use the following:
```
a[x-apple-data-detectors] {
    color: inherit !important;
    text-decoration: none !important;
    font-size: inherit !important;
    font-family: inherit !important;
    font-weight: inherit !important;
    line-height: inherit !important;
}
```

- To add hidden pre-text copy use the following:
```
<div style="color: #000000; display: none; font-family: Arial; font-size: 1 px; line-height: 1 px; max-height: 0 px; max-width: 0 px; mso-hide: all; opacity: 0; overflow: hidden;">
    Put your text here
</div>
```