# 🚀 LEGEND remage Environment Setup Guide (macOS)

This is a step-by-step tutorial/introduction for macOS users to set up an environment for [LEGEND remage](https://remage.readthedocs.io/en/stable/index.html) simulations, and actually run some rather easier examples. I hope this document is comprehensive and straightforward enough, that even if you know nothing about dealing with terminals, creating environments, or coding in Python, you can still understand and use it. My main goal is to help you have a grasp of simulation running, without spending too much time digging through offical documentations from LEGEND and feeling lost.

We will start all the way from an introduction to what remage is, then move on to installing required packages and setting up the proper environment. After that, we will walk through examples in [remage basic tutorial](https://remage.readthedocs.io/en/stable/tutorial.html). By completing these steps should help you become familiar with building/running simulations and prepare you to tackle more challenging tasks.

So let's start, shall we?

<details>
  
<summary> I use VS Code. </summary>

I use **Visual Studio Code (VS Code)** as editor for its tidiness, thus all the following procedures will be done on VS Code. To be honest, I'm not sure whether other code editors will work or not. You can try, but I don't know. Sorry.

</details>

---

## What is remage?

Copied from their official webside, *remage* is a modern simulation framework for low-background physics experiments. You can think of it as a well-constructed Python library that allows you to write codes with it to simulate laboratory equipment, design experiments, and collect data for your particle physics research.

<br>

## Building Environment

Now you already know what *remage* is for! So it's time to build a cozy house for this genie to perform her magic. YOUR BEAUTIFUL MacOS LAPTOP is the cozy house, and for every project you work on, you need to create a "room" (i.e. folder) for it. Of course, you have to install corresponding packages for each room you create.

Before we really create a room/folder, we need to make sure our house is settled, otherwise we won't be able to install packages in the rooms (You will understand why later). Please follow the steps below carefully to make sure the house is cozy enough for Ms.Remage.

<br>

## Settle your House/MacOS

Start your VS Code, and open the terminal in it. If you don't know where to find, see below:

<p align="center">

<img width="45%" height="1009" alt="terminal1" src="https://github.com/user-attachments/assets/39021061-963e-4925-90c0-3a8ae046d9e1" />

<img width="45%" height="1007" alt="terminal2" src="https://github.com/user-attachments/assets/3e02f192-3b2a-48af-b434-d45a8c8507dd" />

</p>

In the terminal, you should find a string of text with a "%" in the end. By typing specific commands after "%", you get to interact with the terminal, thus being able to settle your computer.

<br>

### 💻 Step 1: Install Homebrew

#### Step 1.1: Homebrew Installing Command

Homebrew is an extremely powerful "package manager" for macOS, and you can think of it as the "App Store" for terminals. We need Homebrew to acquire packages and dependencies, so go to the website of [Homebrew](https://brew.sh) and copy the command on home page. The command should look something like this:

```bash
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Paste it right after that "%" in your terminal and press "Enter".

<details>

<summary> Don't paste that "$". </summary>
The "$" at the beginning of commands is just a notation specifying that these commands should be run in terminals, not cells of files in your projects. In this case, your terminal should look something like
  
"... % /bin/bash -c ..." before pressing Enter.

</details>

#### Step 1.2 Enter Password

Then, you should see your terminal asking you to *enter password*. Type the password of your **Apple account** (i.e. the one you use to log in your macOS) directly and press Enter.

<details>

<summary> Your password won't show. </summary>
It's completely normal that the typed letters are invisible. Don't panic, nothing is wrong, they're just trying to protect your privacy.

</details>

#### Step 1.3 Add Homebrew to your Path

Now there's only one step left for installing Homebrew: Scroll through your terminal and look for 

**===> Nest steps:**

Find all commands start with *echo* or *eval*, paste and run them in the terminal ONE BY ONE.

That is, you should find commands like

```bash
$ echo >> /Users/[your_username]/.zprofile
```

```bash
$ echo 'eval "$(/opt/homebrew/bin/brew shellenv zsh)"' >> /Users/[your_username]/.zprofile
```

```bash
$ eval "$(/opt/homebrew/bin/brew shellenv zsh)"
```

in the section with the title of "===> Nest steps:". ONE AT A TIME, copy one and paste it after the "%" in your terminal, then press Enter.

<details>

<summary> Why echo and eval? </summary>

Merely installing Homebrew in your computer is not enough. We also need to add Homebrew to your path permanently, so that every time you open a terminal in VS Code, it automatically "traces" where Homebrew is. Commands begin with "echo" ann "eval" are assigned to finish this job, and without doing this, you won't be able to continue the following steps (i.e. installing dependencies via commands begin with "brew").

</details>

### 🍺 Step 2: Install Dependencies

Now you already have a powerful installing tool (i.e. Homebrew!), and it's time to get your cozy house done. Run the command below in your VS Code terminal:

```bash
$ brew install opencascade cgal gmp mpfr boost vtk
```

and you have successfully installed all the dependencies needed to acquire packages later. Your house is nicely settled.

<details>

<summary> About dependencies... </summary>
The above command "brew install opencascade cgal gmp mpfr boost vtk" means that

you use **Homebrew** (now you know why we need to install Homebrew first) to **install** dependencies including **OpenCASCADE, CGAL, GMP, MPFR, Boost** and **VTK**. These dependencies play fundamental rules in installing packages (e.g. legend-pygeom-hpges, legend-pygeom-tools, ...) in your rooms/folders.

Also, since Homebrew and dependencies installed with Homebrew are directly built in your macOS(house), you only have to install them ONCE. They will stay in your mac forever once installed, and can be utilized by all rooms in your house permanently. On the contrary, packages(legend-pygeom-hpges, legend-pygeom-tools, ...) built in rooms cannot be shared by other rooms. Each time you create a new folder, you will need to install same packages in it again.

</details>

## Create a Room/Folder

Our house is done, so let's deal with the rooms:

### 📂 Step 1: Open a Folder

Create a folder in your macOS, and open it in VS Code.

### 🐍 Step 2: Create a Python Virtual Environment

The reason why we need to create virtual environments in rooms is to make sure every single room is independent, such that packages, kernels, or edition of Python used in a room won't interfere other rooms.

Hence, after you open the folder in VS Code, run the following commands (one-by-one; in terminal):

```bash
# create a virtual environment
$ python3 -m venv legend_env

# open the virtaul environment
$ source legend_env/bin/activate
```

<details>

<summary> Naming </summary>

In this case, I named the virtual environment "**legend_env**", so that's why the two commands above both include "legend_venv" in the end. You don't have to copy me exactly, just make sure they have the form of:

```bash
# create a virtual environment
$ python3 -m venv [environment_name]

# open the virtaul environment
$ source [environment_name]/bin/activate
```

</details>

<details>

<summary> How to close the environment </summary>

If you want to get out of the virtual environment, run this:

```bash
# close the virtaul environment
$ deactivate
```

It will undo the process of opening the virtaul environment, but it won't delete the environment you create from the room/folder.

</details>

### 📦 Step 3: Install Packages



<details>

<summary> pip vs. brew </summary>

```bash
$ pip install --upgrade pip
$ pip --version
```

</details>

These packages and venv are in your room so for new rooms new installation. Homebrew, dependencies not the case.

## Running Simulations







---
