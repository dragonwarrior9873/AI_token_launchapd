# AI_token_launchapd


#### Allows you to automatically generate meme names, symbols, descriptions and images from start to finish using AI. It will generate the text for the meme (optionally based on a user-provided concept), create a related image, and combine the two into a final image file.
----------------------

## Features

- Uses OpenAI's GPT-4 to generate the meme name, symbol, description text and image prompt for the meme.
- Automatically sends image prompt request to an AI image generator of choice, then combines the text and image
- Allows customization of the meme generation process through various settings.
- Generates memes with a user-provided subject or concept, or you can let the AI decide.
- Logs meme generation details for future reference.

## Usage

1. For Python Version Only: Clone the repository & Install the necessary packages.
2. Obtain at least an OpenAI API key, but it is recommended to also use APIs from Clipdrop or Stability AI (DreamStudio) for the image generation stage.
3. Edit the settings variables in the settings.ini file.
4. Run the script and enter a meme subject or concept when prompted (optional).

## Settings

Various settings for the meme generation process can be customized:

- OpenAI API settings: Choose the text model and temperature for generating the meme text and image prompt.
- Image platform settings: Choose the platform for generating the meme image. Options include OpenAI's DALLE2, StabilityAI's DreamStudio, and ClipDrop.
- Basic Meme Instructions: You can tell the AI about the general style or qualities to apply to all memes, such as using dark humor, surreal humor, wholesome, etc. 
- Special Image Instructions: You can tell the AI how to generate the image itself (more specifically,  how to write the image prompt). You can specify a style such as being a photograph, drawing, etc, or something more specific such as always using cats in the pictures.

## Example Image Output With Log
![Screenshot_7](https://github.com/user-attachments/assets/25dcfc2d-0832-4ec7-b5ba-eb5e6fef46b9)

```
Meme File Name: meme_2025-01-09-15-28_1.png
AI Basic Instructions: You will create funny memes that are clever and original, and not cliche or lame.
AI Special Image Instructions: The images should be photographic.
User Prompt: 'anything'
Chat Bot Meme Text: "When your portfolio is in the red, but you're a Unfazed Unicorn, unfazed by the dips!"
Chat Bot Image Prompt: Photograph of a stoic unicorn staring at a plummeting stock graph with a carefree smile
Image Generation Platform: openai

```

## Optional Arguments
### You can also pass options into the program via command-line arguments whether using the python version or exe version.

#### • API Key Arguments: Not necessary if the keys are already in api_keys.ini
`--openaikey`: OpenAI API key.

`--clipdropkey`: ClipDrop API key.

`--stabilitykey`: Stability AI API key.

#### • Basic Meme Arguments

`--userprompt`: A meme subject or concept to send to the chat bot. If not specified, the user will be prompted to enter a subject or concept.

`--memecount`: The number of memes to create. If using arguments and not specified, the default is 1.

#### • Advanced Meme Settings Arguments

`--imageplatform`: The image platform to use. If using arguments and not specified, the default is 'clipdrop'. Possible options: 'openai', 'stability', 'clipdrop'.

`--temperature`: The temperature to use for the chat bot. If using arguments and not specified, the default is 1.0.

`--basicinstructions`: The basic instructions to use for the chat bot. If using arguments and not specified, the default is "You will create funny memes that are clever and original, and not cliche or lame.".

`--imagespecialinstructions`: The image special instructions to use for the chat bot. The default is "The images should be photographic.".

#### • Binary arguments: Just adding them activates them, no text needs to accompany them

`--nouserinput`: If specified, this will prevent any user input prompts, and will instead use default values or other arguments.

`--nofilesave`: If specified, the meme will not be saved to a file, and only returned as virtual file part of memeResultsDictsList.

## How to Build Exe Yourself
#### Note: To build the exe you have to set up the python environment anyway, so by that point you can just run the python version of the script. But if you want the build the exe yourself anyway here is how:
1. Ensure required packages are installed
2. Additionally, install PyInstaller: `pip install pyinstaller` (If using a virtual environment, install it into that)
3. Run this command in terminal from within the project directory: `python -m PyInstaller main.spec`



https://github.com/user-attachments/assets/f8455286-cbf8-4edc-abc5-29fdb9aab224

