# Network Bending as Circuit-Bending Inspired Live Neural Synthesis Hacking

## Abstract

Circuit bending has long framed technical malfunction and misuse as sites of musical invention, enabling non-expert, hands-on engagement with electronic sound circuits through the practice of an immediate canvas. This paper articulates *Network Bending* as a circuit-bending–inspired approach to neural audio synthesis, making its connection to the tradition and ethos of circuit bending explicit. Network Bending is presented here as realtime, hands-on modification of neural network parameters—specifically weights and biases—during sound generation, where instability, breakdown, and opacity become compositional material.

The paper situates this practice within histories of musical hacking and instrument repurposing, and introduces an open-source Network Bending tool that enables parameter-level intervention in neural audio models within a realtime environment. Drawing on repeated use in performances and workshops, we introduce the *Bending Log* as a compositional technique for documenting and reusing exploratory interventions across models and performance contexts, and present a complementary *Network Blending* experiment that combines corresponding parameter spaces across models. We further reflect on workshop-based dissemination and community uptake, positioning Network Bending as an instrument-centered performance practice, a pedagogical tool, and an exploratory engineering approach for engaging with the internal dynamics of neural audio systems.

---

## Example Bending Log

| id  | name                                                  | operation          | result                                                                                                                          |
| --- | ----------------------------------------------------- | ------------------ | ------------------------------------------------------------------------------------------------------------------------------- |
| 17  | pretrained.decoder.input_latent_bottleneck.0.bias     | roll to the right  | produce more harmonic and brighter timbres                                                                                      |
| 17  | pretrained.decoder.input_latent_bottleneck.0.bias     | squeeze            | sharper, more compressed sound (a bit like OTF)                                                                                 |
| 24  | pretrained.decoder.input_latent_bottleneck.6.weight   | roll to the right  | smear the transients                                                                                                            |
| 26  | pretrained.decoder.input_latent_bottleneck.7.weight   | scale              | low – lower volume, higher dynamics<br>mid – introducting distortion<br>high – introducing extra tonal timbral elements         |
| 32  | pretrained.decoder.input_features_bottleneck.3.weight | various            | various operations embellish different parts of the spectrum in a difficult to explain way                                      |
| 34  | pretrained.decoder.input_features_bottleneck.4.weight | flip               | add a lot of highs                                                                                                              |
| 36  | pretrained.decoder.input_features_bottleneck.6.weight | draw               | various interesting short-term timbral glitches                                                                                 |
| 36  | pretrained.decoder.input_features_bottleneck.6.weight | roll               | effects similar to highpass / lowpass filtering                                                                                 |
| 37  | pretrained.decoder.input_features_bottleneck.6.weight | offset up          | bring up brightness and detail                                                                                                  |
| 40  | pretrained.decoder.gru.weight_ih_l0                   | roll               | abrupt timbral changes, from slight smearing to complete deconstruction                                                         |
| 40  | pretrained.decoder.gru.weight_ih_l0                   | scale              | lower values – rhythmic modulation<br>higher values – distortion                                                                |
| 40  | pretrained.decoder.gru.weight_ih_l0                   | drawing            | drawing in area around 75–90% of the array brings timbral changes without affecting temporal structure                          |
| 41  | pretrained.decoder.gru.weight_hh_l0                   | scale              | expanding – interesting array of temporal glitches<br>contracting – timbral shift                                               |
| 41  | pretrained.decoder.gru.weight_hh_l0                   | drawing            | lower half – rhythmic modulation<br>upper half – distortion<br>overall – a spectrum of glitches, timbral shifts and modulations |
| 44  | pretrained.decoder.gru.weight_ih_l1                   | scaling            | contracting – fast rhythmic modulation                                                                                          |
| 44  | pretrained.decoder.gru.weight_ih_l1                   | rolling            | all kinds of timbral shifts                                                                                                     |
| 59  | pretrained.decoder.inter_mlp.7.bias                   | scaling, offseting | low pass filtering                                                                                                              |
| 58  | pretrained.decoder.inter_mlp.7.weight                 | offseting          | upwards – adding noise and reverb<br>downwards – spectral modeling style effects                                                |
| 52  | pretrained.decoder.inter_mlp.3.weight                 | rolling            | small room reverbs and various distortions                                                                                      |
| 52  | pretrained.decoder.inter_mlp.3.weight                 | drawing            | smearing and drone                                                                                                              |
| 60  | pretrained.decoder.output_params.weight               | rolling            | spectral modeling style effects                                                                                                 |
| 60  | pretrained.decoder.output_params.weight               | scaling            | scaling up – sinusoidal modeling, watery sounds<br>                                                                             |
| 60  | pretrained.decoder.output_params.weight               | drawing            | adds narrow-band noise of different frequencies                                                                                 |

---

## Example bending session video
The video shows a network bending session of a rhythmic DDSP model with use of a previously prepared _Bending Log_.

<iframe width="100%" src="https://www.youtube.com/embed/7mH7LqVvBSc?si=4zhFd8AL7RIuwypu" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

---

## Example model blending session video
This video documents a process of _Model Blending_ two different DDSP models.

<iframe width="100%" src="https://www.youtube.com/embed/7mH7LqVvBSc?si=4zhFd8AL7RIuwypu" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

---

## Pd patch and external

*(This section will be filled out later with details about the Pure Data patch and any relevant externals)*
