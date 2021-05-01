# Architecture

## High Level

Electron consists of Chromium (displaying), NodeJS (file and operating system bridge) and custom APIs (native stuff).

## Process

### Main

Creates and manages `BrowserWindow`s and their corresponding Renderer processes (one per window).

### Renderer

Manages the corresponding web page, isolated from other processes. Communicates via IPC (inter-proc-comm) modules (ipcMain, ipcRenderer).
