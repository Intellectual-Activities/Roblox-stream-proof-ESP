# Roblox: Stream proof ESP

A Roblox ESP project that uses a Lua data collector with an external C++ overlay.

## How It Works

The Lua script collects player data and writes it to a file.

The external C++ application reads that data and renders the ESP through an external overlay.

## Usage

1. Run the external ESP application.
2. Execute the Lua data collector.

## Why use this?

Unlike traditional Roblox externals, this project does not rely on Roblox memory offsets for its ESP data. Traditional externals require offsets to be found and updated everytime Roblox updates, which can result in downtime until the external is updated.

This project instead uses an internal Lua data collector to provide the information needed by the external C++ renderer. This means the ESP itself is not dependent on Roblox offsets and should require little to no maintenance across Roblox updates.

The hybrid approach also allows the project to combine external rendering with functionality normally only implemented through Internal cheats. Future versions could expand beyond ESP into a complete external style interface controlling internal features such as autofarming, kill aura, Remote vulnerabilities, and other features which REAL externals cannot replicate all while being stream proof.

## What does stream proof mean?

Stream proof means the ESP overlay is excluded from supported screen capture methods. The ESP can remain visible on your monitor while being hidden from applications capturing the game window or display.

This is useful when recording, streaming, sharing your screen, or taking screenshots because the captured output can show the game without the ESP overlay.

> **Note:** Whether the overlay is hidden depends on the capture method and application. No implementation can guarantee compatibility with every possible capture method.

## What apps does this work for?

The stream proof functionality is designed to work with common capture applications and methods, including:

* Discord screen sharing
* OBS and other recording/streaming software
* Screenshot and screen capture utilities
* Game/window capture
* Many other applications that use standard Windows capture APIs

Compatibility can vary depending on the application's capture method and settings.

## Notes

- The Lua collector and external application must both be running for the ESP to update correctly.
