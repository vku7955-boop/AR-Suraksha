# AR-Suraksha

**AR-Based Vocational Training Simulator for Industrial Safety**

## Problem Statement

**SIH 2026 — PS 26041**

AR-Based Vocational Training Simulator for Industrial Safety in Jharkhand's Mining and Manufacturing Sector.

## Overview

AR-Suraksha is a proposed mobile Augmented Reality (AR) training platform designed to help industrial workers learn and practise safety procedures through interactive simulations on compatible Android smartphones.

The project aims to make safety training more accessible through realistic scenarios, interactive assessments, offline functionality, and digital training records.

## Planned Features

* **Fire and Explosion Response:** Interactive practice of fire response and evacuation procedures.
* **Gas Leak and Confined-Space Safety:** Practice hazard recognition, PPE selection, and safe procedures.
* **Rule-Based Assessment:** Evaluate trainee decisions and calculate scores.
* **Offline-First Training:** Store training progress locally and synchronize records when connectivity is available.
* **QR-Based Certificates:** Generate and verify training completion records.
* **Regional Languages:** Hindi and Santali localization.
* **Admin Dashboard:** View worker records, assessment results, and certificate information.

## Proposed Technology Stack

| Component             | Technology                      |
| --------------------- | ------------------------------- |
| Android Application   | Unity and C#                    |
| Augmented Reality     | AR Foundation and Google ARCore |
| 3D Training Scenarios | 3D Models and Animations        |
| Assessment            | Rule-Based Assessment Engine    |
| Local Storage         | SQLite                          |
| Backend API           | Python and FastAPI              |
| Central Database      | PostgreSQL                      |
| Communication         | REST API                        |
| Administration        | Web Dashboard                   |

## Architecture Overview

The Android application provides interactive AR training and rule-based assessment. Training progress is stored locally using SQLite. When an internet connection is available, pending records can be synchronized through the backend API to the central database. Administrators can access centralized training records through the web dashboard.

## Development Status

**Current status:** Initial GitHub repository created. Technical design and implementation are in progress.

Planned features will be updated as they are implemented and tested.

## Intended Use

This project is intended for vocational training and educational purposes. It does not replace site-specific safety procedures, required professional training, or legally recognized industrial certification.

