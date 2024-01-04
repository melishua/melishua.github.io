---
layout: page
title: Wearable Visual Memory Prothetic for Prosopagnosia​
description: A computer-centred healthcare system for prosopagnosia patients utilizing machine learning and clinical training. Heads up! This will redirect to my old home page, migration to github page is in progress.
img: assets/img/wearable_cropped.jpg
# redirect: https://zhiyangpan.com/wearable_prosopagnosia/
importance: 3
category: research
related_publications: 9283058
---

**Leverage the power of technology to develop a human-centred system to help people with prosopagnosia.**

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/wearable_project.jpg" title="Wearing ISEE" class="img-fluid rounded z-depth-1" %}
    </div>
    <i>"Face Recognition and Rehabilitation: A Wearable Assistive and Training System for Prosopagnosia": <a href="assets/img/IEEE_SMC2020_prosopagnosia">PDF</a> </i>
</div>
<br>

Our work was presented and published at SMC2020:
<div class="row">
<iframe width="358" height="200" src="https://www.youtube.com/embed/bd7rJAimunw?si=HWncFO3PtL3Hd7yT" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

## What is prosopagnosia?
Prosopagnosia (commonly known as **“face-blindness”**) is an impairment in recognizing or remembering (visual memory) faces due to neurological disorder <a href="https://www.psychologytoday.com/ca/basics/prosopagnosia">[1]</a>. Instead of having an inability to see a face – two eyes, one nose, and a mouth – the patients are unable to recognize or remember faces. Thus, prosopagnosics cannot distinguish familiar people by face. Depending on the level of severity, other symptoms range from unable to identify self image, to differentiating faces from other objects <a href="https://www.ninds.nih.gov/Disorders/All-Disorders/Prosopagnosia-Information-Page">[2]</a>.

Social awkwardness, anxiety or depression are common complications for prosopagnosics <a href="https://www.ninds.nih.gov/Disorders/All-Disorders/Prosopagnosia-Information-Page">[2]</a>. Relationship development and maintenance are difficult as patients have trouble recognizing family members and friends [2]. While some individuals tend to avoid interactions with people or large social events, others might have developed various social phobias <a href="https://www.thecut.com/2015/07/what-its-like-to-be-profoundly-face-blind.html">[3]</a>.


## Project Goal
The goal of this project was to develop a computer-centred healthcare system for prosopagnosia patients. This system recognizes faces through a camera in real-time using an open-sourced face recognition library, facilitates face-name management with the option to add facial feature annotations to each face, and provides long-term at-home training to improve their face-processing skills.


## ISEE
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/isee_system_diagram.jpg" title="ISEE system diagram" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        <p>An all-in-one Android application that includes features during and after social interactions in a single device.</p>
        <p>The system has two major modes according to the identified purposes above: <i><b>real-time face recognition mode</b></i> and <i><b>at-home self-training mode</b></i>. The overview of the system design can be organized into three parts: hardware component, real-time component, and training component (left diagram) using three different colours.</p>
    </div>
</div>

### Wearable device
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <p>The wearable component of the system: camera + wearable medium</p>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/isee_glasses.jpg" title="ISEE glasses" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Real-Time Recognition
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <p>Daily memory assistant prompting name reminder upon social situtations</p>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/isee_recongition_mode1.jpg" title="ISEE real-time mode" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Self-Training Tool
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <p>Mimic clinical visual memory training</p>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/isee_training_mode.jpg" title="ISEE training mode" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

## ISEE Implementation:
<div class="row">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/isee_cameras.jpg" title="ISEE system diagram" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <h3>Wearable devices</h3>
        <p>Besides the PI-camera integrated glasses, the users have various options to hold the phone for the real-time mode: to plug in <i><b>a wearable set</b></i> as the video input source under the hardware component or use the <i><b>phone’s integrated camera</b></i>. The phone can be held by hand, put in the front pocket, or hang by the phone lanyard.</p>
    </div>
</div>
<div class="row">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/isee_recongition_mode2.jpg" title="ISEE system diagram" class="img-fluid rounded z-depth-1" %}
        {% include figure.html path="assets/img/isee_recongition_mode3.jpg" title="ISEE system diagram" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <h3>Real-Time Recognition Mode</h3>
        <li>Video streamed from the perspective of the user to the interacting human subject.</li>
        <li>Audio notification is given on contact information if match found, else prompt as unknown.</li>
        <li>The user is able to add a new person as the contact through selecting training images.</li>
        <li>Supports multi-face recognition.</li>
        <br>
        <p>As we can see from the first screenshot that my face was not recognized by ISEE before getting added to the contact list.</p>
        <p>Then we go ahead to add me as a new person by selecting the image frame that ISEE saved for unknown faces.</p>
        <p>After that, ISEE will train and update its model immediately.</p>
        <p>At the end, we can see that ISEE can recognize my face and report “Melissa” both visually and auditorily.</p>
    </div>
</div>
<div class="row">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/isee_training_mode2.jpg" title="ISEE system diagram" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <h3>At-Home Self-Training Mode</h3>
        <p>The at-home self-training mode is an interactive interface that allows the user to train on their face-naming ability.</p>
        <p>It is a standalone mode that users can use before or after the real-time training mode.</p>
        <li>Mimic clinical training to train on face-naming ability</li>
        <li>Face images fetch from the user’s contact</li>
        <li>One training cycle contains 15 rounds of sections</li>
        <li>At the end of each round, the training accuracy and total reaction time will be saved into the database for future analysis</li>
        <li>Users can view and edit their contact list information as shown in the last figure</li>
    </div>
</div>

## Experiments
### Real-Time Recognition Mode
The team set up the system to test the average reaction of real-time face recognition. We calculated the average reaction time of eight tests. On average, it takes 0.4081 second to compute and output the result.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/isee_experiment1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### At-Home Self-Training Mode
A total of 10 participants were divided into one experimental group and one control group, where each group had five participants. Each participant performed five blocks of ten trails of the training using ISEE.

For the experimental group, participants were required to perform face-feature naming upon incorrect selection of a face image. The participant has five seconds to list three facial features with the correct image.

For the control group, participants did not perform feature naming where they learn the correct face for five seconds on their own. The hypothesis is that face-feature naming allows the participant to acquire a better holistic understanding of the training face image.

I and my team recorded reaction time and accuracy for each block of the face recognition task. The figures below show participants’ accuracy and reaction time in each block of trials. It can be seen that there is a general improvement in accuracy and reaction time for both the experimental and control group where the experimental group has a slightly better performance.

Accuracy and Reaction Time Trend: 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/isee_experiment2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

## Future Directions
* Real Prosopagnosia Patient
* EEG Signal Feedback
* Face Flashback Training
* Wearable Wifi/bluetooth Integration
* Camera Upgrade
* Computation Speed Optimization
