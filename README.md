Dispatch Decision Engine  
C++ Text-Based Visual Novel

Project Overview
  The Dispatch Decision Engine is a text-based visual novel developed in C++ that follows Robert’s character arc in *Dispatch*,
Episode 1. The program allows players to make key decisions that influence Robert’s morality, relationships, combat style, 
and eventual transition from frontline superhero work to a dispatcher role.

  The project demonstrates how functions, Boolean variables, integers, and conditional statements can be used to create branching 
narratives and persistent consequences across multiple scenes.

Objectives of the Program
- Implement a decision-driven narrative using C++
- Track long-term character traits using global variables
- Use `if/else` statements to control story flow
- Simulate relationship and personality development
- Produce a final epilogue that reflects accumulated player choices

Program Structure
  The program is divided into five main scene functions and one epilogue function.  
Each scene represents a key moment from the story where the user must choose between two actions. 
These actions update global variables that affect later scenes and the ending. The scenes are called sequentially from the `main()` function.


Global Variables
The following global variables store persistent player decisions:
- `bool isMerciful`  
  Tracks whether Robert chooses compassion or ruthless efficiency.
- `int Blazer_Impression_Score`  
  Measures how strongly Blonde Blazer remembers Robert’s public actions.
- `bool isRomanticTensionActive`  
  Determines whether a romance path is activated.
  
Additional Tracking Variables
- `int Robert_Health`  
  Tracks damage taken during the street fight and reflects combat consequences.
- `bool isTactical`  
  Indicates whether Robert learned tactical awareness from combat.
These additional variables add depth and are explained through narrative output in later scenes and the epilogue.

Scene Breakdown and Decision Paths
1. Apartment Interrogation  
Function:`scene_interrogation()`
This scene establishes Robert’s moral direction.
- Pulling the goon back sets `isMerciful = true`
- Letting him drop reinforces a ruthless reputation
This choice influences later combat narration and the epilogue.

2. Street Fight  
Function: `scene_street_fight()`
This scene teaches immediate tactical consequences.
- Right-hand punch causes Robert to take damage and lowers effectiveness
- Left-hand punch succeeds and sets `isTactical = true`
Health reduction is reflected using the `Robert_Health` variable.

3. Superhero Bar (Flambae Scene)  
Function: `scene_bar_flambae()`
This scene affects public perception and relationship memory.
- Throwing water results in a mild impression
- Throwing alcohol amplifies chaos and awards more points
The choice updates `Blazer_Impression_Score`, which affects the epilogue.

4. Billboard Scene (Romance Route)  
Function:`scene_billboard()`
This is the emotional pivot point with Blonde Blazer.
- Choosing to kiss activates `isRomanticTensionActive`
- Letting the moment pass keeps tension unresolved
This decision directly impacts relationship outcomes in the ending.

5. Combat with Toxic  
Function: `scene_combat_toxic()`
This scene reflects Robert’s established personality.
- Punting shows creativity and restraint
- Stomping emphasizes brutal efficiency
Dialogue output changes depending on the value of `isMerciful`.

Epilogue Summary

Function:`epilogue_summary()`

The epilogue evaluates all stored variables and prints a personalized conclusion:
- Moral alignment is based on `isMerciful`
- Relationship impact depends on `Blazer_Impression_Score`
- Romance outcome depends on `isRomanticTensionActive`
- Tactical growth is reflected using `isTactical`
- Remaining health is displayed
This reinforces the idea that early decisions have long-term consequences.

Branching Logic Explanation
  Each scene functions like a station in a railway system.  
Player choices act as switches, while Boolean variables remain set throughout the program and determine which 
narrative tracks become available or altered. This structure demonstrates how simple conditional logic can simulate complex story branching.

How to Run the Program:
1. Compile the code using a C++ compiler.
2. Run the program.
3. Follow on-screen prompts to make decisions.


References:
Dispatch Episode 1 Walkthrough  
https://gam3s.gg/dispatch/guides/dispatch-episode-1-walkthrough/

C++ Visual Novel Logic Reference  
https://www.youtube.com/watch?v=ak78JicnW_E
