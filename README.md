# Video Translation

Our basic goal is to take a video and an image / another video and merge them.




# Setting Up Environment

We want to set up a common "environment" for everyone to make sure that we're all able to run the same code.

We'll do most of our work on UChicago's linux servers because that provides a common operating system. 

We only have to set this environment up once.

1. ssh to CNETID.fe.ai.cs.uchicago.edu
2. Run:

```
conda create --name video_translation python=3.7
conda activate video_translation
conda install pytorch torchvision torchaudio cudatoolkit=11.0 -c pytorch
conda install matplotlib scikit-image scikit-learn scipy
pip install opencv-contrib-python
```
3. Check that GPU is visible:

First make sure that you enter into a GPU node. To enter, you need to execute a `srun` command, like the one below.

Run Python and then execute 
```
import torch
torch.cuda.is_available()
```

It should say `True`.



# Computing

Jin has access to a lot of GPU computing resources, but he doesn't have the ability to share those resources with everyone else. Here's what we'll do for computing.

## UChicago Linux

There's GPU resources at fe.ai.cs.uchicago.edu, but it's limited in many ways. You can use this to work on / test out your code / debug, but DO NOT run long-lasting code. If you want to make a long run, please send the script to Jin and Jin will run that script on his computing resources.

Also, not many people know about the GPU resources, so it's best not to share that the the GPU resources exist to other people. The more people who use the resources, the less resources you have to use.


## Process For Accessing GPU Compute

This is a very simple starting command:

```
ssh UCHICAGOID@fe.ai.cs.uchicago.edu
srun -p general --gres=gpu:1 --pty --cpus-per-task 4 --mem 500 -t 0-01:00 /bin/bash
```

If you want an explaination on what this is doing, check [this](https://howto.cs.uchicago.edu/slurm#interactive_jobs) out. 

## UChicago Linux Resources to Look at:

* https://howto.cs.uchicago.edu/slurm:peanut
* https://howto.cs.uchicago.edu/slurm



# Contributing 

We’ll push all our code [here](https://github.com/MLUChicago/VideoTranslation). You don’t have direct access to that repository. What you want to do is fork the repo (aka make a copy) on to your own account. When you modify your code, you have unlimited access to your own copy and you can push to your own account. When you feel that you are ready, make a pull request to `MLUChicago/VideoTranslation` so that you can push your changes to that repository.

By implementing this process, this reduces the amount of conflict that you will have with your teammates.

## Notes
Please don't push large files to your git repo. For example, do not push datasets to the repositories.

To ignore certain files, put those files in `.gitignore`.



# Things To Keep In Mind




# Acknowledgements

This work is a modification of https://github.com/jiupinjia/SkyAR.