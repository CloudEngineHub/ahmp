# AHMP: Agile Humanoid Motion Planning with Contact Discovery

This is the repository of the paper "AHMP: Agile Humanoid Motion Planning with Contact Sequence Discovery" accepted at the 2025 IEEE-RAS 24th International Conference on Humanoid Robots (Humanoids)".

<p align="center">
<img width="500" alt="concept-figure" src="https://github.com/user-attachments/assets/20f7cfb1-a87d-43f1-8b8f-7573d8e76381" />
</p>

## Abstract
Planning agile whole-body motions for legged and humanoid robots is a fundamental requirement for enabling dynamic tasks such as running, jumping, and fast reactive maneuvers. In this work, we present AHMP, a multi-contact motion planning framework based on bi-level optimization that integrates a contact sequence discovery technique, using the Mixed-Distribution Cross-Entropy Method (CEM-MD), and an efficient trajectory optimization scheme, which parameterizes the robot’s poses and motions in the tangent space of SE(3). AHMP permits the automatic generation of feasible contact configurations, with associated whole-body dynamic transitions. We validate our approach on a set of challenging agile motion planning tasks for humanoid robots, demonstrating that contact sequence discovery combined with tangent space parameterization leads to highly dynamic motion sequences while remaining computationally efficient.

## Video Presentation
TBA

## Results

### Handrails Environment

Move 3m ahead in a handrail equipped environment. The generated motions take advantage of the robot’s dynamics to perform agile movements like hand-walking.


https://github.com/user-attachments/assets/807fb4b1-4b97-4881-8d9b-f15480fcdf36

### Chimney Environment

Discover sequences for climbing an emulated chimney. The robot is weaving from left to right and uses feet and hands to proper itself upwards.

#### Target 1m ahead

https://github.com/user-attachments/assets/dfb88fa6-f5e5-4a3f-a4a2-f72c8464f11e

#### Target 3m ahead

https://github.com/user-attachments/assets/564d7501-60d8-44e7-9203-8c64e76d7c45


AHMP can generate agile multi-contact whole-body trajectories for humanoid robots in a median time of 200 seconds for the average 
task. The image below shows the wall-time performance for handrails and chimney (low and high targets) environments. The box plots on the left show the median (black line) and the interquartile range (25th and 75th percentiles) over 20 successful replicates.

<p align="center">
<img width="500" alt="wall_times-1" src="https://github.com/user-attachments/assets/4c4f27db-fb9e-42d6-8350-c433a5c5c9f5" />
</p>

## Docker Installation

### Add coinhsl libraries (optional)
This code requires the HSL_MA97 linear solver internally with IPOPT. If you wish to use IPOPT with another linear solver, you can change the option in the code.
- Obtain an HSL license (free for academic use) from [here](https://www.hsl.rl.ac.uk/licensing.html).
- Extract coinhsl.zip folder in ci/ folder.

### Create container image
- `cd ci`
- `docker build -t ahmp`

### Run the container
- `cd [project_folder]`
- `./run_docker.sh'`



## Citing AHMP
To cite AHMP in your academic research, please use the following BibTeX entry:
```bibtex
@inproceedings{tsikelis2025ahmp,
               title={AHMP: Agile Humanoid Motion Planning with Contact Discovery},
               author={Tsikelis, Ioannis and Tsiatsianas, Evangelos and Kiourt, Chairi and Ivaldi, Serena and Chatzilygeroudis, Konstantinos and Mingo Hoffman, Enrico},
               booktitle={IEEE-RAS International Conference on Humanoid Robots (Humanoids)},
               year={2025}
               }
```
## Acknowledgments

The latest version of the trajectory optimization code can be found [here](https://github.com/upatras-lar/se3_trajopt).

This research was supported by the CPER CyberEntreprises, the Creativ’Lab platform of Inria/LORIA, the EU Horizon project euROBIN (GA n.101070596), the French National Research Agency (ANR) under the project ANR-24-CE33-0753-01 ([MeRLin](https://members.loria.fr/EMingoHoffman/merlin-2024-2028/)), the National Recovery and Resilience Plan Greece 2.0 funded by the European Union under the NextGenerationEU Program ([project MIS 5154714](https://lar.upatras.gr/projects/ibrics.html)).

<p align="center">
  <img width="150" alt="logo_inria" hspace=15 vspace=15 src="https://github.com/user-attachments/assets/f8749971-7ce8-40dc-ae68-cef5890c7982"/>
  <img width="80" alt="logo_cnrs" hspace=15 vspace=15 src="https://github.com/user-attachments/assets/96108418-2df4-4054-ac5b-b91b46c74b33"/>
  <img width="80" alt="logo_loria" hspace=15 vspace=15 src="https://github.com/user-attachments/assets/a6786fb5-39ff-4007-a086-e5dc377f8f08"/>
  <img width="150" alt="logo_ul" vspace=15 src="https://github.com/user-attachments/assets/83e56d7a-2d0c-4c34-8994-4e89e2fac954"/>
  <br>
  <img width="150" alt="logo_upatras" hspace=15 vspace=15 src="https://github.com/user-attachments/assets/cf2306bd-e62f-49dc-a031-cbb2cb73d5eb" />
  <img width="70" alt="logo_lar" hspace=15 vspace=15 src="https://github.com/user-attachments/assets/b579dc71-f6fc-42aa-b30e-85dcf141be7c" />
  <img width="150" alt="logo_archimedes" vspace=15 src="https://github.com/user-attachments/assets/98608a5d-7fcc-40f4-b166-c35e1a8c61ed" />
</p>
