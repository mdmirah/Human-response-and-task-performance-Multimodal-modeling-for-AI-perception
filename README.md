# Human Behavior and Task Performance Modeling for AI Perception

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.7+](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![AIAA Paper](https://img.shields.io/badge/AIAA%20Scitech%202026-2734-red.svg)](https://doi.org/10.2514/6.2026-2734)

A comprehensive framework for analyzing human performance states by integrating physiological signals (heart rate, pupil diameter) with task performance metrics (deviation, rate of change). Designed for aviation psychology research and AI-based operator state monitoring.

## 📄 Citation and Academic Context

The theoretical framework and core methodology implemented in this repository were originally published in:

**Rahman, M. M., & Fala, N. (2026). "A Multimodal Framework for Assessing Fitness to Fly in Flight Training."** *AIAA Scitech 2026 Forum*, Paper AIAA 2026-2734. https://doi.org/10.2514/6.2026-2734

This paper introduces the **Fitness-to-Fly (F2Y)** score, an operational construct that integrates a pilot's heart rate with flight performance metrics to estimate their internal state of fitness. The framework defines four F2Y states (Relaxed Controlled, Stressed Controlled, Relaxed Uncontrolled, and Stressed Uncontrolled) and addresses the critical disconnect between psychophysiological measures and flight performance that individual methods cannot capture.

**If you use this code in your research, please cite both the original paper (for the theoretical framework) and this repository (for the code implementation).**

## 🎯 Key Features

- **Multi-dimensional State Classification**: Combines physiological and performance metrics for holistic operator state assessment based on the F2Y framework
- **Dynamic Thresholding**: Adapts performance thresholds based on JASAT (Just Another Source of Action Time)
- **Comprehensive Statistics**: Calculates state durations, transitions, and episode analysis
- **Rich Visualizations**: Generates publication-quality plots with state-based coloring
- **Self-Transition Tracking**: Includes same-state persistence in transition analysis

## 📊 State Classification Logic (F2Y Framework)

The system classifies operator states along two dimensions as defined in Rahman & Fala (2026):

### Physiological State (HR/PD)
- **Stressed**: High Heart Rate AND High Pupil Diameter
- **Relaxed**: Any other combination

### Performance State
- **Controlled**: Low Deviation AND Low Rate of Change (Smooth)
- **Uncontrolled**: Any other combination

### Combined F2Y States
1. **Stressed Uncontrolled** 🔴 - High physiological arousal with poor performance
2. **Relaxed Uncontrolled** 🟠 - Low physiological arousal with poor performance  
3. **Stressed Controlled** 🔵 - High physiological arousal with good performance
4. **Relaxed Controlled** 🟢 - Low physiological arousal with good performance (Ideal state)

## 📚 Citation Guidelines

The Fitness-to-Fly (F2Y) framework used in this study was originally proposed by 
Rahman and Fala [1], and the implementation follows the open-source code repository 
accompanying that work [2].

[1] Rahman, M. M., and Fala, N., "A Multimodal Framework for Assessing Fitness to 
    Fly in Flight Training," AIAA Scitech 2026 Forum, AIAA Paper 2026-2734, 2026.
    doi: 10.2514/6.2026-2734

[2] Rahman, M. M., and Fala, N., "Human Behavior and Task Performance Modeling for 
    AI Perception," GitHub repository, 2026. https://github.com/yourusername/human-behavior-modeling
