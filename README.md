# **Two Dimensional Histogram Filter**

## Sensing and Movement in 2D in Python and C++

### Explore the code, Implement a Feature, and Fix a Bug

---

**Two Dimennsional Filter with Feature and Bug Project**

The goals / steps of this project are the following:

1. Prototyping in Python
* Explore the code to get a feel for how this code base is organized and what everything does.
* Implement a feature by writing code that gets the robot moving correctly.
* Fix a bug by implementing motion, identify what the bug is and take steps to reproduce it; then identify the cause and fix it.

2. Writing from Python to C++
* Break down functions in Python into .h and .cpp files

3. Optimize code in C++
* techniques used include:
  - reserving memory for vectors
  - passing larger variables to functions by reference
  - removing variables that were not needed
  - modifying vectors in place when possible instead of creating new vector variables
  - iterating with ++i instead of i++
  - removing dead code (lines of code that were in the files but no longer being used)
  - avoiding extra for loops especially nested for loops when possible
  - avoiding extra if statements
  - using static and const keywords when appropriate

[//]: # (Image References)

[image1]: ./Result_Images/1.png "1"
[image2]: ./Result_Images/2.png "2"
[image3]: ./Result_Images/3.png "3"
[image4]: ./Result_Images/4.png "4"

### README

- The implementation of 2D histogram filter can be found in

  * [Python](./Python Version/Histogram_Filter_2D.ipynb) 

  * [C++](./C++ Version) 

  * [Optimized C++](./Optimized C++ Version/main.cpp) 


The below image shows the visualization of the sense function in .ipynb: 

![alt text][image3]


### Steps used:

#### 1. Exploring the code

* Import helpers, localizer and simulate files.

  - red star: robot's true position. 
  - blue circles: the strength of the robot's belief that it is at any particular location.
  - This shows a 5x5 robot world and creates a simulation to shows the initial beliefs of its position

![alt text][image1]

* At this stage, the robot doesn't have a working sense function.

  - As you can see, the robot's beliefs aren't changing. No matter how many times we call the simulation's sense method, nothing happens. The beliefs remain uniform.

  - Ideally we want the biggest blue circle to be at the same position as the red star.

![alt text][image2]

#### 2. Implement a 2D sense function.

* Implement a sense function in [localizer.py](./Python Version/localizer.py)

![alt text][image3]


#### 3. Identify and Reproduce a Bug

* A user of your robot called tech support with a complaint

    "So I was using your robot in a square room and everything was fine. Then I tried loading in a map for a rectangular room and it drove around for a couple seconds and then suddenly stopped working. Fix it!"

* Now we have to debug. We are going to use a systematic approach.

  - 1. Reproduce the bug
  - 2. Read (and understand) the error message (when one exists)
  - 3. Write a test that triggers the bug.
  - 4. Generate a hypothesis for the cause of the bug.
  - 5. Try a solution. If it fixes the bug, great! If not, go back to step 4.

  * Reproduce the bug
    
   - rectangular environments seem to be causing the bug as seen

 ![alt text][image4]

  
