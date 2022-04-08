---
title: ExperimentqPCR
tags: [qPCR, Assays, DNA]
keywords: qPCR, Assays, DNA
last_updated: April 7, 2022
sidebar: mydoc_sidebar
permalink: mydoc_ExperimentqPCR.html
folder: mydoc
---

## Notes
- Default value for melting curve time is 2333s, which may not be desirable.

{% include important.html content="Default values for activation time, extension time, and denaturation time are not always correctly set for a given Master Mix. Confirm settings with the chosen Master Mix procotol." %}


## Example 1 - Multiple Samples
{% include code_header.html %}
```mathematica
(* Define Primers and Samples *)
forwardPrimer5 = Object[Sample, "id:bbb"];
reversePrimer5 = Object[Sample, "id:ccc"];
myPrimerPairs = {{{forwardPrimer5, reversePrimer5}},{{forwardPrimer5, reversePrimer5}}};
mySamples = {Object[Sample,"id:zzz"],Object[Sample,"id:aaa"]};
masterMix = Model[Sample, "Power SYBR Green PCR Master Mix"];

(* Protocol *)
myExperimentqPCR = ExperimentqPCR[
	mySamples,
	myPrimerPairs,
	MasterMix -> masterMix,
	NumberOfReplicates -> 3,
	ActivationTime -> 10 Minute,
	ExtensionTemperature -> 60 Celsius,
	MeltingCurveTime -> 233 Second,
	DenaturationTime -> 60 Second,
	Name -> "qPCR Experiment 001"
]
```

{% include code_header.html %}
```bash
ls -l
```

{% include links.html %}
