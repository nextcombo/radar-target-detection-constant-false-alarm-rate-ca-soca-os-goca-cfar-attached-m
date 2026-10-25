# Radar Target Detection - Constant False Alarm Rate (CA/SOCA/OS/GOCA-CFAR) [Attached MATLAB Code]

MATLAB main code:
clear; close all; clc;
function [position, threshold, start_cell, stop_cell] = cacfar(signal, Pfa, ref_num, guard_num)\n    % ======>INPUT:\n    % signal: Data of signal(include signal and noise).[DATATYPE: row vector]\n    % Pfa: Probability of false alarm.[DATATYPE: scalar]\n    % ref_num: Number of reference cell.[DATATYPE: scalar]\n    % guard_num: Number of guard cell.[DATATYPE: scalar]\n    % ======>OUTPUT:\n    % position: positions of target.[DATATYPE: row vector]\n    % threshold: CFAR threshold of input signal.[DATATYPE: row vector]\n    position = [];\n    left_num = guard_num + ref_num;\n    start_cell = left_num + 1;\n    stop_cell = length(signal) - left_num;\n    N = 2*ref_num;\n    alpha = N * (Pfa ^ (-1/N) - 1);\n​\n    threshold = zeros(1, stop_cell - start_cell + 1);\n    for ii = start_cell : stop_cell\n        tmp_data = [signal(ii-left_num : ii-guard_num-1), ...\n                    signal(ii+guard_num+1 : ii+left_num)];\n        tmp = mean(tmp_data) * alpha;\n        % threshold(ii - left_num)\n        % tmp\n        threshold(ii - left_num) = tmp;\n        if tmp < signal(ii)\n            position = [position, ii];\n        end\n    end\nreturn\n  
MATLAB Simulation Results:  
\tSOCA/OS/GOCA-CFAR Code:

## Images

![Constant False Alarm Rate Detection in Radar Target Detection (CA/SOCA/OS/GOCA-CFAR) [with MATLAB Code]](01.jpg)
![Constant False Alarm Rate Detection in Radar Target Detection (CA/SOCA/OS/GOCA-CFAR) [with MATLAB Code]](02.jpg)
![Constant False Alarm Rate Detection in Radar Target Detection (CA/SOCA/OS/GOCA-CFAR) [with MATLAB Code]](03.jpg)
![Constant False Alarm Rate Detection in Radar Target Detection (CA/SOCA/OS/GOCA-CFAR) [with MATLAB Code]](04.jpg)
![Constant False Alarm Rate Detection in Radar Target Detection (CA/SOCA/OS/GOCA-CFAR) [with MATLAB Code]](05.jpg)
![Constant False Alarm Rate Detection in Radar Target Detection (CA/SOCA/OS/GOCA-CFAR) [with MATLAB Code]](06.jpg)
![Constant False Alarm Rate Detection in Radar Target Detection (CA/SOCA/OS/GOCA-CFAR) [with MATLAB Code]](07.jpg)
![Constant False Alarm Rate Detection in Radar Target Detection (CA/SOCA/OS/GOCA-CFAR) [with MATLAB Code]](08.jpg)
![Constant False Alarm Rate Detection in Radar Target Detection (CA/SOCA/OS/GOCA-CFAR) [with MATLAB Code]](09.jpg)
![Constant False Alarm Rate Detection in Radar Target Detection (CA/SOCA/OS/GOCA-CFAR) [with MATLAB Code]](10.jpg)
![Constant False Alarm Rate Detection in Radar Target Detection (CA/SOCA/OS/GOCA-CFAR) [with MATLAB Code]](11.jpg)
![Constant False Alarm Rate Detection in Radar Target Detection (CA/SOCA/OS/GOCA-CFAR) [with MATLAB Code]](12.jpg)
![Constant False Alarm Rate Detection in Radar Target Detection (CA/SOCA/OS/GOCA-CFAR) [with MATLAB Code]](13.jpg)
![Constant False Alarm Rate Detection in Radar Target Detection (CA/SOCA/OS/GOCA-CFAR) [with MATLAB Code]](14.jpg)
![Constant False Alarm Rate Detection in Radar Target Detection (CA/SOCA/OS/GOCA-CFAR) [with MATLAB Code]](15.jpg)
![Constant False Alarm Rate Detection in Radar Target Detection (CA/SOCA/OS/GOCA-CFAR) [with MATLAB Code]](16.jpg)
![Constant False Alarm Rate Detection in Radar Target Detection (CA/SOCA/OS/GOCA-CFAR) [with MATLAB Code]](17.jpg)
![Constant False Alarm Rate Detection in Radar Target Detection (CA/SOCA/OS/GOCA-CFAR) [with MATLAB Code]](18.jpg)
![Constant False Alarm Rate Detection in Radar Target Detection (CA/SOCA/OS/GOCA-CFAR) [with MATLAB Code]](19.jpg)
![Constant False Alarm Rate Detection in Radar Target Detection (CA/SOCA/OS/GOCA-CFAR) [with MATLAB Code]](20.jpg)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
