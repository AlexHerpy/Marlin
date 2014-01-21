ReadMe - Auto Bed Leveling

Date:
2014-01-21

Summary:
A few notes on configuring the Auto Bed Leveling feature of Marlin for use with a modified Solidoodle.


Detailed Description:

Auto Bed Leveling is a feature that  compensates for a printing surface that is not perfectly level, however the surface does need to be perfectly flat. This feature utilizes the Z-axis endstop to probe 3 points (or more) on the printing surface. Typically, the endstop is mounted to a servo that positions the endstop below the hot end during leveling, then retracts the endstop during printing.

For the Solidoodle printer, rather than using a servo, the Z-axis end stop is rigidly mounted to the carrage. The relative position of the end stop from the tips of the hot end is about [-15, -70, 6.0] mm.  At the probe locations a 6.3 mm tall cap nut is placed. Relative to the end stop position, the probe locations are [0, 130], [0,0], [140,0].

The probe locations should be updated to reflect their position relative to the hot end.   


Auto Bed Leveling Parameters in Configuration.h file:

1. Uncomment #define ENALBLE_AUTO_BED_LEVELING

2. Define the probe locations, where:
	left/front is [x-min,y-min]
	left/back is [x-min, y-max]
	right/front is [x-max, y-min]

3. Define probe offset from hot end (Z-offset must be 0)


