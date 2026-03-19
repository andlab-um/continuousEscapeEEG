# continuousEscapeEEG    <img src="./summary_figure.jpeg" align="right" width="500px">

#[![Paper](https://img.shields.io/badge/Paper-preprint-blue)](https://doi.org/10.1101/2024.01.16.575785)
#[![Twitter URL](https://img.shields.io/twitter/url?label=%40ANDlab3&style=social&url=https%3A%2F%2Ftwitter.com%2FANDlab3)
#](https://twitter.com/ANDlab3)


> From [Affective, Neuroscience, and Decision-making Lab](https://andlab-um.com)



## Description
Code and data for: 'Intracranial and Scalp EEG Evidence of Escape Strategies Under Continuous Threat'.
preprint: [https://doi.org/10.1101/2024.01.16.575785](https://doi.org/10.1101/2024.01.16.575785)

## Abstract
Understanding the neural mechanisms underlying human escape behavior in continuous threat environments remains a critical challenge in cognitive neuroscience. Here, we employed a novel, ecologically valid paradigm combining behavioral trajectory analysis with high-spatial resolution intracranial stereo-electroencephalography (SEEG; Study 1) and scalp electroencephalography (EEG; Study 2) to investigate neural signatures associated with escape responses under continuous threats. In the SEEG study, we found that trial-level human escape behavior could be characterized by distinct behavioral metrics. At the neural level, the vmPFC and amygdala were found to encode these behavioral features. The subsequent EEG study further replicated both the behavioral patterns and electrophysiological effects observed in the SEEG dataset. These findings reveal conserved behavioral patterns of human escape across distinct participant populations, and uncover the corresponding cortical and subcortical neural mechanisms underlying adaptive defensive responses to continuous threats.

## Experiment
<img src="./paradigam.jpg">
We developed an ecological paradigm based on the threat imminence continuum model. This paradigm could investigate the escaping behavior and underlining mechanism under different threat stages, including safe, pre-encounter, post-encounter, and circa-strike. 
In this experiment, participants need to collecting reward (food) and back to the safe zone while evading predators. All elements were positioned within a 2D square space measuring 2 * 2 units. A spatial coordinate system was used to represent the positions of different elements, with the geometric center of the square set as the origin (0,0). Participants were represented by a blue circle, while the safe zone was depicted as a green rectangle located at the bottom edge of the map. For each trial, 5 rewards were randomly generated within the reward zone at the center of the map. To increase the difficulty of collecting all rewards, a minimum distance of 0.12 units was maintained between any two rewards . Two types of predators could appear in the experiment: direct attack predators and divert attack predators, represented by red and orange triangles, respectively. Participants could move freely within the map by using directional keys at a speed of 0.4 unit/s.

## Data path and analysis



## Notes
If you want to run the code, pay attention to the environment configuration and the file path.

> package required:
> Python

```bash
mne
numpy
scipy
pandas
nibabel
matplotlib  
```
