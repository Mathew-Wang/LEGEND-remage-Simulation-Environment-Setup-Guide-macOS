# 🚀 LEGEND remage Simulation Environment Setup Guide (macOS)

This is a step-by-step tutorial/introduction for macOS users to set up an environment for [LEGEND remage](https://remage.readthedocs.io/en/stable/index.html) simulations, and actually run some rather easier examples. I hope this document is comprehensive and straightforward enough that even those who know basically nothing about dealing with terminals, creating environments, or coding in Python, are able to understand and use it, without spending too much time digging through offical documentations from LEGEND and feeling lost.

We will start all the way from an introduction to what remage is, then move on to installing required packages and setting up the proper environment. After that, we will walk through examples in [remage basic tutorial](https://remage.readthedocs.io/en/stable/tutorial.html). By completing these steps should help you become familiar with building/running simulations and prepare you to tackle more challenging tasks.

So let's start, shall we?

<details>
<summary> I use VS Code. </summary>
I use Visual Studio Code (VS Code) as editor because of its tidiness. To be honest, I'm not sure whether other code editors will work or not. You can try, but I don't know. Sorry.
</details>

---

## What is remage?
Copied from their official webside, *remage* is a modern simulation framework for low-background physics experiments. You can think of it as a well-constructed Python library that allows you to write codes with it to simulate laboratory equipment, design experiments, and collect data for your particle physics research.

## Building Environment
Now you already know what *remage* is for! So it's time to build a cozy house for this genie to perform her magic. 








## 📂 Step 0: The Workspace
Before we begin, create a dedicated folder for your simulations on your computer and open it in **VS Code**. Open an integrated terminal in VS Code to run the following commands.

---

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
