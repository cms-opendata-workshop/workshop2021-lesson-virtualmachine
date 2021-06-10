---
title: "Introduction"
teaching: 10
exercises: 0
questions:
- "What are virtual machines?"
- "What are virtual machine images?"
- "Why are they needed for studying CMS open data?"
objectives:
- "Acquire a working knowledge of what a virtual machine is."
- "Differentiate between a hypervisor and virtual machine images"
- "Understand the advantages and disadvantages of using virtual machines."
keypoints:
- "A virtual machine is an emulation of a computer system that can run within another host system."
- "A hypervisor is a program that creates virtual machines from virtual machine image files and runs them virtually."
- "Virtual machines can be used to run over CMS open data in a very intuitively way.  However, they take up a lot of resources, are less efficient than real machines, and harder to use for batch processing."
---

> ## Helpline
>
> Remember that we are always available to help.  Our [Mattermost][mattermost] channel is open.
{: .callout}

## The need for VMs

CMS open data and legacy data, even though still exciting and full of research potential, are already a few years old. Because of the rapidly evolving technologies, the computing environments that were used to analyze these data are already ancient compared to the current, bleeding edge ones.

Therefore, in order to maintain our ability to study these data, we have to rely on technologies that help us preserve adequate computer environments. One way of doing this is by using virtual machines.

In simple words, a [virtual machine](https://en.wikipedia.org/wiki/Virtual_machine) is an emulation of a computer system that can run within another system. The latter is usually known as the host.

## Open data releases, CMSSW versions and operating systems

CMS open data from our 2010 release can be studied using `CMSSW_4_2_8`, a version of the [CMSSW](https://github.com/cms-sw/cmssw) software that used to run under Scientific Linux CERN 5 (slc5) operating system.  Likewise, open data from our 2011/2012 release used `CMSSW_5_3_32` under Scientific Linux CERN 6 (slc6).

The virtual machines that are used to analyze these data, therefore, need to consider all these compatibility subtleties.  They have to offer the correct operating system so the right version of CMSSW can be used to manipulate the dataset of interest.

## Virtual machine images

In practical terms, a virtual machine image is a computer file that has all the right ingredients to create a virtual computer inside a given host by the process of [virtualization](https://youtu.be/FZR0rG3HKIk).  This file, however, needs to be *decoded* and run by a virtual machine interpreter, usually known as [hypervisor](https://en.wikipedia.org/wiki/Hypervisor), which runs on the host machine.  The hypervisor we are going to use in this lesson is the Oracle's [VirtualBox](https://en.wikipedia.org/wiki/VirtualBox).

## CMS VM images

The most current images for CMS open data usage are described separately in the CERN Open Portal site for [2010](http://opendata.cern.ch/record/250) and [2011/2012](http://opendata.cern.ch/record/252).  In later episodes we will be using the latter image file.

## Advantages and disadvantages of using VMs

For the end user, VMs really look and feel like a physical machine, so working with them is easy and very convenient. The CMS VMs, in particular, come equipped with the [ROOT](http://root.cern.ch/) framework (although with an older version), [CMSSW](http://cms-sw.github.io/) and [CVMFS](https://cvmfs.readthedocs.io/en/stable/index.html) access, all the goodies you need to start analyzing data right away.

However, VMs are usually heavy and take up a lot of the host resources, which can affect performance.  Also, it is more difficult to run batch jobs (large scale processing) with them.

{% include links.md %}
