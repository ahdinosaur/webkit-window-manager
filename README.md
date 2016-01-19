# webkit-window-manager

## idea

what if customizing your Linux desktop meant writing HTML, CSS, and JavaScript?

## design

Linux [desktop environments](https://en.wikipedia.org/wiki/Desktop_environment) are built on [window managers](https://en.wikipedia.org/wiki/Window_manager) which are built on [display managers](https://en.wikipedia.org/wiki/X_display_manager_(program_type)). [X11](https://en.wikipedia.org/wiki/X_Window_System) is the most common legacy display manager, to be superseded by [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol).

for this project, we use a minimal compositor library (like [wlc](https://github.com/Cloudef/wlc), [swc](https://github.com/michaelforney/swc), or [orbment](https://github.com/Cloudef/orbment)) with a WebKit rendering engine (like [electron](http://electron.atom.io/) or [NW.js](http://nwjs.io/)) to create a minimal window manager where each window (panel, ...) is a WebKit window.

## open questions

### how do we render normal programs?

obviously we need to render normal programs within our WebKit windows. we wonder if it's possible to have custom DOM elements / web views, similar to how Chrome renders PDFs on page, so the display output from a normal program could be represented in the DOM tree.
