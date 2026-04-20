---
layout: post
title:  "Lyapunov-Guided Self-Alignment: Test-Time Adaptation for Offline Safe Reinforcement Learning"
date:   2026-04-20 20:21:59 +00:00
image: images/sas.png
categories: research
author: "Seungyub Han"
authors: "<strong>Seungyub Han*</strong>, Hyungjin Kim*, Jungwoo Lee (*equal contribution)"
venue: "AISTATS 2026"
paper: https://openreview.net/forum?id=GPNwYOQECX
arxiv:
slides:
code: https://github.com/seungyubhan/sas
---
We present SAS (Self-Alignment for Safety), a transformer-based framework for test-time adaptation in offline safe RL. At test time, the pretrained agent imagines rollouts, filters them via a Lyapunov condition, and recycles the safe segments as in-context prompts to realign behavior without any parameter updates. On Safety Gymnasium and MuJoCo benchmarks, SAS consistently reduces cost and failure while maintaining or improving return.
