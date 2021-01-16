# Video Translation

Our basic goal is to take a video and an image / another video and merge them.




# Setting Up Environment

We want to set up a common "environment" for everyone to make sure that we're all able to run the same code.

We'll do most of our work on UChicago's linux servers because that provides a common operating system. 



# Computing

Jin has access to a lot of GPU computing resources, but he doesn't have the ability to share those resources with everyone else. Here's what we'll do for computing.

## UChicago Linux

There's GPU resources at linux.cs.uchicago.edu, but it's limited in many ways. You can use this to work on / test out your code / debug, but DO NOT run long-lasting code. If you want to make a long run, please send the script to Jin and Jin will run that script on his computing resources.


## Process For Accessing GPU Compute

This is a very simple starting command:

```
ssh UCHICAGOID@linux1.cs.uchicago.edu
srun -p titan --pty --cpus-per-task 4 --mem 500 -t 0-01:00 /bin/bash
```

If you want an explaination on what this is doing, check [this](https://howto.cs.uchicago.edu/slurm#interactive_jobs) out. 

## UChicago Linux Resources to Look at:

* https://howto.cs.uchicago.edu/slurm:peanut
* https://howto.cs.uchicago.edu/slurm



# Contributing 

We’ll push all our code [here](https://github.com/MLUChicago/VideoTranslation). You don’t have direct access to that repository. What you want to do is fork the repo (aka make a copy) on to your own account. When you modify your code, you have unlimited access to your own copy and you can push to your own account. When you feel that you are ready, make a pull request to `MLUChicago/VideoTranslation` so that you can push your changes to that repository.

By implementing this process, this reduces the amount of conflict that you will have with your teammates.

## Notes
Please don't push large files.