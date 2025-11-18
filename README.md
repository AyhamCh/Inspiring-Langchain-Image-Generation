# Image Style Generator

This project takes an input image and generates a set of new images inspired by it, each rendered in a different artistic style such as pop art, jazz, hand-drawn, anime, and more. It uses LangChain to orchestrate prompt generation and AI image-generation models.

## Overview

The goal of this project is to automate the creation of multiple stylistic variations from a single reference image. The system accepts a local image path, applies predefined style prompts, and produces output images for each selected theme.

## Features

- Generates multiple styled images from one reference image
- Supports a wide range of themes (pop, jazz, hand-drawn, anime, digital art, abstract, etc.)
- Modular design using LangChain
- Organized output directory structure
- Easy to extend with new artistic themes
- Jupyter Notebook included for experimentation

## Technology Stack

- Python 3.10+
- LangChain
- AI Image Generation API (OpenAI, Stability AI, etc.)
- Jupyter Notebook
- Pillow (optional, for processing or previewing images)


## Usage

1. Specify the input image path

```python
input_image = "images/original.jpg"
```

2. Select the themes to generate

```python
themes = ["pop", "jazz", "handdraw", "anime"]
```

3. Generate images

```python
generator.generate_images(input_image, themes)
```

## Output

Generated images are saved in:

```
outputs/<theme_name>/
```

## Project Structure

```
project/
│
├── images/               # Input images
├── outputs/              # Generated results
├── notebook.ipynb        # Main workflow
├── generator.py          # Optional class-based implementation
├── README.md             # Documentation
└── requirements.txt      # Dependencies
```

## Extending the Project

You can add new styles by updating the style prompt dictionary:

```python
style_prompts["watercolor"] = "A watercolor-style interpretation of the reference image."
```

The system will handle the generation automatically.

## Requirements

- Python 3.10 or higher
- Internet connection for API requests
- API key for the chosen image-generation model
