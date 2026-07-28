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

<div class="diagram-container" style="background: var(--card-bg, #f8f9fa); border: 1px solid var(--border-color, #e9ecef); border-radius: 8px; padding: 1.5rem; margin: 2rem 0; text-align: center;">
  <h4 style="margin-top:0; font-size:1.1rem;">Data Flow: Standard vs. 00.ong Hardened</h4>
  <svg viewBox="0 0 700 180" width="100%" height="auto" xmlns="http://www.w3.org/2000/svg" style="max-width:700px;">
    <!-- Standard Flow -->
    <g transform="translate(10, 20)">
      <rect x="0" y="0" width="150" height="50" rx="6" fill="#ef4444" opacity="0.15" stroke="#ef4444" stroke-width="2"/>
      <text x="75" y="30" text-anchor="middle" fill="#dc2626" font-weight="bold" font-size="13">Default Windows 11</text>
      
      <path d="M 155 25 L 245 25" stroke="#ef4444" stroke-width="2" stroke-dasharray="4"/>
      <text x="200" y="18" text-anchor="middle" fill="#ef4444" font-size="10">Telemetry Traffic</text>

      <rect x="250" y="0" width="150" height="50" rx="6" fill="#ef4444" opacity="0.15" stroke="#ef4444" stroke-width="2"/>
      <text x="325" y="30" text-anchor="middle" fill="#dc2626" font-weight="bold" font-size="13">Cloud Diagnostic Servers</text>
    </g>

    <!-- 00.ong Hardened Flow -->
    <g transform="translate(10, 100)">
      <rect x="0" y="0" width="150" height="50" rx="6" fill="#10b981" opacity="0.15" stroke="#10b981" stroke-width="2"/>
      <text x="75" y="30" text-anchor="middle" fill="#059669" font-weight="bold" font-size="13">00.ong Hardened</text>
      
      <line x1="155" y1="25" x2="225" y2="25" stroke="#10b981" stroke-width="2"/>
      <circle cx="235" cy="25" r="10" fill="#ef4444"/>
      <text x="235" y="29" text-anchor="middle" fill="#fff" font-weight="bold" font-size="12">✕</text>
      
      <rect x="250" y="0" width="150" height="50" rx="6" fill="#9ca3af" opacity="0.15" stroke="#9ca3af" stroke-width="1.5" stroke-dasharray="2"/>
      <text x="325" y="30" text-anchor="middle" fill="#6b7280" font-weight="bold" font-size="13">Connections Blocked</text>
    </g>
  </svg>
  <p style="font-size: 0.875rem; color: #666; margin-top: 0.5rem; margin-bottom: 0;">Figure 1: Default Windows telemetry output vs. 00.ong hardened network blocking.</p>
</div>

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
