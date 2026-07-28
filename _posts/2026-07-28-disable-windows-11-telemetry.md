---
title: "How to Disable Windows 11 Telemetry (5 Minute Setup)"
date: 2026-07-28 10:00:00 +0200
categories: [Privacy, Guides]
tags: [windows, telemetry, open-source, hardening]
description: "A quick 5-minute guide to disabling invasive telemetry in Windows 11 and taking control of system diagnostic tracking."
author: 00ong
steps:
  - name: "Open System Privacy Settings"
    text: "Navigate to Windows Settings -> Privacy & security -> Diagnostics & feedback."
  - name: "Turn Off Diagnostic Data Transmission"
    text: "Toggle Optional diagnostic data to Off and disable Tailored experiences."
  - name: "Apply the 00.ong Telemetry Shield Tweak"
    text: "Run the audited open-source script to block background tracking endpoints."
---

{% include tldr.html 
   what="Windows 11 transmits diagnostic logs, app usage metrics, and hardware IDs to cloud endpoints by default."
   why="Disabling telemetry protects personal privacy, saves background network bandwidth, and prevents diagnostic profiling."
   pick="Shield Rust Cleaner Pro"
   link_url="https://github.com/00ong" %}

## What is Windows Telemetry?
Windows Telemetry is an automated service in Windows 11 that collects system health statistics, diagnostic traces, and app activity data, sending it periodically to remote cloud servers.

{% include diagram_telemetry.html %}

## Step-by-Step Implementation Guide

### Step 1: Open System Privacy Settings
Press **Win + I** to launch **Settings**. Navigate to **Privacy & security** -> **Diagnostics & feedback**.

### Step 2: Turn Off Diagnostic Data Transmission
Set **Send optional diagnostic data** to **Off**. Next, expand **Tailored experiences** and toggle the setting to **Off** to stop customized recommendations based on diagnostic data.

### Step 3: Run the 00.ong Hardening Script
Download and run the open-source **Shield Rust Cleaner Pro** disabler engine to apply WinApp2-based privacy rules and disable background diagnostic services (`DiagTrack` and `dmwappushservice`).

## Further Reading & Trusted Open-Source Resources
* [Shield Rust Cleaner Pro Repository](https://github.com/00ong) — Open-source Windows cleanup and telemetry disabler engine.
* [Microsoft Diagnostics & Privacy Overview](https://learn.microsoft.com/) — Official documentation on Windows telemetry collection.
* [Privacy Guides: Windows Hardening](https://www.privacyguides.org/) — Community-curated recommendations for privacy-conscious users.
