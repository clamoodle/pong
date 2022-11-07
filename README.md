Game!!

# Log Entries
## Tuesday, 5/24, 8:20 - 8:27 pm
**WHO:** Twombly

**WHAT:** Copied over necessary files and created a game_demo.c file. We were set back because there was a technical error that prevented the project repo from opening.

**BUGS:** Might be missing sdl library downloads and we might need an extra JSON file + new Makefile.

**RESOURCES USED:** TAs


## Wednesday, 5/25, 3:00-5:11 pm
**WHO:** Twombly

**WHAT:** 
- Added new get / set functions for surface and texture in body
- Added surface and texture in body struct
- Started a simple outline in game_demo.c and added some possible constants
- Added #includes for libraries in most files
- Added variables to scene struct then updated scene_init and scene_free
- Added get / set / add functions for new variables and sound effects / sprites
- Created an extras folder for sounds / sprites / textures

**BUGS:** 
- Need to work on sdl file
- Need to make a file(s) to init background / props
- Might be missing a file or two

**RESOURCES USED:** 


## Wednesday, 5/25, 6:50 - 7:10 pm
**WHO:** Twombly

**WHAT:** Added sound effect / noises .wav files in extras folder.

**BUGS:** 

**RESOURCES USED:** free download mp3 libraries on internet

## Thursday, 5/26, 7:00pm - Friday, 5/27 3:00am
**WHO:** Joaquín

**WHAT:** Built proof-of-concept for the first menu and level (and how switching from one to the other will work). Created a state.c file to lay out what elements each level will have.

**BUGS:** 

**RESOURCES USED:** am having a "Runtime error: Unreachable" in the console of the demo

## Week of 5/23, on and off for around 5 hours total
**WHO:** Pearl

**WHAT:** Made character/background/pellet sprites

## Friday, 5/27, 1:00 - 3:00 pm
**WHO:** Pearl and Twombly

**WHAT:** 
- Drew / Added more sprites
- Drew / Added background to fit rectangle dimensions
- Added create functions for texture and noises in sdl
- Updated some sdl functions
- Added free functions for texture and noises
- Added create functions for pictures/jpegs/pngs/sprites

**BUGS:** 
- May need editing: sdl_render_scene, sdl_draw_polygon

**RESOURCES USED:** sdl library documentation


## Saturday 5.28 11 am - 2 pm
**WHO:** Jaeyoon

**WHAT:** Working on the pong demo

**BUGS:** Collisions are not working as expected. restarting the game does not work

**RESOURCES USED:** 


## Saturday 5.28 2 pm - 3 pm
**WHO:** Jaeyoon

**WHAT:** Working on the pong demo

**BUGS:** . restarting the game does not work.
- Recopied the correct physics library from last project.
- Collisions are now working as expected.

**RESOURCES USED:** 

## Saturday, 5/28, 3:00 - 4:38 pm (on and off)
**WHO:** Twombly

**WHAT:** 
- Worked on (some) text rendering in sdl
- Worked on rgb for text/points
- Figuring out sdl functions
- Attempted to implement point rendering in sdl
- May be switched out later^

**BUGS:** 
- Accidentally uploaded wrong physics folder oops :')
- SDL types are weird but SDL library has a section with examples
- Need to guess and check some sizes and locations

**RESOURCES USED:** sdl library documentation


## Sunday 5.28 1 pm - 3 pm
**WHO:** Jaeyoon

**WHAT:** Finished up the pong demo

**BUGS:** 
- Added scoring, AI.
- completes 1ab and 2b as well as 3a.


**RESOURCES USED:** 

## Sunday, 5/29, 5:30 - 7:00 pm
**WHO:** Pearl

**WHAT:** 
- changed sdl_show_points arg to int instead of string
- worked on game_demo.c trying to make text show
- added points_acc to state
- worked on some key_handling in demo

**BUGS:** 

**RESOURCES USED:** sdl library documentation


## Sunday, 5/29, 7:30 - 10:00 pm
**WHO:** Pearl

**WHAT:** 
- drew more sprites (ending screen + 2 more backgrounds)

## Sunday, 5/29, 8:00pm - Monday, 5/30, 3:30am
**WHO:** Joaquín

**WHAT:** 
- Created game_t to store state, misc global game variables (curr_level), and a looping function for each level
- Created game_info.h to store global constants (window size)
- Made emscripten functions loop only on game_t
- Moved emscripten.c function headers to emscripten_main.h (emscripten.h is reserved for something else and having them in state.h created circular dependencies)
- Created button class with a button_trigger function
- Created shapes.h to store functions related to making shapes (list_t of vector_t)
- Put key_handler inside game_demo.c (may make key_handler) a field of game_t such that it can easily be switched when levels are changed
- Got level/menu-switching implementation working
- Created sprite_t to hold sprites for bodies and scenes
- Wrote functions for drawing sprites in sdl_wrapper
- Implemented static sprite rendering in bodies and scenes (including properly freeing them)
- Updated MakeFile

**BUGS:** Cool bug where after freeing a state in a for loop looping over only 1 item, I was getting heap_use_after_free. This was due to calling the list_size function as the upper bound for the for loop, which was freed when the state was freed. Fixed by adding a break statement.

**RESOURCES USED:** 


## Monday 5.30 3 pm - 6 pm
**WHO:** Jaeyoon

**WHAT:** Merging in with master

**BUGS:** 

**RESOURCES USED:** '


## Tuesday, 5/31, 2:45 - 3:50 pm
**WHO:** Pearl

**WHAT:** 
- split title screen sprite into title/character selection
- made character sprites into paddle-holding ones

**BUGS:** 

**RESOURCES USED:** 


## Tuesday, 5/31, 4:15pm - 6:15pm
**WHO:** Pearl and Joaquín

**WHAT:** 
- Wrote the text rendering abstraction (sdl_draw_text)

**BUGS:** Didn't run TTF_Init().

**RESOURCES USED:** 


## Tuesday, 5/31, 7:00 - 8:00 pm
**WHO:** Pearl

**WHAT:** 
- added text_update_content to text.c
- implemented scene_update_text_content and scene_remove_text

**BUGS:** 

**RESOURCES USED:**


## Tuesday 5/31 10:00pm - Wednesday 6/1 7:56am
**WHO:** Joaquín

**WHAT:** 
- Wrote abstraction for levels to provide different key handlers
- Wrote abstraction for character selection
- Updated the sprites
- Made the option to provide bodies only a sprite, in which case the shape defaults to the sprite's bounding rectangle
- Wrote abstraction for 2-player character selection
- Moved pong.c to level1.c and rewrote to fit abstraction, added sprites
- Added player-dependent rotated sprites
- Made pellet reset when points are scored
- Added text displaying player points
- Added caps to pellet velocity
- Made the pellet reset after leaving the screen
- Made ai character selection random
- Capped ai position

**BUGS:** A lot of circular dependency issues for key handling. Resolved by declaring the existence of a game_t struct in game_info.h

**RESOURCES USED:** 

## Wednesday 6/1 4:00 pm - 7:00 pm
**WHO:** Twombly

**WHAT:** 
- Implemented noise when the ball hits opposing players wall
- Implemented game background sound
- Cut and compressed wav files
- Uploaded new sounds
- Got ride of excess files
- Updated header files
- Tried to free

**BUGS:** Not freeing properly, I don't think the sounds are being added 
to the list in scene.

**RESOURCES USED:** sdl libraries, online compression tools

## Thursday 6/2 9:20 pm - 9:40 pm
**WHO:** Twombly

**WHAT:** 
- Freed sounds / noises
- 3 functions

**BUGS:** I was passing in NULL for the free function oops

**RESOURCES USED:** TAs

## Thursday 6/2 9:30 pm - Friday 6/3 12:40 am
**WHO:** Pearl

**WHAT:** 
- Levels abstraction (made level.c and level.h)
- Modified level1.c and grav_lvl1.c to use level.h 
- added multiball_lvl1.c level with multiple pellets
- modified level.c to generalize level_reset_pellets to reset a whole list of pellets

**BUGS:** errors when compiling, including "undefined symbol" for all level.c functions

**RESOURCES USED:** TAs
