# AR-Suraksha — System Architecture

## 1. Project Overview

AR-Suraksha is a proposed mobile AR vocational training simulator for industrial safety in Jharkhand's mining and manufacturing sector.

**SIH 2026 Problem Statement:** PS 26041

## 2. Architecture Components

### A. Android Application

* **Unity:** Development environment for the interactive 3D application.
* **C#:** Application logic, interactions, and assessment behaviour.
* **Purpose:** Provides the worker-facing training experience.

### B. Augmented Reality

* **AR Foundation:** Unity's framework for building AR experiences.
* **Google ARCore:** Provides supported Android AR capabilities.
* **Purpose:** Places virtual training elements into the worker's surroundings on compatible devices.

### C. Training and Assessment

* **3D Models and Animations:** Represent equipment, hazards, and safety scenarios.
* **Rule-Based Assessment Engine:** Evaluates predefined actions and answers using explicit scoring rules.
* **Initial module scope:** Fire and Explosion Response; Gas Leak and Confined-Space Safety.

### D. Offline Storage

* **SQLite:** Stores local training progress and assessment records.
* **Purpose:** Allows core training to work without continuous internet connectivity.

### E. Backend and Central Database

* **Python and FastAPI:** Proposed backend API and synchronization layer.
* **REST API:** Communication between the mobile application and backend.
* **PostgreSQL:** Central storage for worker records, assessment attempts, scores, and certificate records.

### F. Administration and Certificates

* **Web Dashboard:** Intended for authorized administrators to review training records and results.
* **QR-Based Verification:** A certificate identifier can be checked against the corresponding record.

## 3. Proposed Data Flow

1. The worker opens the Android application.
2. The worker completes an interactive AR safety scenario.
3. The assessment engine evaluates the worker's actions or answers.
4. Training progress and results are saved locally in SQLite.
5. When connectivity is available, pending records are sent to the backend API.
6. FastAPI validates and processes the records.
7. PostgreSQL stores the centralized records.
8. Authorized administrators access available records through the web dashboard.

## 4. Offline-First Design

Core training and assessment are intended to work offline. Records will be queued locally for synchronization when connectivity returns.

The implementation must confirm successful server receipt before marking pending records as synchronized.

## 5. Proposed Technology Stack

| Layer              | Technology                   |
| ------------------ | ---------------------------- |
| Mobile Application | Unity, C#                    |
| Augmented Reality  | AR Foundation, Google ARCore |
| Training Content   | 3D Models, Animations        |
| Assessment         | Rule-Based Engine            |
| Local Database     | SQLite                       |
| Backend            | Python, FastAPI              |
| API Communication  | REST API                     |
| Central Database   | PostgreSQL                   |
| Administration     | Web Dashboard                |

## 6. Development Status

This document describes the proposed architecture. Individual components will be updated as they are implemented, integrated, and tested.

## 7. Important Limitations

* AR functionality depends on device compatibility and successful tracking.
* Central synchronization and live certificate verification require connectivity unless an offline verification mechanism is separately implemented.
* Training completion certificates are not represented as government-recognized statutory certifications.
* The simulator is intended to support training, not replace official safety procedures or required professional instruction.
