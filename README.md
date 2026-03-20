# LambdaLink
A professional desktop controller for TDK Lambda Z+ / Genesys power supplies — built in Python with a clean dark-theme GUI, real-time waveform monitoring, automated power-cycle testing, and curve playback.

LambdaLink gives test engineers a clean, reliable desktop interface for controlling TDK Lambda programmable power supplies over RS-232 — replacing manual front-panel interaction with automated, scriptable test workflows.
Key features:

Stable serial connection — Uses the Win32 CreateFile API directly, bypassing a known pyserial bug that causes Error 31 on CH340 / CP2102 USB-to-serial adapters. The COM port handle is kept open between connect/disconnect cycles, eliminating USB firmware re-enumeration and making reconnect instant and reliable.
Real-time monitoring — 500 ms live readout of voltage, current, and power with a scrolling dual-Y waveform chart and timestamped TX/RX communication log.
Auto power cycle — Configurable count, ON time, and OFF time. Runs entirely in a background thread so the UI stays responsive throughout long test runs.
Curve playback — Import a V/I/hold-time profile from Excel or CSV and play it back step by step — ideal for burn-in, IV sweeps, and automated compliance testing.
Standalone EXE — Build a single .exe with PyInstaller; no Python installation required on the test bench.

Hardware: TDK Lambda Z+ / Genesys Series · RS-232 · 9600 baud 8N1
Requirements: Python 3.8+ · pyserial · matplotlib · openpyxl · Windows 10/11
