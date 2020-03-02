# What are the Security Concerns With Using Eye-tracking?

As eye-tracking technology has progressed over time, there are growing privacy implications of collecting vast amounts of this new kind of personal information.

## Scanpath

Unlike the ability to disguise our voice or change our appearance, eye movement is not under conscious control. There are various environmental factors at play which influence where our eyes gaze or what grabs our attention. Eye movements are condensed into fixations that approximate the focus of attention. Ordered in time, the sequence of fixations sequence comprises a scanpath.

This day may be coupled with details about the underlying area of interest thus creating a stronger notion of *what* was attended to and *how* attention varied. Even without knowledge of the area of interest, some scanpaths are highly stereotyped and recognizable. Knowing how and what people gaze provides a wealth of understanding. Yet gaze data for a single purpose such as evaluating a new UI can unintentionally reveal sensitive attributes of users when it is analyzed more deeply.

## Uniquely Identify Individuals

Gaze patterns can uniquely identify individuals. For example, with machine learning, we can identify individuals whose gaze has been tracked using eye trackers. At the Eye Movement Verification and Identification Competition in 2012, 
four datasets included 250-1000 Hz recordings from
two eye trackers, as participants followed a jumping
dot. The best models achieved accuracy from 58% to
almost 98% using models of movement speed and
direction.

Even if the individual’s gaze data has not previously
been recorded and associated with his or her identity,
one could use attributes derived from the gaze patterns
to approximate that identity. For example, gender identification effectively halves the global search space. By
carefully selecting combinations of attributes, identity predictability can be greatly increased.

## Privacy Loss

The data that is collected through gaze tracking results
in privacy losses of two kinds: 

**Identity of an Individual**

The user’s unique gaze pattern allows fingerprinting. Part of the identity inference are also several bio-indicators, including health status, both momentary and longer term, age, and fatigue. 

**Inference of Interests**

When annotated by the semantics of the
content displayed, the measurement of interest in
items displayed on screen reveals political, sexual,
cultural or other lifestyle preferences.

**Scale**

The scale of tracking data is a key consideration; if a
participant performs one laboratory experiment, then
that data is unlikely to be released and there is probably little impact to the subject. But when eye trackers
are pervasive and share their data with a central
infrastructure, the opportunity to track individuals
across time and place now becomes real.

source: [Privacy Considerations for a Pervasive Eye Tracking World](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/eyetracking-privacy-cameraready.pdf)