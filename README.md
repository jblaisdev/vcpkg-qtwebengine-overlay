# vcpkg-qtwebengine-overlay
Port overlay files for building [qtwebengine] v6.8.3

These are the vcpkg files from [qtwebengine] v6.8.3 port#0 with three additional patches to allow building on x64 windows with VS2022.

Two patches are a syntax and additional include file:
  gc-marking-state-fix.patch
  blink-more-include-fixes.patch

One patch disable precompiled headers for the chromium blink module. This may not be required in your environment, but was in mine:
  blink-pch-off.patch

Finally, --x-buildtrees-root was also used so that builds happen in a short-named top level directory to avoid windows 260 char path length issues. For example, "C:\blds" 
