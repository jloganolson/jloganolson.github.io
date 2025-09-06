---
layout: post
title: "Back in the saddle!"
date: 2025-09-06 13:00 -0700
---
This was my first week getting to tinker full time!

![posing the G1 in blender](assets/img/250906/rigged-g1-blender.png)

## tl;dr
* Updated my G1 MJCF and USD with new 3D-printed forearms
* Vibecoded basic MJCF -> rigged glTF .glb version of the Unitree G1 [(dumped code on to github here)](https://github.com/jloganolson/g1-blender-arms/tree/main)
* Created a background script that captures my desktop every few seconds and builds a timelapse at the end of teh day
* Stood up FastVLM to see how well it could grok the desktop capture 

## Learnings
* Vibecoding did really well with the glTF creation beuracracy but got really tangled up in the transform/matrix logic - should've tackled smaller chunks and maintained awareness of what it was generating earlier on
* No clear way to do formal structurd output with FastVLM (e.g. Outlines) but prompt engineering was sufficient for simpler schema (and given it's a 1.5B model, you should be doing simple)
* FastVLM is promising for very simple cases (is the screen showing email, spotify, or coding?) - will probably use as a PII filter before sending visuals to Gemini
* Should start each day asking why I'm doing something - the rigged glTF is a cool idea but not necessary to just do one pose, especially given how much work is left just to add constraints and export poses back to the robot

## Next steps
* Prototype daily report from FastVLM/gemini/script from daily screencaps
* Do the simplest possible thing to get the pose I want and move on with my current goal (quadruped G1) - probably just joint sliders in Mujoco or Isaac 

