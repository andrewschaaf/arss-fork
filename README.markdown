
Michel Rouzic wrote ARSS (Analysis & Resynthesis Sound Spectrograph) and maintained it through 2008.

The [ARSS project page](http://arss.sourceforge.net/) says "ARSS is now superseded by [Photosounder](http://photosounder.com/)", his non-[FOSS](http://en.wikipedia.org/wiki/Free_and_open_source_software) spectrogram editor.

This repo is a fork of ARSS 0.2.3.

## Building

<pre>cd src; cmake . &amp;&amp; make</pre>

## Examples

### (mono WAV) &rarr; (spectrogram as raw 32-bit float matrix columns)
<pre>cat foo.wav | ./arss-fork STDIN STDOUT --min-freq 500 --max-freq 20000 --height 100 --pps 100 --analysis --float32-columns > foo.matrix</pre>

You may want: [util_c/matrix2img](http://github.com/andrewschaaf/util_c)

## Changelog

### 0.3 : 2010-09-28
* Support for reading from/to STDIN/STDOUT
* Alternate output format: raw 32-bit float matrix columns.

## Notes

("STDIN","STDOUT") used instead of ("-"/"-") due to the original project's option parser.
