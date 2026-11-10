# Bootrig

Sets up a new Windows PC with one download instead of installing every app by hand.
Live site: https://bootrig.com

## How it works
- Pick apps on the website (300+ available).
- Download a small installer written in C# on .NET Framework 4.8,
  which is already on every Windows 10/11 PC.
- The installer fetches a digitally signed install plan and checks the signature
  before doing anything. A tampered plan is refused.
- Apps are installed through WinGet, straight from each publisher. WinGet checks
  every file against its SHA-256 hash, so a swapped file won't install.
- Installs run silently: one admin (UAC) prompt, no wizards, apps you already
  have are skipped.

## For IT teams (in development)
Central web console, app baselines per team, automatic app updates on managed PCs,
role-based access and audit log, rollout via Intune, Group Policy or RMM.

The source code is private. Happy to walk through it in an interview.
