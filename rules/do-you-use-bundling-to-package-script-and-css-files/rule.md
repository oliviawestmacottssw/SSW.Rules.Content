---
type: rule
title: Do you use Bundling to package script and css files?
uri: do-you-use-bundling-to-package-script-and-css-files
created: 2013-03-08T14:33:01.0000000Z
authors:
- id: 23
  title: Damian Brady

---

ASP.NET provides a great way to compress and package multiple script files or multiple css files.  Bundling multiple files together results in fewer requests from the client and smaller payloads which leads to much faster render times.
 
Rather than link to each script or css file individually, use bundling to group many together and get the advantages of minification and versioning out of the box.

[[greyBox]]
| ```
<link rel="stylesheet" href="~/Content/themes/base/jquery.ui.core.css" />
<link rel="stylesheet" href="~/Content/themes/base/jquery.ui.resizable.css" />
<link rel="stylesheet" href="~/Content/themes/base/jquery.ui.selectable.css" />
<link rel="stylesheet" href="~/Content/themes/base/jquery.ui.accordion.css" />
<link rel="stylesheet" href="~/Content/themes/base/jquery.ui.autocomplete.css" />
<link rel="stylesheet" href="~/Content/themes/base/jquery.ui.button.css" />
<link rel="stylesheet" href="~/Content/themes/base/jquery.ui.dialog.css" />
<link rel="stylesheet" href="~/Content/themes/base/jquery.ui.slider.css" />
<link rel="stylesheet" href="~/Content/themes/base/jquery.ui.tabs.css" />
<link rel="stylesheet" href="~/Content/themes/base/jquery.ui.datepicker.css" />
<link rel="stylesheet" href="~/Content/themes/base/jquery.ui.progressbar.css" />
<link rel="stylesheet" href="~/Content/themes/base/jquery.ui.theme.css" />
```


Figure: Bad Example – each reference will be downloaded separately and won’t be compressed
[[greyBox]]
| ```
Configuration:
public static void RegisterBundles(BundleCollection bundles)
{
        bundles.Add(new StyleBundle("~/Content/themes/base/css").Include(
                "~/Content/themes/base/jquery.ui.core.css",
                "~/Content/themes/base/jquery.ui.resizable.css",
                "~/Content/themes/base/jquery.ui.selectable.css",
                "~/Content/themes/base/jquery.ui.accordion.css",
                "~/Content/themes/base/jquery.ui.autocomplete.css",
                "~/Content/themes/base/jquery.ui.button.css",
                "~/Content/themes/base/jquery.ui.dialog.css",
                "~/Content/themes/base/jquery.ui.slider.css",
                "~/Content/themes/base/jquery.ui.tabs.css",
                "~/Content/themes/base/jquery.ui.datepicker.css",
                "~/Content/themes/base/jquery.ui.progressbar.css",
                "~/Content/themes/base/jquery.ui.theme.css"));
}

View:
@Styles.Render("~/Content/themes/base/css")
```


Figure: Good Example – Define a bundle and render it in the view for maximum performance
