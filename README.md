# FenixAIStudio
AI System for Music, Music Videos and Coding. 



It connects to **Ollama** and provides a cleaner interface for chatting with models, coding, testing outputs and running AI-assisted tasks locally on your own hardware.

This is an early **v0.1 release**, so expect a few rough edges.

## Features

* Local LLM support through Ollama
* Chat interface
* Coder workspace
* Model selection and management
* Configurable generation options
* Low VRAM mode
* Local-first operation
* Simple Windows startup
* Designed to work with a range of Ollama-compatible models

## System Requirements

### Recommended

For a good general experience:

* **Windows 10 or Windows 11**
* **NVIDIA RTX 3060 12 GB VRAM or better**
* **32 GB RAM**
* **100 GB free storage**
* **Python 3.10+**
* **Ollama**

The application itself does not require 100 GB of storage. The extra space is recommended because local LLM models can consume a lot of disk space.

### 8 GB VRAM Systems

Fenix AI Studio can also run on GPUs with **8 GB VRAM**.

If using an 8 GB GPU, enable:

**Options → Low VRAM**

You should also choose models and quantizations appropriate for the amount of VRAM and system memory available.

Larger models may still run by using system RAM, but performance can drop significantly.

## Installation

### 1. Install Python

Install Python 3.10 or newer.

Make sure **Add Python to PATH** is enabled during installation.

### 2. Install Ollama

Install Ollama and download at least one model.

For example:

```bash
ollama pull gemma3:4b
```

Use whatever model is suitable for your hardware.

### 3. Start Fenix AI Studio

Run:

```text
START.bat
```

On the first launch, the startup script will create the required Python virtual environment and install the required dependencies.

First launch will therefore take longer than normal.

Future launches will use the existing environment.

## General Usage

Start Ollama, then launch Fenix AI Studio using `START.bat`.

Select the model you want to use and choose the appropriate area of the program.

Different models have very different hardware requirements. A larger model is not automatically better for every task.

In many cases, a smaller model that fits comfortably inside your VRAM will provide a much better experience than a larger model that constantly needs to move data between GPU memory and system RAM.

## Memory Management

Local LLMs can use a significant amount of VRAM and system RAM.

Fenix AI Studio attempts to manage this sensibly, but the limits of your hardware still apply.

If you're using a slower or lower-memory system:

* Use models appropriate for your available VRAM.
* Enable **Low VRAM** mode where required.
* Avoid loading unnecessarily large models.
* Avoid running lots of tasks at the same time.
* Allow models time to load and unload when switching between them.
* Close other GPU-heavy applications if you're running low on VRAM.

### Don't Spam Tasks

Sending several tasks in rapid succession can create unnecessary memory pressure and slow everything down.

On slower systems, it is better to submit a task, allow it to finish, check the result, and then submit the next one.

Once you know what your hardware can comfortably handle, you can push it further.

## Be Patient With Final Results

On some systems, particularly slower machines or systems under heavy memory pressure, there can be a delay between the model finishing its generation and the completed result appearing in the interface.

This can happen while the final output is being transferred, processed or displayed.

If the model appears to have finished but the result has not appeared yet, **give it a little time**.

Repeatedly clicking the button or submitting the same task again can make things worse rather than speeding it up.

## Low VRAM Mode

If you have an **8 GB GPU**, Low VRAM mode is strongly recommended.

Enable it from the Options menu.

Low VRAM mode helps Fenix AI Studio operate more comfortably on systems with limited GPU memory, but model choice still matters.

An 8 GB GPU cannot magically run every model efficiently simply because Low VRAM mode is enabled.

## Known Issue — v0.1

There is currently one known issue with the **Coder script integration**.

Dropdown options inside the Coder script integration do not always correctly override the main Coder options.

Until this is fixed, the main Coder settings should be considered the authoritative settings when the two conflict.

## Demo Content

A demo song is included with the release for testing relevant features.

## Contributing

Fenix AI Studio is being released publicly so other people can use it, modify it and improve it.

Bug fixes, compatibility improvements, UI improvements and useful new features are welcome.

If you make something useful, contributing your changes back to the project is strongly encouraged so everyone can benefit from them.

## Licence

Fenix AI Studio is released under the:

**GNU Affero General Public License v3.0 — AGPL-3.0**

You are free to use, modify and redistribute the software under the terms of the AGPLv3.

If you distribute a modified version, the corresponding source code must remain available under the terms of the licence.

The AGPL also contains provisions covering modified versions of the software that are made available for users to interact with over a network.

See the `LICENSE` file for the full licence terms.

Third-party libraries and dependencies remain subject to their own respective licences.

## Version

**Fenix AI Studio v0.1**

Early public release.

Expect bugs, weird behaviour and improvements as development continues.
