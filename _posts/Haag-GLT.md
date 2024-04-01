---
layout: post
title:  On the issue Haag's theorem and Gell-Man and Low theorem
date:   2021-01-20 16:40:16
description: 
tags: 
categories: 
---
The interacting field does not live on the same Hilbert space as of the free field. The Hilbert space of an interacting theory is usually unknown and might not even exist. Rudolf Haag, in 1955, posed this conundrum of having no interaction picture in quantum field theory. His theorem states that there is no unitary mapping between the state space of interacting fields and that of a free fields. So one cannot write the ground state of the interacting theory in terms of states of a free field, at least unperturbatively.

Well, one does attempt to write the ground state perturbatively which assumes some overlap between the ground state and the vacuum state of interacting and free theory, respectively. 

$$\begin{equation}\label{1.4}
    U(t,\pm\infty)\ket{0}=\braket{\Omega|0} V(t)\ket{\Omega},
\end{equation}$$
where 

$$U(t,s)=V(t)V(s)^\dagger=e^{iH_0t}e^{-iH(t-s)}e^{-H_0s}\; \text{and}\,H=H_0+H_I.$$ 

This is the basis of Gell-Mann and Low formula, and (1.4) maps the ground state of the interacting theory to the free vacuum. But this outright contradicts with Haag's theorem on existence of such unitary maps. So the question is who is correct, Rudolf Haag or Murray Gell-Man and Francis Low? 

There are several opinions on Haag's theorem in various literature and on the internet. Some consider it to be ``morally wrong" and ``an excuse for someone who doesn't want to study particle physics", and some look at the issue more respectfully. I agree that a theorem is only as powerful as its assumptions and also in the argument - \textit{`ex falso quodlibet'}, but such arguments should hold for both the theorems. Even Gell-Mann and Low formula has a dodgy derivation in QFT when done using the interaction picture (it can also be seen from a generating functional), and we pay the price by having to deal with infinities. But it is not in vain, scattering theory, formulated under the interaction picture, works, and experiments are the witness. So either of the theorems is based on well defined, or ill-defined, set of assumptions. But which one? 

In this repertoire, we in no scope will answer this question and would simply base our analysis using the Gell-Man and Low theorem. We would calculate our two-point functions of the interacting field in the free vacuum. As far as I understand, Gell-Man and Low theorem works for experiments in high energy physics because at some level discretization of space and time, a discretized QFT, is required. Haag's theorem was originally formulated to hold only in continuous space-time and for translationally invariant theories. So that's one way of understanding why Gell-Man and Low theorem works. \textcolor{red}{Even though Haag's theorem as originally formulated doesn't apply to such discretized QFTs, the spirit of Haag's theorem still applies. It says that if you change the value of a coupling constant in the Lagrangian, then every state in the vacuum representation of one of those theories is very nearly orthogonal to every state in the vacuum representation of the other theory, approaching complete orthogonality as the continuum limit is approached. One implication of this is that even though small-coupling perturbation theory (as enabled by the Gell-Mann and Low theorem) works great for correlation functions (scattering amplitudes, etc), it doesn't work well at all for states. We can calculate QED scattering amplitudes very precisely using small-coupling perturbation theory, but we can't use that same approach to express the theory's true single-particle states in terms of the field operators when the coupling is nonzero, even if the coupling is tiny, because the perturbative approximation produces states that are nearly orthogonal to the true single-particle states.} As long as we're looking only at correlation functions, using Gell-Man and Low theorem is fine.        

