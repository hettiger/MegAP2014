#Video auf Webseiten

##HTML
Moderne Webseiten werden heutzutage mit HTML5 umgesetzt. HTML5 bietet viele Neuerungen, darunter auch das ````<video></video>```-Tag.

###Der Aufbau

Nachfolgend der grundlegende Aufbau eines Videotags

```html
<video width="320" height="240" poster="poster.jpg">
    <!-- MP4 for Safari, IE9, iPhone, iPad, Android, and Windows Phone 7 -->
    <source type="video/mp4" src="myvideo.mp4" />
    <!-- WebM/VP8 for Firefox4, Opera, and Chrome -->
    <source type="video/webm" src="myvideo.webm" />
    <!-- Ogg/Vorbis for older Firefox and Opera versions -->
    <source type="video/ogg" src="myvideo.ogv" />
    <!-- Flash fallback for non-HTML5 browsers without JavaScript -->
    <object width="320" height="240" type="application/x-shockwave-flash" data="flashmediaelement.swf">
        <param name="movie" value="flashmediaelement.swf" />
        <param name="flashvars" value="controls=true&file=myvideo.mp4" />
        <!-- Image as a last resort -->
        <img src="myvideo.jpg" width="320" height="240" title="No video playback capabilities" />
    </object>
    <p>Dein Browser ist leider zu alt f&uuml;r den Video-tag :(</p>
</video>
```
####```<source>```
Innerhalb des Video-tags arbeiten wir mit dem ```<source>```

###Die Videodateiformate

Durch die aktuelle Browservielfalt sind wir leider gezwungen mit mehreren Videodateiformaten zu arbeiten. Nachfolgend eine kurze Übersicht über die Formate:

####MP4
####webM
####ogg


##ein Infovideo

https://www.youtube.com/watch?v=jp-Tlr3kJqg&feature=youtube_gdata_player
