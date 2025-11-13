<div class="project-card">
  <h3>AORF: Automated On-Rail Response Framework</h3>
  <p>A public safety solution for detecting and responding to railroad accidents in real time.</p>
  <a href="aorf.html" class="btn">View Project →</a>
</div>

# AORF — Automated Obstacle & Response Framework
Improving Public Safety through Smart Railroad Accident Detection and Emergency Response
## Overview
Every three hours, a vehicle or person is struck by a train in the U.S. Many of these incidents occur at unmanned crossings where emergency response is delayed.

AORF (Automated Obstacle & Response Framework) is an intelligent system designed to detect railroad accidents and automatically contact local emergency services in real time.

It integrates location-based APIs, Twilio communication, and IoT sensors to minimize response time and enhance public safety.
## Problem
Over 5,800 train-car collisions occur annually in the U.S.

Many are caused by unmanned railroads or delayed emergency notifications.

Average response times remain high due to the lack of real-time accident detection and data sharing.

## Solution

AORF detects sudden stops or speed changes in trains or vehicles and triggers an Emergency Response Module (ERM) that automatically:

Identifies nearest emergency contacts via the Precisely API (PSAP by location)

Sends SMS and email alerts using Twilio

Shares accident information, including:

Location (Latitude/Longitude)

Vehicle or goods info (oil, livestock, etc.)

Accident photos

Enables emergency planning such as:

Doctor notification

Traffic diversion

Hazardous material handling

# Program Flow
AORF detects an anomaly (sudden speed drop or operator trigger).

Latitude & Longitude of the accident are recorded.

ERM (Emergency Response Module) fetches local 911 and PSAP contact data using Precisely API.

Twilio sends SMS or email alerts with detailed info and images.

Authorities receive train info, accident pictures, and response guidance.

## APIs Used

| Component                                | Purpose                                                                     |
| ---------------------------------------- | --------------------------------------------------------------------------- |
| **Precisely API**                        | Fetches nearest Public Safety Answering Point (PSAP) and emergency contacts |
| **Twilio**                               | Sends real-time SMS and email alerts                                        |
| **IoT Sensors / Hummingbird Controller** | Detects sudden speed changes and triggers ERM                               |
| **Raspberry Pi (Next Phase)**            | Runs model, captures live video, and processes ML-based obstacle detection  |


## Design & Implementation
Hardware

Train model with Hummingbird controller

Sensors for speed and obstacle detection

(Planned) Raspberry Pi integration for image and video processing

Software

Python for API integration and communication logic

Precisely API for emergency contact retrieval

Twilio API for automated messaging

(Planned) ML model for obstacle validation


## Demonstration

Slide Deck
https://www.canva.com/design/DAFTSs_13Bc/C1jSLge_f5LW1sYnImLOXQ/edit?utm_content=DAFTSs_13Bc&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton

## Future Plans
Integrate computer vision for accurate obstacle detection

Launch drone surveillance for accident response validation

Implement Raspberry Pi deployment for portability and real-time processing

## Tools and Technology
Python

Precisely API

Twilio API

Hummingbird Controller

Raspberry Pi (planned)

Machine Learning (planned)
