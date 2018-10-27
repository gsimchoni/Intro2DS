# How to Download Class Material

### Without Git:

1. Go to https://github.com/gsimchoni/Intro2DS

2. Click on "Clone or Download"

3. Click on "Download ZIP"

### With Git (assuming you have Git installed, and if not see `git_instructions.md` in this folder)

1. In terminal, go where you want to `Intro2DS` directory to be

2. Input:

	`git clone https://github.com/gsimchoni/Intro2DS.git`

# How to Run Class Jupyter Notebooks in Docker

1. In a terminal, go to `Intro2DS` location, e.g. in Windows:

	`cd C:/Intro2DS`

2. Run the container:

	Windows command-line: `docker run -it -p 8888:8888 -v %cd%:/home/joyvan --entrypoint=bash jupyter/tensorflow-notebook`

	Windows Powershell, Linux, Mac: `docker run -it -p 8888:8888 -v  ${PWD}:/home/joyvan --entrypoint=bash jupyter/tensorflow-notebook`

	This should download the `tensorflow-notebook` image from [Docker Hub](https://hub.docker.com/) (the first time).

	Then it will mount your current working library (C:\Intro2DS) so you can read from/write to it.

	Finally it will load a Linux (Ubuntu) terminal, something similar to:

	`jovyan@f16377e39355:~$`

	(Sometimes Docker on Windows will ask your Windows password (or Microsoft account password if you don't have one) to share the folder. Do it.)

	You are now in Linux land, with every python library you'll need, installed.

3. You can try inputting `ls` to see that your local libraries are indeed mounted to this container.

	You can try inputting `python --version` to see the python version you'll be working in (`3.6.6`).

4. Start Jupyter:

	`jupyter notebook`

	You should receive a message as if you were running `jupyter notebook` locally, to open the notebooks in your browser:

	> to login with a token:
	>       http://(8aa11443e34c or 127.0.0.1):8888/?token=94aab8e6c6a21606eeba9a76c3b4fe660f2287d270598

	Copy the URL into your browser and you should be able to see the `Intro2DS` directory and start working with notebooks, including saving your work locally.

	More comments:

	* If you ever had to install tensorflow you'd appreciate the speed.
	* This image includes all libraries we'll be working on in the course, including: pandas, numpy, sklearn, tensorflow, keras and more.
	* There are other Jupyter images [here](https://hub.docker.com/u/jupyter/), e.g. also including R.

5. Exiting:

	Stop Jupyter, returning to terminal: simply press `Ctrl + C` and answer `yes` if asked.

	Exit terminal and container: `exit`
