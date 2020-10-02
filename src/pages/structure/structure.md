---
title: Structure
description: This explains the structure of a site made with 11ty
layout: base
permalink: /structure/
eleventyNavigation:
  key: Structure
---
# {{title}}

As mentioned previously, 11ty supports a plethora of different templating languages, which are the basis of your site when using 11ty. The key to 11ty, is that it will find any file written in a supported templating language and converts **all** of them into HTML.

### _now we get into the fun stuff_

When using 11ty, there is a clear division between source content and static HTML site files. 11ty will locate the content for your site, written in any of the supported templating languages, then convert it into HTML and place it into the `_site` directory. Within the `_site` directory, there is an exact clone of the directory structure where all of the source files lived previously. This `_site` directory is key, because this is the directory that includes the HTML files needed to power a website. The `_site` directory can be zipped and uploaded to a website hosting platform.

These HTML files are generated through a process that 11ty calls **the eleventy data cascade** The data cascade dictates the order of priority for sources of layout and style data for the static HTML files. While extremely technical, the cascade basically begins by applying global data to the template files, and then overwrites these data files as it moves deeper into the directory. Data files with the same name and same directory as the templating files are given the highest priority.

Lastly, the YAML front matter in each templating file is applied, which overwrites values further up in the data cascade. This is helpful for applying specific properties, such as a permalink, to individual files. 

When a website goes live, the folder structure that contains the markdown files transfers directly to the generated static HTML files. So, for example, if a particular markdown file is located in `/src/welcome` then the subsequent HTML file will appear in the `_site/src/welcome` folder.

One caveat to 11ty is that it does not automatically copy non-supported file types (anything other than files written in the supported templating languages) into the `_site` directory. In order to request that these files are copied into the `_site` directory, use the `--formats =` flag on the command line to specify certain file types. 

