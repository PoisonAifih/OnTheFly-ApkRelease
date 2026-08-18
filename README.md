# Volare

An Android app for running and monitoring Cursor Cloud Agents from your phone.

Point an agent at one of your repositories, watch it work in real time, and open the pull request it produces. Finish the job by merging the pull request on GitHub.

- Start an agent from a prompt on any repository your Cursor account can reach
- Follow the transcript live as it works
- Send follow-ups or cancel a run in progress
- Get a notification when a run finishes, even after you close the screen
- Jump straight to the pull request it opened

## Install

Download the latest `volare-*.apk` from
[Releases](https://github.com/PoisonAifih/Volare-ApkRelease/releases/latest), open it on your phone, and allow installs from unknown sources when prompted. Android 8.0/Sdk 26 or newer is required.

## Setup

The app calls the Cursor API on your behalf, so it needs your own API key. Create one at [cursor.com/dashboard/api](https://cursor.com/dashboard/api) and paste it in on first launch.

The key is encrypted with a key held in the Android Keystore and never leaves your device.
Everything the app shows you (repositories, agents, runs) belongs to whichever account that key came from. If you lose the phone, revoke the key from the dashboard.

## Updates

The app updates itself. The overflow menu on the agent list has **Check for updates**, which compares your installed build against `latest.json` in this repository, then downloads and installs the newer APK.

Every build is signed with the same key, so updates install cleanly over the previous version. That signature is also what protects the channel: an APK built by anyone else is rejected by Android rather than installed as an update.

## What is in this repository

Signed release builds and the `latest.json` manifest the app reads, both published automatically by CI. The source code lives in a separate repository (private as of now, will be public in the future ◝(ᵔᗜᵔ)◜).
