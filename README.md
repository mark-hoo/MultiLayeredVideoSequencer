<h1>Multi Layered Video Sequencer</h1>
Made with:<br>
<li>
	<ul>Processing 1.5.1: <a href="http://processing.org/download/">http://processing.org/download/</a><br>
	GSVideo 1.0.0: <a href="http://sourceforge.net/projects/gsvideo/files/gsvideo/1.0/">http://sourceforge.net/projects/gsvideo/files/gsvideo/1.0/</a><br>
	GLGraphics 1.0.0: <a href="http://sourceforge.net/projects/glgraphics/files/glgraphics/1.0/">http://sourceforge.net/projects/glgraphics/files/glgraphics/1.0/</a><br>
	ControlP5 1.5.2: <a href="http://code.google.com/p/controlp5/downloads/list">http://code.google.com/p/controlp5/downloads/list</a><br>
	JSON4Processing 1.3.1: <a href="https://github.com/MAKIO135/JSON-processing">https://github.com/MAKIO135/JSON-processing</a></ul>
</li>
<p>Videos used in the demo are from <a href="http://www.beeple-crap.com/vjclips.php">Beeple</a></p>
<h3>This project is under developpement.<br>Help welcome.</h3>
<img src="http://makio.free.fr/divers/Github/VideoSequencer.jpg">
<br>
<p>First, add your videos inside /data/videos folder. It will automatically create playlist and check if thumbnails exist or need to be created.<br>The Sequencer works in 3 steps/parts:</p>
<li>
	<ul>- Clips: choose a video, modify its settings and add the created clip to a chosen Layer.<br>
	- Layers: a succession of clips playing one after another, you can modify each layer settings and choose a delay before playing Layer.<br>
	- Composition: all the Layers playing at the same time (after their launch delay is met) with the blendMode chosen for the current clip of each Layer.</ul>
</li>
<br>


<h2>Part 1: Clip Editor</h2>
<img src="http://makio.free.fr/divers/Github/VideoSequencerPart1.png" alt="Video Sequencer Part 1"><br>
<p>The Clip Editor allows you to edit Clip settings like:</p>
<li>
	<ul>- play mode: loop or play-playback<br>
	- number of repetition (loop 1 = play once, you need 2 for play-playback)<br>
	- how fast/slow the movie should be run<br>
	- position XY<br>
	- scale<br>
	- opacity<br>
	- blendmode<br>
	- custom fade in and fade out<br>
	- choice of VideoLayer to add the clip to</ul>
</li>

<h3>Needing fixes:</h3>
<li>
	<ul>- Some videos are freezing randomly whitout error message: codecs? GLGraphics, GSVideo or GStreamer ??<br>
	- ControlP5 Timeline: Sometimes not updating correctly<br></ul>
</li>

<h3>GStreamer issue</h3>
<p>
	<b>** (java.exe:6352): WARNING **: gstvideo: failed to get framerate property of pad playsink0:audio_raw_sink<br>
	(java.exe:6352): GStreamer-CRITICAL **: gst_value_get_fraction_numerator: assertion `GST_VALUE_HOLDS_FRACTION (value)' failed</b><br>
	Happens when using movie.frame() continuously.<br>
	Depends on videos and have them restart.
</p><br>
<br>


<h2>Part 2: VideoLayers</h2>
<img src="http://makio.free.fr/divers/Github/VideoSequencerPart2.png" alt="Video Sequencer Part 2"><br>
<p>A videoLayer is defined as an array clips playing successively.<br>
The Layer Editor allows you to edit each Layer settings like:</p>
<li>
	<ul>- position XY<br>
	- scale<br>
	- opacity<br>
	- custom fade in and fade out<br>
	- delay before playing first clip of the Layer</ul>
</li>

<h3>Needing fixes:</h3>
<li>
	<ul>- Layer Timeline is buggy when adding clips with "Aller Retour" playmode</ul>
</li>

<h3>Needs:</h3>
<li>
	<ul>- method for re-editing Clip + method to update Clip</ul>
</li>
<br>
<br>


<h2>Part 3: Composition</h2>
<img src="http://makio.free.fr/divers/Github/VideoSequencerPart3.png" alt="Video Sequencer Part 3"><br>
<p></p>

<h3>Needs:</h3>
<li>
	<ul>- Layers display with blend modes<br>
	- BlendModes<br>
	- Save method with JSON<br>
	- Load method</ul>
</li>