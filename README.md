# sdlgui
C++ GUI system (graphical user interface) for libSDL 1.2.x with optional OpenGL support (no further dependencies)

Project modules:
  - UNICODE - Basic support for Unicode strings and encoding conversion (standalone)
  - FONT - Text rendering using glyph bitmaps (depends on UNICODE and SDL/OpenGL, not GUI)
  - UNISURFACE - Universal surface structure wrapping SDL surface and OpenGL texture (depends on SDL/OpenGL)
  - GUI - Widgets, event binding and rendering of widget trees (depends on FONT/UNICODE, SDL/OpenGL)


Notes:
  - UNICODE, FONT, UNISURFACE don't depend on GUI (just copy the specific module src files and include to your project)
  - OpenGL dependency can be removed via preproc. macro
  - Event handling via widget bound callback functions, also supports binding of callback methods
  - Avoids freezing issue on Windows (when moving or resizing the window) via extra thread
  - Support for OS dependent features (drag & drop, file dialog)
  - libSDL 1.2.x is available for much more systems, so no SDL2 support yet (SDL2 is not "Simple" anymore and will never be ported to that many platforms.)
