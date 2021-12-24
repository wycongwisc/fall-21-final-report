# Final Report
- [Project Files](#project-files)
- [Bibliography](#bibliography)
- [Results](#results)
- [Process](#process)
- [Learning](#learning)
- [Self-Evaluation](#self-evaluation)

## Project Files

1. (VR robot simulation) https://github.com/wycongwisc/urdf-loader-test-vr
1. (CS559 framework) https://github.com/wycongwisc/CS559-Framework21
1. (CS559 Three) https://github.com/wycongwisc/CS559-Three21

For a demo of the robot simulation with VR support, see [here](https://wycongwisc.github.io/urdf-loader-test-vr/). For a demo of CS559 Graphics Town with VR support, see [here](https://wycongwisc.github.io/graphics-town-vr/wcong/for_students/12-grtown.html) (note this may not work with Oculus Quest).

## Bibliography

**Learning web-based VR**

1. Documentation for A-Frame, WebXR, and Three.
1. Entity-Component-System, Wikipedia.
1. Link Traversal and Portals in A-Frame, Mixed Reality Blog.
1. Entity Systems are the future of MMOG development, T-machine.
1. Using VR controllers and locomotion in THREE.js, Ada.is.

**Reviewing basic computer graphics concepts**

1. Transformation Matrices, Fundamentals of Computer Graphics.
1. Viewing, Fundamentals of Computer Graphics.

**Papers relating to our research area (depth perception, robot teleoperation in VR)**

1. A Motion Retargeting Method for Effective Mimicry-based Teleoperation of Robot Arms, Rakita.
1. Understanding Human Robot Interaction in Virtual Reality, Liu.
1. Effects of Onset Latency and Robot Speed Delays on Mimicry-Control Teleoperation, Rakita.
1. A Systematic Review of Virtual Reality Interfaces for Controlling and Interacting with Robots, Wonsick.
1. The Virtual and the Physical: Two Frames of Mind, Mutlu.
1. Comparing Human-Robot Proxemics between Virtual Reality and the Real World, Li.

## Results

**VR Robot Simulation**: an interactive, web-based robot simulation in VR with the ability to walk around (with parallax), remain stationary despite moving in real life (without parallax), and toggle on and off stereoscopic vision. The user is able to control the robot arm using the VR controller and perform a variety of pick and place tasks involving moving targets and randomized block sizes and positions. 

The VR portion of the robot simulation primarily uses Three.js and WebXR. The code lacks proper documentation, however I will be continuing this project next semester so it is not a huge issue (I will be sure to provide documentation whenever I do pass it off to somebody else).

In the future, the application can be used as a way to (1) evaluate how different aspects of a VR system influence robot teleoperation, and (2) perform a study. 

**CS 559 Framework**: an updated version of the CS 559 framework using the latest version of Three (r135). Students will now be able to enter VR for any Three scene and can fly around using the controller. Students can also enable various performance metrics for any scene. Apart from the VR additions, I updated all instances of `Geometry` to `BufferGeometry` and cleaned up the code, using `const` whenever appropriate and taking advantage of the `??` operator.

In terms of documentation, I added comments for all the code I added and seperated my Github commits so that they were as clear as possible (there are also additional comments in Github). 

*Note*: There are still a few things I (or someone else) needs to do including testing out the new type-checking system Three uses and testing out VR on the Quest.

## Process

This was my first exposure to programming and working with VR so I spent the first few weeks setting things up and exploring some different web-based technologies, most notably AFrame. Though I never ended up using it for anything (Three's integration with WebXR was good enough), I learned a lot. 

While Three.js and WebXR were pretty easy to get into, the lack of documentation regarding OS/browser/device compatibility was frustrating and it took me a while to figure out what was compatible with what. Up until I discovered Chrome Canary and was able to use the Rift, I also couldn't properly test my code at home and would have to run to the lab all the time to see if things actually worked (I was using a WebXR emulator at home but it was a poor indicator of whether things would work on the Vive/Quest).

Once I figured out all the compatibility issues and developed an efficient workflow, I was able to make some good progress. Implementing monoscopic vision and preventing the camera from translating in VR (no parallax) was challenging because neither Three nor WebXR provided a way to do this and I had to hack something together for both. Everything else with the robot simulation was pretty straightforward and updating the 559 framework was quicker than I expected.

## Learning

I had never even used a VR headset before this so in terms of technical things, everything I did this semester that was VR-related was completely new to me. I also learned a lot about teleoperation and robot manipulation (RelaxedIK).

As for non-technical things, the biggest thing I learned (and am still learning) was what to prioritize and how to allocate my time. It was hard to get myself to do research-related things when I had an exam or project deadline coming up, even if I knew I was well prepared. I think I naturally view tasks with strict deadlines (school work) as a higher priority and have the tendency to over-study even when I know my research work is more important for my future.

This was also my first semester doing research, so Pragathi and especially Yeping helped me understand what its like, most notably realizing the fact that a majority of everyone's "research" is spent debugging and that its not just me.

## Self-Evaluation

Overall, I'm happy with what I got done with the semester, especially on the technical side of things. I think I could have been more involved with the actual research part (reading papers and thinking about potential research ideas), which is something I want to improve on next semester. I would also like to spend more time in general, even if it means dropping a class/taking fewer credits.

As for advice, I would tell people not to become discouraged when something doesn't work and that progress is very non-linear. Sometimes it takes a good nights sleep to find the solution to a problem.