# Roller Coaster Simulation

## Summary
This is a computer graphics project simulating roller coaster physics, connecting modular tracks with Catmull-Rom spline interpolation, and general OpenGL programming. 

<img src="./Results/Screenshot 2025-03-02 220048.png" width="800">

### Instructions to run:
- Run this [Executable](./Project_2/Project_2.exe) <br>
or
- Watch this [Demonstration](./Results/2022-10-18%2018-50-15.mkv) instead

### Controls:

	T: toggle between riding the coaster and free movement
	
	W, A, S, D to move camera

	H: toggle heightmap
	N: toggle normals
	B: toggle boxes

			No Modifier				Shift				Ctrl
	U	Increase rotation rate in x-axis | Increase the scale in x-axis | Positive translation in the x-Axis
	J	Decrease rotation rate in x-axis | Decrease the scale in x-axis | Negative translation in the x-Axis
	I	Increase rotation rate in y-axis | Increase the scale in y-axis | Positive translation in the y-Axis
	K	Decrease rotation rate in y-axis | Decrease the scale in y-axis | Negative translation in the y-Axis
	O	Increase rotation rate in z-axis | Increase the scale in z-axis | Positive translation in the z-Axis
	L	Decrease rotation rate in z-axis | Decrease the scale in z-axis | Negative translation in the z-Axis

## Code 	
- Source code can be found here: [Code](./Project_2/Sources/)

- Headers can be found here: [Headers](./Project_2/Headers/)

- Since this was a class project. Most of this project is starter code. Below are all of the change and implementation made by me.

### Implementations made:
- [track.hpp](./Project_2/Headers/track.hpp)
	- [lines 40-42](./Project_2/Headers/track.hpp#L40-L42):
		- Vertex arrays for the right rail, left rail, and ties
	- [lines 65-98](./Project_2/Headers/track.hpp#L65-L98):
		- draw function is implemented
		- right rail, left rail, and ties are drawn
	- [lines 108-132](./Project_2/Headers/track.hpp#L108-L132):
		- Get_point function implemented
	- [lines 136-141](./Project_2/Headers/track.hpp#L136-L141):
		- Free data from vertex arrays
	- [line 148](./Project_2/Headers/track.hpp#L148):
		- VAOs and VBOs for the right rail, left rail, and ties
	- [lines 166-182](./Project_2/Headers/track.hpp#L166-L182):
		- interpolate function implemented
		- Catmull-Tom Spline interpolation
	- [lines 193-237](./Project_2/Headers/track.hpp#L193-L237):
		- create_track function implemented###
	- [lines 249-276](./Project_2/Headers/track.hpp#L249-L276):
		- make_triangle function implemented
	- [lines 283-489](./Project_2/Headers/track.hpp#L283-L489):
		- makeRailPart function implemented
	- [lines 509-571](./Project_2/Headers/track.hpp#L509-L571):
		- setup_track function implemented

- [camera.hpp](./Project_2/Headers/camera.hpp)
	- [lines 40-41](./Project_2/Headers/camera.hpp#L40-L41):
		- car variables
	- [lines 52-54](./Project_2/Headers/camera.hpp#L52-L54):
		- T button toggle variables
	- [lines 102-165](./Project_2/Headers/camera.hpp#L102-L165):
		- ProcessTrackMovement function implemented

- [Project2.cpp](./Project_2/Sources/Project2.cpp)
	- [line 177](./Project_2/Sources/Project2.cpp#L177):
		- rail texture loaded
	- [lines 194-196](./Project_2/Sources/Project2.cpp#L194-L196):
		- car model loaded
	- [lines 235-238](./Project_2/Sources/Project2.cpp#L235-L238):
		- ProcessTrackMovement called
	- [lines 284-287](./Project_2/Sources/Project2.cpp#L284-L287):
		- call to draw track
	- [lines 382-392](./Project_2/Sources/Project2.cpp#L382-L392):
		- draw car model
	- [lines 449-458](./Project_2/Sources/Project2.cpp#L449-L458):
		- free look toggle
	- [lines 461](./Project_2/Sources/Project2.cpp#L461):
		disable movement controls when on track
	- [line 632](./Project_2/Sources/Project2.cpp#L632):
		- disable camera rotation control when on track

- [Project2.hpp](./Project_2/Headers/Project2.hpp)
	- line 71(./Project_2/Headers/Project2.hpp#L71):
		- drawTrack bool added

- Extra Credit:
	- car model is added and follows the rail when onTrack is true
	- the model follows the position and rotation of the camera