# AnnouncementSlidesGenerator

This proposal shows how to build homogen appearing announcement slides as png-file-format output from [Markdown](https://en.wikipedia.org/wiki/Markdown).


## Marp
Install Marp either as VS-Code plugin or [cli tool](https://github.com/marp-team/marp-cli)
See also [Reference](https://marpit.marp.app/markdown) for general usage.

## Slides
Each slide consists of title picture and the key-points of the announcement. 
End of slide is indicated by `---` after the data

``` md
# Title of Announcement
![bg right:66%](https://fakeimg.pl/1280x720/0288d1/fff/?text=UriToPicture)

📅 when, (01.01.2000 10:00)
📍 where 
🔘 Optional notes

---
```

The two blocks at the beginning of the file define the style and specify some style adaptions
``` md
---
theme: default
...
---
<style> 
p { ... }
</style>

```

## Call Arguments
Call CLI with `marp --allow-local-files --images png AnnouncementSlides.md` in order to generate png-Slides from Markdown-file. 
The slides will be placed at the location of the Markdown-file.
