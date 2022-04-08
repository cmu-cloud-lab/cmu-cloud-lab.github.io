---
title: ExperimentqPCR
tags: [qPCR, Assays, DNA]
keywords: qPCR, Assays, DNA
last_updated: April 7, 2022
sidebar: mydoc_sidebar
permalink: mydoc_ExperimentqPCR.html
folder: mydoc
---

## Code Examples
### Example 1 - Multiple Samples
{% include note.html content="Test note." %}

{% include important.html content="Test important." %}

{% include warning.html content="Test warning." %}

{% include tip.html content="Test tip." %}

{% include code_header.html %}
```Mathematica
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

{% include links.html %}
