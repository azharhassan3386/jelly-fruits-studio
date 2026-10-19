# jelly-fruits-studio
🍓 Jelly Studio

An interactive fruit-slicing playground built with plain HTML, CSS and JavaScript: no frameworks, no game engine, no build step. Drag the fruit to make it wobble, slice it seven different ways, and watch the pieces dance.

Add a demo GIF or video link here, for example: ![Jelly Studio demo](demo.gif)

Features
Spring-physics wobble: drag the fruit and it squashes, stretches and bounces back.
Hand-drawn SVG fruit: strawberry (with seeds and calyx), mango and grapes, plus a glossy jelly dome.
7 cutting styles: slices, wedges, cubes, diagonal, halves, layers and zigzag, all made from clip-path so one shape becomes many independent pieces.
Dancing pieces: six dance steps (bounce, wave, spin, shake, disco, wobble) with a small note played on every beat.
Auto show: press Slice once and it cycles through every cut while the dance step shuffles.
Sound: slice and squish sound effects made with the Web Audio API (no audio files).
Responsive and accessible: works on phones, supports dark mode and reduced motion, and has keyboard shortcuts.
Run it

It is a single file with no dependencies.

Download index.html (or clone this repo).
Open it in any modern browser.

If your browser blocks fonts or audio when opening a local file, serve it instead:

bash
python -m http.server 8000
# then open http://localhost:8000
Controls
Action	How
Wobble the fruit	Drag it with mouse or finger
Start the auto show	Slice button or Space
Reset to a whole fruit	Reset button or R
Choose one cut yourself	Click a cut style (stops the auto show)
Change fruit	Strawberry, Jelly, Grapes or Mango
Change dance move	Step button
Pause or resume dancing	Dance button
Mute	Speaker button
How it works
Wobble: a small spring simulation (position, velocity, damping) updated every frame with requestAnimationFrame.
Cutting: the fruit SVG is cloned once per piece, and each clone is clipped with a different clip-path (inset() or polygon()).
Cut faces: a CSS mask built from the fruit's outline draws a lighter edge only where the fruit was cut.
Cube pieces: a canvas isPointInPath test skips grid cells that fall outside the fruit.
Dancing: each piece gets its own phase offset, so the pieces move as a wave instead of in unison.
Tech

HTML5, CSS3 (custom properties, clip-path, mask-image), SVG, vanilla JavaScript, Web Audio API.

Ideas for later
A record button to export the show as a video
More fruits and more cutting styles
Slicing by dragging a knife across the fruit
License

MIT. Use it, remix it, learn from it.
