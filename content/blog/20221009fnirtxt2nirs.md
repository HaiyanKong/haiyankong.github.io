---
title: "Convert fNIRS data.txt to data.nirs"
date: 2022-10-09
author: Haiyan Kong
slug: 20221009/fnirtxt2nirs
draft: false
tags: fnirs
---

{{< alert "circle-info" >}}

**Summary**: 

- Convert the data recorded by SHIMADZU (data.txt) to HOMER readable format (data.nirs).
- Also on Github: [HaiyanKong/tutorial_fNIRStxt2nirs](https://github.com/HaiyanKong/tutorial_fNIRStxt2nirs)

{{< /alert >}}

## Step1: Prepare the followings

- MATLAB2013b

- [homer2](https://www.nitrc.org/plugins/mwiki/index.php/homer2:MainPage)

- [Shimadzu2nirs](https://www.nitrc.org/projects/shimadzu2nirs/)

## Step2: Set the path

Set **homer2**  in the path of MATLAB2013b.

{{<figure src="/blog/en/20221009fnirtxt2nirs/20221009fnirtxt2nirs-1.png" caption="Figure 1">}}

## Step3: Open the SDgui

- Set your work path at  *D:\toolbox\homer2\PACKAGES\SDgui* (change the path in the computer)

- Run **SDgui.m** in MATLAB2013b.

{{<figure src="/blog/en/20221009fnirtxt2nirs/20221009fnirtxt2nirs-2.png" caption="Figure 2">}}

- Next, a prompt will appear for you to select a file. Simply click "Cancel" to proceed.

{{<figure src="/blog/en/20221009fnirtxt2nirs/20221009fnirtxt2nirs-3.png" caption="Figure 3">}}

- Then you will see this.

{{<figure src="/blog/en/20221009fnirtxt2nirs/20221009fnirtxt2nirs-4.png" caption="Figure 4">}}

## Step4: Create the SD File

- Base on your optodes arrangement to fill in the blank in the sources and detectors.
  - Note: z is always 0.


{{<figure src="/blog/en/20221009fnirtxt2nirs/20221009fnirtxt2nirs-5.png" caption="Figure 5">}}

- When you complete setting the sources and detectors , then click the number, you will get the channel.

{{<figure src="/blog/en/20221009fnirtxt2nirs/20221009fnirtxt2nirs-6.png" caption="Figure 6">}}

{{<figure src="/blog/en/20221009fnirtxt2nirs/20221009fnirtxt2nirs-7.png" caption="Figure 7">}}

- After setting channels, and you need to fill in the “Lambda” based on your data acquiring device.

{{<figure src="/blog/en/20221009fnirtxt2nirs/20221009fnirtxt2nirs-8.png" caption="Figure 8">}}

- Provide a name for the SD file, and let's call it "test.SD," including the ".SD" suffix.

{{<figure src="/blog/en/20221009fnirtxt2nirs/20221009fnirtxt2nirs-9.png" caption="Figure 9">}}

- Click the ''Save", and in the new window, you need to choose the "units", here is "mm"

{{<figure src="/blog/en/20221009fnirtxt2nirs/20221009fnirtxt2nirs-10.png" caption="Figure 10">}}

- Your SD file is saved successfully ! Just close the SDgui.

{{<figure src="/blog/en/20221009fnirtxt2nirs/20221009fnirtxt2nirs-11.png" caption="Figure 11">}}



## Step5: Convert!

- Put **the data need to convert (.txt)**, **3 files from Shimadzu2nirs.zip** and **test.SD created in step 4**  together, and set the MABLAB work path to them.

{{<figure src="/blog/en/20221009fnirtxt2nirs/20221009fnirtxt2nirs-12.png" caption="Figure 12">}}

- Run the **Shimadzu2nirs.m**.

{{<figure src="/blog/en/20221009fnirtxt2nirs/20221009fnirtxt2nirs-13.png" caption="Figure 13">}}

- Then you will get the **.nirs** data file !

{{<figure src="/blog/en/20221009fnirtxt2nirs/20221009fnirtxt2nirs-14.png" caption="Figure 14">}}

