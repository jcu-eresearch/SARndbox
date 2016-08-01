# Todo

## Future projects

These are a selection of potential improvements that we could assign to
students (honours, masters or PhD) or work experience groups.

### General concepts

* Environmental modelling (flooding, temperature changes)
* Ecological changes (animal distribution)
* Urban planning and development (buildings, traffic movement, foot traffic
  dependent on features, etc)
* Disaster management and simulations
* Interactive games design

### Software

* Improved colour coding for different scenarios:

  * Coast and continental shelf colouring (rainforest, island, shelf), see
    <https://en.wikipedia.org/wiki/Continental_shelf>
  * Segments of DEM colouring: eg https://www.arcgis.com/home/item.html?id=feb3c625dc094112bb5281c17679c769

* Improved settings for hydrology modelling. Try water modelling with `-wts
  200 150` for initial testing or unless the PC running the Augmented Reality
  Sandbox has a top-of-the line CPU:

  * -wo 2.0 is water opacity (2.0cm down is opaque)
  * -rer mix max for rain cloud level
  * -rs rain strength
  * -evr evaporation rate
  * -rws render water surface as a geometric surface

* Improved calibration process: at present, the process is very manual,
  requiring at least two people to run through the steps.  The Kinect camera
  could be configured to automatically recognise the shape of the calibration
  disc and automatically record the relevant positioning.  The process of
  recording the depth field and base plane require manual copy-pasting of the
  values found; this could be written automatically.

* User interface improvements:

  * UI for changing settings or configuration (eg wrapper or Kinect-based UI)
  * Ability to configure settings (environment/colour schemes) dynamically

* Reproducible construction and topographic models:
  essentially "Paint by numbers" shaping; an easy-to-follow interface for
  changing the sandpit into a prescribed topographical model.  For instance,
  to build a model of Townsville one would use a 'diff' process between the
  desired share and the current landscape, and show the user where to raise
  and where to lower sand to make the models roughly match.  Colour coding,
  kinetic sand and a grid would make things even easier.

* Wider range of environmental variables and graphics:

  * Lava, snow, mud (derivatives of water/fluid)
  * Clouds
  * Wind
  * Dynamic rain
  * Time (day/night/sun/moon)
  * Tides

* Adding physical or rasterised base layers to the model; using slices rather
  than just colours to show different aspects at different depths.  Examples
  include:

  * Aerial photography
  * Archaeological dig sites (fossils, ruins etc)
  * Mining and geology (mineral/resource layers)
  * Sedimentology

* Interactive gaming: tower defence, SimCity-style urban development

### Hardware

* Investigate kinetic sand (expensive)
* Kinect v2 coming soon! http://lakeviz.org/forums/topic/what-will-change-in-2-0/
* Select a projector that's suitable for use in high-light situations
  * Investigate pico-sized projectors
  * 3D stereoscopic projection onto the sand surface
* Set up new computer
  * Test with Raspberry Pi 3 or similar sized cheaper computing
  * Determine minimum specs for graphics card to run the hydrology modelling
    (tested with GTX 970 so far)
* Perspex (clear) sides for the sandbox

## Code improvements

* Mention to check projector keystone settings; keystone may not be 0
* Document where and which files to backup (etc/SARndbox*/*)
* Examine the popup menu options in SARndbox
* Document raising/lowering the BoxLayout.txt height to change colour settings

  * Can use the -slf option to set a specific filename (eg
    higher.txt/lower.txt)

* Formalise the file formats: use CSV with headings, JSON/YAML/XML etc

## To read

* https://system76.com/weekend-project/arsandbox
* http://lakeviz.org/forums/topic/common-issues-read-this-first/
* http://lakeviz.org/forums/topic/sandbox-posters/
* http://geoinfo.nmt.edu/publications/periodicals/litegeology/39/lg_v39.pdf - geology tasks
* https://brmlab.cz/project/ar_sandbox
* http://isandbox.co.uk/
* http://en.sandystation.cz
