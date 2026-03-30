# 🚀 LEGEND remage Environment Setup Guide (macOS)

This is a step-by-step tutorial/introduction for macOS users to set up an environment for [LEGEND remage](https://remage.readthedocs.io/en/stable/index.html) simulations, and actually run some rather easier examples. I hope this document is comprehensive and straightforward enough that even those who know basically nothing about dealing with terminals, creating environments, or coding in Python, are able to understand and use it, without spending too much time digging through offical documentations from LEGEND and feeling lost.

We will start all the way from an introduction to what remage is, then move on to installing required packages and setting up the proper environment. After that, we will walk through examples in [remage basic tutorial](https://remage.readthedocs.io/en/stable/tutorial.html). By completing these steps should help you become familiar with building/running simulations and prepare you to tackle more challenging tasks.

So let's start, shall we?

<details>
<summary> I use VS Code. </summary>
I use Visual Studio Code (VS Code) as editor for its tidiness, thus all the following procedures will be done on VS Code. To be honest, I'm not sure whether other code editors will work or not. You can try, but I don't know. Sorry.
</details>

---

## What is remage?
Copied from their official webside, *remage* is a modern simulation framework for low-background physics experiments. You can think of it as a well-constructed Python library that allows you to write codes with it to simulate laboratory equipment, design experiments, and collect data for your particle physics research.

## Building Environment
Now you already know what *remage* is for! So it's time to build a cozy house for this genie to perform her magic. YOUR BEAUTIFUL MacOS LAPTOP is the cozy house, and for every project you work on, you need to create a "room" (i.e. folder) for it. Of course, you have to install corresponding packages for each room you create.

Before we really create a room/folder, we need to make sure our house is settled, otherwise we won't be able to install packages in the rooms (You will understand why later). Please follow the steps below carefully to make sure the house is cozy enough for Ms.Remage.

## Settle your House/MacOS
Start your VS Code, and open the terminal in it. If you don't know where to find, see below:
<p align="center">
<img width="49%" height="1003" alt="terminal1" src="https://github.com/user-attachments/assets/5d2909c5-2dc4-42b6-96bf-2c5db105fc6b" />
<img width="49%" height="1002" alt="terminal2" src="https://github.com/user-attachments/assets/f71c467f-79fc-4c80-abfc-0d66667978f5" />
</p>

In the terminal, you should find a string of text with a "%" at the end. By typing specific commands after "%", you get to interact with the terminal, thus being able to settle your computer (i.e. make you house cozy).

### 💻 Step 1: Install Homebrew
Homebrew is a very powerful "package manager" for macOS, and you can think of it as the "App Store" for terminals. We need Homebrew to acquire packages and dependencies, so go to the website of [Homebrew](https://brew.sh) and copy the command. The command should look something like this:
```bash
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
Paste it right after that "%" in your terminal and press "Enter".

<details>
<summary> Don't paste that "$". </summary>
The "$" at the beginning of commands is just a notation specifying that these commands should be run in terminals, not cells of files in your projects. In this case, your terminal should look something like "... % /bin/bash -c ..." before pressing Enter.
</details>

### 🍺 Step 2: Install Dependencies

## Create a Room/Folder

### 📂 Step 1: Open a Folder

### 🐍 Step 2: Create Python Virtual Environments

### 📦 Step 3: Install Packages

## Running Simulations







---

### 📂 Step 0: The Workspace
Before we begin, create a dedicated folder for your simulations on your computer and open it in **VS Code**. Open an integrated terminal in VS Code to run the following commands.


## 🍺 Step 1: Install Homebrew
Homebrew is the ultimate package manager for macOS. We will use it to install our underlying system dependencies.

```bash
# Install Homebrew (It will ask for your Mac password. Typing is invisible, which is normal!)
/bin/bash -c "$(curl -fsSL [https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh](https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh))"
```

<details>
<summary>💡 點我展開看進階說明 (Click to expand)</summary>

這裡面可以放任何妳想隱藏的內容！
而且**完全支援** Markdown 語法喔！

像是放一段程式碼：
```bash
echo "Hello, LEGEND!"
```
</details>

Lebron james
