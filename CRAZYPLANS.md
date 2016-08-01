
# Possible future projects


## Hardware improvements


### Projector options

* Select a projector that's suitable for use in high-light situations
* Investigate pico-sized projectors
* 3D stereoscopic projection onto the sand surface


### Compute options

* Test with Raspberry Pi 3 or similar sized cheaper computing
* Determine minimum specs for graphics card to run the hydrology modelling
  (tested with GTX 970 so far)


### Materials options

* Perspex (clear) sides for the sandbox
* Kinetic sand (expensive)
* is there a formula for better / firmer / smoother modelling sand?
* consider "green sand" used for casting


## Interface improvements


### improved settings for hydrology modelling

Try water modelling with `-wts 200 150` for initial testing or unless the PC running the Augmented Reality Sandbox has a top-of-the line CPU:

  * `-wo 2.0` is water opacity (2.0cm down is opaque)
  * `-rer mix` max for rain cloud level
  * `-rs` rain strength
  * `-evr` evaporation rate
  * `-rws` render water surface as a geometric surface


### Better UI

The C++ interface is spectacularly awkward to use.  Go through major actions (setup, config, calibration) note difficult moments, and fix them.

* Mention checking projector keystone settings; keystone may not be 0 (but should be)
* Document where and which files to backup (etc/SARndbox*/*)
* Examine the popup menu options in SARndbox
* Document raising/lowering the BoxLayout.txt height to change colour settings
  * Can use the -slf option to set a specific filename (eg
  higher.txt/lower.txt)


### Better / automated calibration

At present, calibration is very manual, requiring at least two people to run through the steps.  The Kinect camera could be configured to automatically recognise the shape of the calibration disc and automatically record the relevant positioning.  The process of recording the depth field and base plane require manual copy-pasting of the values found; this could be written automatically.


### Wrapper UI

Rather than or alongside an update to the C++ interface, let's develop software in Python or something that wraps the C++ process with a friendly GUI.

* invoke the process from the command line behind the GUI
* use checkboxes to engage command line flag items
* allow user selection of colour schemes, copy or symlink the scheme into place
* maybe some calibration values are user tweakable?
* support forks/adaptations of sARndbox other than then original
* maybe preview colour schemes on a gradient bar?
* maybe have user editing of colour schemes?


### In-sandbox interface

Is there a way to use Kinect sensing to allow the user to interact with settings etc?

* a board with circles drawn on: options projected, user places an object to select an option
* a menu projected across sandbox, user places or waggles hand to select items
* how can the menu disappear when it's not being used?


### More colour schemes

* tropical colours (yellower greens, pacific-cyan water, brown mountains)
* temperate colours (bluer greens, atlantic-blue water, grey and white mountains)
* versions without blue waterline (for use with fluid modelling)
* coral reef / continental shelf (colour shallower water as if it's a reef) see <https://en.wikipedia.org/wiki/Continental_shelf>
* other planets -- mars, jupiter...
* full rainbow for maximum differentiation
* grids, alternating stripes, etc


### Richer overlays

Add physical or rasterised base layers to the model; using slices rather than just colours to show different aspects at different depths.  Eg:

* Aerial photography
* Archaeological dig sites (fossils, ruins etc)
* Mining and geology (mineral/resource layers)
* Sedimentology


### Richer modelling

Enable a wider range of environmental variables and graphics.

* lava, snow, mud (derivatives of water/fluid)
* clouds
* wind
* dynamic rain
* time (day/night/sun/moon) maybe even with shaded hillsides
* tides
* "flood from here" to simulate continuous water (or lava, etc) flow from a single point


### Model matching mode

Essentially "paint by numbers" shaping -- given a known topographic model, create an easy-to-follow interface for changing the sandpit to match the model. Project colours (or even animation like marching stripes) to show where the sand doesn't match the model?  Red for dig away more, blue for pile up more?  This would help to quickly construct a sand model of a known area.

* how to supply known model?  a bunch of x,y,z points?
* match against sand level
* colour based on difference
* can we do an area animation?


### Wandering monsters

Randomly add a passing animal, person, or vehicle traversing the area.

* flying things can just traverse the map
* with feature detection, eagles can circle mountains
* people can respond to altitude-mapped (temperature): bikinis at the beach, jackets on the mountainside, scuba in water


### Archaeology / paleontology / mining sim

Use the sandbox to simulate excavation through various geologic strata.

* start with a high sand level and excavate down
* project colour banding to represent geological strata
* support a "prep" mode that starts empty, builds up sand to a certain time period / depth, adds the relevant dinosaur bones or pottery shards or whatever, then layers more sand on top
* if there are known, preset locations for finds, could project a "spotlight" to highlight the discovery area


### Interactive gaming

Perhaps with feature recognition, for placing buildings etc.

* tower defence -- creepers can't scale hills
* SimCity-style urban development




