---
layout: home
title: "Enhancing Neural Speech Embeddings for Generative Speech Models"
---
###### Submitted to IWAENC 2024

### Authors

Doyeon Kim, Yanjue Song, Nilesh Madhu, and Hong-Goo Kang

### Proposed Method

<img src="overall.png" width="80%" height="30%" title="px(픽셀) 크기 설정" alt="Proposed framework overview"></img>\
We consider a speech enhancement setup where neural speech embeddings, obtained from pre-trained self-supervised learning (SSL) models applied to the noisy signal, are subsequently input to a neural vocoder to synthesize the underlying clean speech. The key innovation is in enhancing these latent neural embeddings to mitigate the distortions due to noise and reverberation, resulting in a superior quality of the synthesized signal. Separating the task, thus, into distinct _embedding enhancement_ and _speech generation_ phases permits increased flexibility in network design. We further explore the benefit of combining the hidden states from the SSL model in a learnable manner, to produce a more robust embedding as the vocoder input. Finally, we also investigate different loss functions for training the neural vocoder. Experimental results validate the effectiveness of our proposed approach, particularly in scenarios characterized by concurrent background noise and reverberation. 

### Samples
- __Clean Vocoder__: trained to synthesize the *clean speech signals* from embeddings extracted from the *clean* 
- __Denoising Vocoder__: trained to synthesize *clean speech signals* from distorted embeddings extracted from the *distorted* input signals 
- __Proposed__: trained to synthesize *clean speech signals* from enhanced embeddings extracted from the *distorted* input signals and enhanced from the embedding enhancement network 
- __HuBERT__: trained clean vocoder using learnable weighted summation of *pre-trained HuBERT* model with the generator loss only 
- __WavLM__: trained clean vocoder using learnable weighted summation of *pre-trained WavLM* model with the generator loss only 
- __TERA__: trained clean vocoder using learnable weighted summation of *pre-trained TERA* model with the generator loss only 

<table>
  <thead>
    <tr>
      <th>Sample</th>
      <th>Clean Vocoder</th>
      <th>Denoising Vocoder</th>
      <th>Proposed</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Sample 1</td>
      <td><audio controls  src="p232_002.wav"> </audio></td>
      <td><audio controls  src="p232_002.wav"> </audio></td>
      <td><audio controls  src="p232_002.wav"> </audio></td>
    </tr>
    <tr>
      <td>Sample 2</td>
      <td><audio controls  src="p232_002.wav"> </audio></td>
      <td><audio controls  src="p232_002.wav"> </audio></td>
      <td><audio controls  src="p232_002.wav"> </audio></td>
    </tr>
    <tr>
      <td>Sample 3</td>
      <td><audio controls  src="p232_002.wav"> </audio></td>
      <td><audio controls  src="p232_002.wav"> </audio></td>
      <td><audio controls  src="p232_002.wav"> </audio></td>
      </tr>
  </tbody>
</table>



<table>
  <thead>
    <tr>
      <th>Sample</th>
      <th>HuBERT</th>
      <th>WavLM</th>
      <th>TERA</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Sample 1</td>
      <td><audio controls  src="p232_002.wav"></audio></td>
      <td><audio controls  src="p232_002.wav"> </audio></td>
      <td><audio controls  src="p232_002.wav"> </audio></td>
    </tr>
    <tr>
      <td>Sample 2</td>
      <td><audio controls  src="p232_002.wav"> </audio></td>
      <td><audio controls  src="p232_002.wav"> </audio></td>
      <td><audio controls  src="p232_002.wav"> </audio></td>
    </tr>
    <tr>
      <td>Sample 3</td>
      <td><audio controls  src="p232_002.wav"> </audio></td>
      <td><audio controls  src="p232_002.wav"> </audio></td>
      <td><audio controls  src="p232_002.wav"> </audio></td>
    </tr>
  </tbody>
</table>
