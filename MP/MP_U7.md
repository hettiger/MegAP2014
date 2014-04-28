#Video auf Webseiten

Nachfolgend gehe ich auf das Videotag und die Videodateitypen ein. Abgerundet wird diese Übersicht mit einem Infovideo von Bueny.

##HTML
Moderne Webseiten werden heutzutage mit HTML5 umgesetzt. HTML5 bietet viele Neuerungen, darunter auch das ```<video>```-Tag. Damit Videos in allen Browsern verfügbar sind müssen wir mit mehreren Videodateitypen (siehe unten) arbeiten.

###Der Aufbau

Nachfolgend der grundlegende Aufbau eines Videotags in einer simplen und einer komplexen Variante

####Simple Variante

Nachfolgend eine simple Varainte des Videotags. Ein Kompatibilität zu mehreren Browsern kann nicht gewährleistet werden, da hier nur ein Videodateityp eingebunden werden kann.

```html
<video width="320" height="240" type="video/mp4" src="myvideo.mp4" poster="poster.jpg" controls="controls" autoplay>
    <p>Dein Browser ist leider zu alt f&uuml;r den Video-tag :(</p>
</video>
```

####Komplexe Variante

Mit dieser Variante können wir für mehrere Browser Videos bereitstellen.

```html
<video width="320" height="240" poster="poster.jpg" controls="controls" autoplay loop>
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
####```<video>```

wie man in unserem Beispiel schon sieht, haben wir im Video-tag mehrere Attribute zur Auswahl. Diese werden nachfolgend erklärt.

#####audio
Wenn der Wert "muted" gesetzt, ist der Ton stummgeschaltet

#####autoplay

Medieninhalt direkt beim Laden abspielen

#####controls

Browsertypische Kontrollleiste anzeigen

#####height

Definiert die Höhe des Videos

#####loop

Medieninhalt endlos wiedergeben

#####poster

Bild welches bis zum Abspielvorgang angezeigt wird

#####preload

Medieninhalt bei Seitenaufruf vorladen

#####src

Gültige URL zum jeweiligen Medieninhalt (sofern nur ein Video verwendet wird)

#####type

Gültiger Dateityp für das Video.

#####width

Definiert die Breite des Videos

####```<source>```
Innerhalb des Video-tags können wir mit dem ```<source>```-tag arbeiten. Dies dient als Alternative zum ```src```-Attribut im ```<video>```-Tag. Zudem können wir mehrere Videodateiformate verwenden und somit auch eine Kompatitbilität zu den aktuellen Browsern gewährleisten. Technisch gesehen nutzt z.B. der Internet Explorer nur das Videoformat was er kennt und ignoriert die anderen.

Für das ```<source>```-Tag stehen uns folgende Attribute zur Verfügung.

#####src

Gültige URL zum jeweiligen Medieninhalt (sofern nur ein Video verwendet wird)

#####type

Gültiger Dateityp für das Video.

##Die Videodateitypen

Durch die aktuelle Browservielfalt sind wir leider gezwungen mit mehreren Videodateitypen zu arbeiten. Nachfolgend eine kurze Übersicht über die Formate:

###MPEG4 (H.264)

H.264/MPEG-4 AVC ist ein [H.-Standard](http://de.wikipedia.org/wiki/H.-Standards) zur hocheffizienten Videokompression. H.264 wurde nicht auf einen spezifischen Verwendungszweck zugeschnitten, sondern entfaltet seine Leistung in einem recht breiten Spektrum an Anwendungen. [Mehr Informationen](http://de.wikipedia.org/wiki/H.264)

###WebM (Theora)

WebM ist ein Video-Containerformat, das für das Internet entwickelt wurde. Das von Google initiierte Projekt wird unter anderem von der Mozilla Foundation und von Opera Software unterstützt. [Mehr Informationen](http://de.wikipedia.org/wiki/WebM)

###Ogg (VP8)

Ogg ist ein Container-Dateiformat für Multimedia-Dateien, kann also gleichzeitig Audio-, Video- sowie Textdaten enthalten. Ogg wurde mit dem Ziel konzipiert, eine freie und von Softwarepatenten unbeschränkte Alternative zu proprietären Formaten zu bieten, um Multimedia-Inhalte effizient zu speichern und zu streamen. [Mehr Informationen](http://de.wikipedia.org/wiki/Ogg)

###Übersicht über unterstützte Dateitypen nach Browser

Browser | Ogg | MP4 | WebM
--- | --- | --- | ---
Internet Explorer 11 | ja | nein | ja
Firefox 26.0+ | ja | nein | ja
Chrome 32.0+ | ja | ja | ja
Safari 7.0+ | ja | ja | nein
Opera 18+ | ja | nein | ja

##Ein übersichtliches Infovideo von Bueny

[![Ein übersichtliches Infovideo von Bueny](http://img.youtube.com/vi/jp-Tlr3kJqg/0.jpg)](http://www.youtube.com/watch?v=jp-Tlr3kJqg)
