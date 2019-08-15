---
layout: post
title: "Return Oriented Programming Survey Research Paper"
date: 2018-12-18
---

Return Oriented Programming Survey Research Paper
-------------------------------------------------

This paper was completed as a final project for a class called Computer Security. This paper surveys current defense mechanisms for Return Oriented Program attacks as well as offers suggestions for best use defense mechanisms moving forward.

Return Oriented Programing is where a call stack is tampered with to change the destinations of return statements. This allows an intruder to string gadgets together to accomplish a specific task that was not intended by the initial code.

My role within this project was to analyze current defense mechanisms as well as offer overarching analysis of the current landscape of ROP defenses. I analyzed the following defenses: SAT Solver, G-Free, Data Execution Prevention, Address Space Randomization and HyperCrop II. The conclusion regarding best defense mechanisms is that most techniques are susceptible to more recent and robust attacks with the exception of HyperCrop II as it has the ability to restrict return statements to stay within an immediate memory space and remain read only.

For further reading on the paper and my team's findings, the paper is available below.

<div class="blurb">
	<embed src="/../ROPSurvey.pdf" type="application/pdf" width="100%" height="600px" />
</div>
