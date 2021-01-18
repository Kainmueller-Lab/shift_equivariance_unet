# How Shift Equivariance Impacts Metric Learning for Instance Segmentation

PDF: https://arxiv.org/abs/2101.05846

Josef Lorenz Rumberger<sup>1</sup>
Xiaoyan Yu<sup>1</sup>
Peter Hirsch<sup>1</sup>
Melanie Dohmen<sup>1</sup>
Vanessa Emanuela Guarino<sup>1</sup>
Lisa Mais
Ashkan Mokarian
Dagmar Kainmueller  
<sup>1</sup>Authors contributed equally</br>

## Abstract

Metric learning has received conflicting assessments concerning its suitability for solving instance segmentation tasks. It has been dismissed as theoretically flawed due to the shift equivariance of the employed CNNs and their respective inability to distinguish same-looking objects.  
Yet it has been shown to yield state of the art results for a variety of tasks, and practical issues have mainly been reported in the context of tile-and-stitch approaches, where discontinuities at tile boundaries have been observed. To date, neither of the reported issues have undergone thorough formal analysis.  
In our work, we contribute a comprehensive formal analysis of the shift equivariance properties of encoder-decoder-style CNNs, which yields a clear picture of what can and cannot be achieved with metric learning in the face of same-looking objects.  
In particular, we prove that a standard encoder-decoder network that takes *d*-dimensional images as input, with *l* pooling layers and pooling factor *f*, has the capacity to distinguish at most *f^(dl)* same-looking objects, and we show that this upper limit can be reached.
Furthermore, we show that to avoid discontinuities in a tile-and-stitch approach, assuming standard batch size 1, it is necessary to employ valid convolutions in combination with a training output window size strictly greater than *f^l*, while at test-time it is necessary to crop tiles to size *n f^l* before stitching, with *n >= 1*.  
We complement these theoretical findings by discussing a number of insightful special cases for which we show empirical results on synthetic data.


## Overview

This repository contains the *jupyter* notebooks used for the experiments and to generate the figures.

## WIP

We will (soon) provide shift equivariant U-Net implementations for tensorflow and pytorch.
