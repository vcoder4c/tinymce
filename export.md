# Purpose
I want to customize AdminTextAreaWidget on Django to support TinyMCE.

# How
TinyMCE support bundle all what we need into the same js file, so it will be easy to integrate.

At this moment, I will try to integrate as much as possible due to I'm still not sure yet. So, what I will bundle as below:
* Theme: silver - this is newest from TinyMCE 5.x
* Plugins: advlist,anchor,autolink,autoresize,autosave,bbcode,charmap,code,codesample,colorpicker,contextmenu,directionality,fullpage,fullscreen,hr,image,imagetools,insertdatetime,legacyoutput,link,lists,media,nonbreaking,pagebreak,paste,preview,quickbars,save,searchreplace,table,tabfocus,template,textcolor,textpattern,toc,visualblocks,visualchars,wordcount

So, final command for bundle will be:
```
grunt bundle --themes=silver --plugins=advlist,anchor,autolink,autoresize,autosave,bbcode,charmap,code,codesample,colorpicker,contextmenu,directionality,fullpage,fullscreen,hr,image,imagetools,insertdatetime,legacyoutput,link,lists,media,nonbreaking,pagebreak,paste,preview,quickbars,save,searchreplace,table,tabfocus,template,textcolor,textpattern,toc,visualblocks,visualchars,wordcount
```

*Note*: 
* we need to run ```grunt``` before run above command
* Due to this issue https://github.com/tinymce/tinymce/issues/4847, so emoticons can not be bundled, so I exclude it.
* Bundle does not support skin, so we will need to get skin release when integrate  

# Output
After execute above commands, we will have ```tinymce.full.js``` & ```tinymce.full.min.js``` on ```js/tincymce``` and skins output files
  