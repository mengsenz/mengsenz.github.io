[Publications](/pubs.md) | [CV](/docs/cv_Mengsen_20180414.pdf) | [Google Scholar](https://scholar.google.com/citations?user=YfVxfjMAAAAJ&hl=en) | [Current Lab](http://www.ccs.fau.edu/hbbl3/) | [ResearchGate](https://www.researchgate.net/profile/Mengsen_Zhang) | [Twitter](https://twitter.com/Mengsen) | [Contact](contact.md)

## Who am I
Without getting into the biggest philosophical question, I am Mengsen Zhang, currently a Ph.D. student in the Center for Complex Systems and Brain Sciences at Florida Atlantic University, under the mentorship of Drs. Emmanuelle Tognoli and J. A. Scott Kelso. I'm interested in how coordination patterns form and change in biological and social systems on multiple spatiotemporal scales. (...more: [Why Complexity](/complexity.md))

## Current research
During Ph.D training, I have been studying human social coordination at the level of physiology, neural dynamics and social groups, both experimentally and theoretically. Overall, my work follows two themes:

### Multiagent social coordination
A lot of works on coordination phenomena focus on either systems of very few (often 2) or very many component (better to be infinite). The in-between was somewhat neglected. To understand coordination dynamics across scales, I felt necessary to bridge this gap between the very few and very many by studying the middle. I have developped a new experimental paradigm (+ an aparatus) to study the coordination of rhythmic tapping among eight humans in a controlled environment - network connectivity and individuals' frequency of movement can be systematically manipulated. 

We have recently published a paper ([here](https://doi.org/10.1371/journal.pone.0193843)) about the first experiment using this paradigm, dubbed the "Human Firefly" experiment (because people's taps were displayed as flashes of LEDs, which looked like glowing fireflies in the dark). At micro level (interpersonal relations), we identified what phase relations people coordinated in (metastably, i.e. people come together and separate recurrently); at macro level (intergroup relations), we identified the critical level of frequency diversity that led to segregation between frequency groups. 

![Phase transition in pairing](/pics/transitionof8.png)

Following the experiment, we have developped a mathematical model which successfully captured these key observations. The model also provided dynamic explanations for some of the statistical features in the experimental data. More importantly, it connects small-scale and large-scale theories of coordination. The manuscript is in preparation and will soon be submitted. 

Along the way, I have also done some exploratory work on how to find phase transitions in coordination patterns in, for a start, eight-person coordination. This is when I came across Computational Topology (homology in particular), which later led to the discovery of a transition between isomorphic graphs in the figure above (A1 to A2 to A3, corresponding to graphs in D). Some proof-of-concept work is to be organized into a paper or report.   

### Human-Virtual Partner interaction

I have conducted a series of experiments to look "within" the person during social coordination, using a recently developped paradigm named the Human Dynamic Clamp ([here](https://doi.org/10.1073/pnas.1407486111)). In the paradigm, a person coordinate his/her movement with a "Virtual Partner" (VP), whose movement is driven by a empirically grounded model of human coordination (Haken-Kelso-Bunz equations). The nice thing is that we can quantitatively set the boundary conditions of the dyadic coordination by choosing model parameters. 

![VPI Emotion](/pics/VPI_SPR_gd.jpg)

I first used it to study how emotional arousal (measured by skin potential response) in human particpants was affected by social coordination and found that humans had greater emotional responses when their coordination with the VP was stable and when they thought the VP's behavior was controlled by a human (they did not know it was controlled by the model all the time). This work has been published [here](https://doi.org/10.1016/j.ijpsycho.2016.04.001). Two more experiments were done with participants' neural activities (EEG, fMRI) recorded. The data analyses is ongoing.  

## Other passion projects
### Low-cost engineering for real-time experiments
Since I studies dynamic patterns, the real-timeness of experimental equipments are essential, especially when there is a closed-loop component (for which long latency may change coordination patterns qualitatively). When the design of the behavioral paradigm gets a bit novel, proprietary hardwares becomes really cumbersome and in some cases cannot at all satisfy the needs of the experimenter (e.g. for the "Human Firefly" experiment mentioned above). After a brief initial skepticism, I fell rapidly in love with open hardwares, which includes Arduinos (microcontrollers) and open source sensors. They gave me highly flexible control of real-time signal processing at an extremely low cost (comparing to, say, something from the National Instruments), along with accessible circuit schematics which I can modify to suit the need of a particular experiment. Without open hardwares, it would have not been possible to build a satisfactory apparatus (in a reasonable time frame) for the "Human Firefly" experiment mentioned above. I have since used them for varies experiments (for the behavioral components; you really do need something proprietary for MRI) and helped colleagues to incoporate them into their experiments. 
### CUDA programming
At the beginning of my Ph.D. training, I found some signal processing procedures rather time-consuming (e.g. continuous wavelet transform, CWT). I started to look into using graphic processing units (GPU) to accelerate these repetitive computations and wrote a CWT algorithm with parallel convolution using CUDA C/C++ (a toolkit developed by NVIDIA for computation on GPU). With some moderate success, I began to think about a better application of CUDA - to do parameter exploration in parallel for a given nonlinear dynamical system. This idea was eventually realized when I was simulating eight-oscillator coordination problems (in order to under phenomena in the "Human Firefly" experiment above). The result surprised myself - more than one Terabyte of simulated data can be generated under 2 hours (which would take months with MATLAB's ode15s for my particular model), which took more than 6 hours to write on a harddrive (later I realized that there is no need to save the data if the data can be simulated faster than it can be read from hard drive). This kind of performance can be achieved by using the most basic CUDA runtime library, not so much however by using higher level ones (e.g. boost) due to unnecessary data transfers between CPU and GPU memories.  
### Topology

### Pattern formation
