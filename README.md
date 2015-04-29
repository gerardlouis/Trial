## Default hotkeys

### General description

The hotkeys, as you can set them in `Config.ini`, are noted in the format
<modifier><key>; you may copy the
string from ` ` and use it as a template for a new line in `Config.ini`.
Possible modifiers are the following:

* `!` <kbd>Alt</kbd>
* `^` <kbd>Ctrl</kbd>, Control
* `#` <kbd>Win</kbd> / LWin, the left Windows key
* `+` <kbd>Shift</kbd>

You will have to press all keys of a hotkey at the same time beginning with the
modifier for calling the associated function, e. g. `#^q` means pressing the
left 'Windows key' and the 'Control key' and the 'Q key'
(<kbd>Win</kbd><kbd>Ctrl</kbd><kbd>Q</kbd>) for quitting bug.n.

### Window management

<kbd>Win</kbd><kbd>Down</kbd>
> Activate the next window in the active view.

<kbd>Win</kbd><kbd>Up</kbd>
> Activate the previous window in the active view.

<kbd>Win</kbd><kbd>Shift</kbd><kbd>Down</kbd>
> Move the active window to the next position in the window list of the view.

<kbd>Win</kbd><kbd>Shift</kbd><kbd>Up</kbd>
> Move the active window to the previous position in the window list of the view.

<kbd>Win</kbd><kbd>Shift</kbd><kbd>Enter</kbd>
> Move the active window to the first position in the window list of the view.
You may also move the active window to any other absolute position in the
window list by using the first parameter.

<kbd>Win</kbd><kbd>c</kbd>
> Close the active window.

<kbd>Win</kbd><kbd>Shift</kbd><kbd>d</kbd>
> Show / Hide the title bar of the active window.

<kbd>Win</kbd><kbd>Shift</kbd><kbd>f</kbd>
> Toggle the floating status of the active window (i. e. dis- / regard it when
tiling).

<kbd>Win</kbd><kbd>Ctrl</kbd><kbd>m</kbd>
> Minimize the active window; this implicitly makes the window floating.

<kbd>Win</kbd><kbd>Shift</kbd><kbd>m</kbd>
> Move the active window by key (only floating windows).

<kbd>Win</kbd><kbd>Shift</kbd><kbd>s</kbd>
> Resize the active window by key (only floating windows).

<kbd>Win</kbd><kbd>Shift</kbd><kbd>x</kbd>
> Move and resize the active window to the size of the work area (only floating
windows).

<kbd>Win</kbd><kbd>i</kbd>
> Get information for the active window (id, title, class, process name, style,
geometry, tags and floating state).

<kbd>Win</kbd><kbd>Shift</kbd><kbd>i</kbd>
> Get a window list for the active view (id, title and class).

<kbd>Alt</kbd><kbd>Down</kbd>
> Manually move the active window to the next area in the layout.

<kbd>Alt</kbd><kbd>Up</kbd>
> Manually move the active window to the previous area in the layout.

<kbd>Alt</kbd><kbd>Shift</kbd><kbd>Enter</kbd>
> Move and resize the active window to the size of the work area (only floating
windows).

<kbd>Alt</kbd><n>
> Manually move the active window to the n<sup><small>th</small></sup> area in
the layout (n = 1..9).

<kbd>Alt</kbd>0
> Manually move the active window to the n<sup><small>th</small></sup> area in
the layout.

<kbd>Alt</kbd><kbd>BackSpace</kbd>
> Toggle the stack area of the layout. If the stack area is disabled, the
master area takes up the whole view.

### Window debugging

<kbd>Win</kbd><kbd>Ctrl</kbd><kbd>i</kbd>
> Dump window information on the windows of the active view to the log.

<kbd>Win</kbd><kbd>Shift</kbd><kbd>Ctrl</kbd><kbd>i</kbd>
> Dump window information on the contents of the managed window list (floating
and tiled windows of all views) to the log.

<kbd>Win</kbd><kbd>Ctrl</kbd><kbd>h</kbd>
> Print a description of the formatting (column headings) used in the previous
two log messages (`Manager_logViewWindowList` and
`Manager_logManagedWindowList`) to the log.

<kbd>Win</kbd><kbd>Ctrl</kbd><kbd>d</kbd>
> Decrement the debug log level. Show fewer debug messages. You may also set
the debug log level to an absolute value by using the first parameter.

<kbd>Win</kbd><kbd>Ctrl</kbd><kbd>Shift</kbd><kbd>d</kbd>
> Increment the debug log level. Show more debug messages. You may also set
the debug log level to an absolute value by using the first parameter.

### Layout management

<kbd>Win</kbd><kbd>Tab</kbd>
> Set the previously set layout. You may also use `View_setLayout(0, +1)` for
setting the next or `View_setLayout(0, -1)` for setting the previous layout in
the layout array.

<kbd>Win</kbd><kbd>f</kbd>
> Set the 3<sup><small>rd</small></sup> defined layout (i. e. floating layout
in the default configuration).

<kbd>Win</kbd><kbd>m</kbd>
> Set the 2<sup><small>nd</small></sup> defined layout (i. e. monocle layout in
the default configuration).

<kbd>Win</kbd><kbd>t</kbd>
> Set the 1<sup><small>st</small></sup> defined layout (i. e. tile layout in
the default configuration).

<kbd>Win</kbd><kbd>Left</kbd>
> Reduce the size of the master area in the active view (only for the "tile"
layout). You may also set an additional parameter for accelerating the third
one. E. g. with
<kbd>Win</kbd><kbd>Left</kbd> the first
step, by which the master area is reduced, is -0.0016% and will be doubled with
consecutive calls until it reaches -0.05%.
With the second parameter you may set an absolute value, e. g.
`View_setLayoutProperty(MFactor, 0.5, 0)` splits the view in half.

<kbd>Win</kbd><kbd>Right</kbd>
> Enlarge the size of the master area in the active view (only for the "tile"
layout). You may also set a additional parameter for accelerating the third
one. E. g. with
<kbd>Win</kbd><kbd>Right</kbd> the
first step, by which the master area is reduced, is 0.05%, but with consecutive
calls it will be halved until it reaches 0.0016%.
With the second parameter you may set an absolute value, e. g.
`View_setLayoutProperty(MFactor, 0.67, 0)` makes the master area two thirds
and the stacking area one third the size of the view.

<kbd>Win</kbd><kbd>Ctrl</kbd><kbd>t</kbd>
> Rotate the layout axis (i. e. 2 -> 1 = vertical layout, 1 -> 2 = horizontal
layout, only for the "tile" layout).

<kbd>Win</kbd><kbd>Ctrl</kbd><kbd>Enter</kbd>
> Mirror the layout axis (i. e. -1 -> 1 / 1 -> -1 = master on the left / right
side, -2 -> 2 / 2 -> -2 = master at top / bottom, only for the "tile" layout).

<kbd>Win</kbd><kbd>Ctrl</kbd><kbd>Tab</kbd>
> Rotate the master axis (i. e. 3 -> 1 = x-axis = horizontal stack, 1 -> 2 =
y-axis = vertical stack, 2 -> 3 = z-axis = monocle, only for the "tile" layout).

<kbd>Win</kbd><kbd>Ctrl</kbd><kbd>Shift</kbd><kbd>Tab</kbd>
> Rotate the stack axis (i. e. 3 -> 1 = x-axis = horizontal stack, 1 -> 2 =
y-axis = vertical stack, 2 -> 3 = z-axis = monocle, only for the "tile" layout).

<kbd>Win</kbd><kbd>Ctrl</kbd><kbd>Up</kbd>
> Increase the master Y dimension by 1, i.e. increase the number of windows in
the master area by X. Maximum of 9 (only for the "tile" layout).

<kbd>Win</kbd><kbd>Ctrl</kbd><kbd>Down</kbd>
> Decrease the master Y dimension by 1, i.e. decrease the number of windows in
the master area by X. Minimum of 1 (only for the "tile" layout).

<kbd>Win</kbd><kbd>Ctrl</kbd><kbd>Right</kbd>
> Increase the master X dimension by 1, i. e. increase the number of windows in
the master area by Y. Maximum of 9 (only for the "tile" layout).

<kbd>Win</kbd><kbd>Ctrl</kbd><kbd>Left</kbd>
> Decrease the master X dimension by 1, i. e. decrease the number of windows in
the master area by Y. Minimum of 1 (only for the "tile" layout).

<kbd>Win</kbd><kbd>Shift</kbd><kbd>Left</kbd>
> Decrease the gap between windows in "monocle" and "tile" layout. You may also
set an absolute value for the gap width by using the first parameter, e. g.
`View_setLayoutProperty(GapWidth, 0, 0)` will eliminate the gap and
`View_setLayoutProperty(GapWidth, 20, 0)` will set it to 20px.

<kbd>Win</kbd><kbd>Shift</kbd><kbd>Right</kbd>
> Increase the gap between windows in "monocle" and "tile" layout.

### View / Tag management

<kbd>Win</kbd><kbd>Shift</kbd><kbd>n</kbd>
> Toggle the view margins, which are set by the configuration variable
`Config_viewMargins`.

<kbd>Win</kbd><kbd>BackSpace</kbd>
> Activate the previously activated view. You may also use
`Monitor_activateView(0, -1)` or `Monitor_activateView(0, +1)` for activating
the previous or next adjacent view.

<kbd>Win</kbd><kbd>Shift</kbd>0
> Tag the active window with all tags (n = 1..`Config_viewCount`). You may also
use `Monitor_setWindowTag(0, -1)` or `Monitor_setWindowTag(0, +1)` for setting
the tag of the previous or next adjacent to the current view.

<kbd>Win</kbd><n>
> Activate the n<sup><small>th</small></sup> view (n = 1..`Config_viewCount`).

<kbd>Win</kbd><kbd>Shift</kbd><n>
> Tag the active window with the n<sup><small>th</small></sup> tag (n =
1..`Config_viewCount`).

<kbd>Win</kbd><kbd>Ctrl</kbd><n>
> Add / Remove the n<sup><small>th</small></sup> tag (n = 1..`Config_viewCount`)
for the active window, if it is not / is already set.

### Monitor management

<kbd>Win</kbd>.
> Activate the next monitor in a multi-monitor environment. You may also
activate a specific monitor by using the first parameter, e. g.
`Manager_activateMonitor(1)` will activate the first monitor.

<kbd>Win</kbd>,
> Activate the previous monitor in a multi-monitor environment.

<kbd>Win</kbd><kbd>Shift</kbd>.
> Set the active window's view to the active view on the next monitor in a
multi-monitor environment. You may also set the active window on a specific
monitor by using the first parameter, e. g. `Manager_setWindowMonitor(1)` will
set the active window on the first monitor.

<kbd>Win</kbd><kbd>Shift</kbd>,
> Set the active window's view to the active view on the previous monitor in a
multi-monitor environment.

<kbd>Win</kbd><kbd>Ctrl</kbd><kbd>Shift</kbd>.
> Set all windows of the active view on the active view of the next monitor in
a multi-monitor environment. You may also set all windows of the active view on
a specific monitor by using the first parameter, e. g.
`Manager_setViewMonitor(1)` will set all windows of the active view on the
first monitor.

<kbd>Win</kbd><kbd>Ctrl</kbd><kbd>Shift</kbd>,
> Set all windows of the active view on the active view of the previous monitor
in a multi-monitor environment.

### GUI management

<kbd>Win</kbd><kbd>Shift</kbd><kbd>Space</kbd>
> Hide / Show the bar (bug.n status bar) on the active monitor.

<kbd>Win</kbd><kbd>Space</kbd>
> Hide / Show the task bar.

<kbd>Win</kbd><kbd>y</kbd>
> Open the command GUI for executing programmes or bug.n functions.

<kbd>Win</kbd><kbd>Shift</kbd><kbd>y</kbd>
> Toggle the overflow window of the 'notify icons'.

<kbd>Alt</kbd><kbd>Shift</kbd><kbd>y</kbd>
> Indicate the areas of the "tile" layout.

### Administration

<kbd>Win</kbd><kbd>Ctrl</kbd><kbd>e</kbd>
> Open the configuration file in the standard text editor. If you want to set
this hotkey in `Config.ini`, you have to replace `<Config_filePath>` with an
explicit file path.

<kbd>Win</kbd><kbd>Ctrl</kbd><kbd>s</kbd>
> Save the current state of monitors, views, layouts to the configuration file.

<kbd>Win</kbd><kbd>Ctrl</kbd><kbd>r</kbd>
> Reload bug.n (i. e. the whole script), which resets i. a. the configuration
and internal variables of bug.n, including the window lists. It is like
Quitting and restarting bug.n.
If `Config_autoSaveSession` is not set to `off`, the window lists can be
restored and windows are put to their associated monitor and views.

<kbd>Win</kbd><kbd>Ctrl</kbd><kbd>q</kbd>
> Quit bug.n, restore the default Windows UI and show all windows.
